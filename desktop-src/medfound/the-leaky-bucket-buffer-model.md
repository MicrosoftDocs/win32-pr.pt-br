---
description: A &\# 0034; o Bucket de vazamento&\# 0034; o modelo é uma maneira de modelar os requisitos de buffer para uma reprodução suave.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: O modelo de buffer de buckets vazados (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a99932fb121808f6a49323360c47c09d0acbb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105761582"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>O modelo de buffer de buckets vazados (Microsoft Media Foundation)

Quando você transmite mídia em uma rede, o decodificador recebe dados codificados em uma taxa teoricamente constante (a taxa de transmissão). O decodificador consome esses dados para produzir saída decodificada. No entanto, no caso geral, o decodificador consome os dados em uma taxa *variável* , porque o codificador pode usar uma taxa de codificação variável.

O modelo "Bucket de vazamentos" é uma maneira de modelar os requisitos de buffer para uma reprodução suave. Nesse modelo, o decodificador mantém um buffer. Os dados codificados vão da rede para o buffer e do buffer para o decodificador. Se o buffer fluir, isso significará que o decodificador está removendo dados do buffer mais rápido do que a rede que o está entregando. Se o buffer estourar, isso significa que a rede está entregando dados mais rápido do que o decodificador.

Este tópico descreve o modelo de "Bucket de vazamentos" de buffers para codificação e decodificação.

-   [O Bucket de vazamentos](#the-leaky-bucket)
-   [O Bucket em uso](#the-bucket-in-use)
-   [Definindo valores de Bucket vazado para fluxos ASF](#setting-leaky-bucket-values-for-asf-streams)
-   [Valores de buckets vazados no Multiplexador de ASF](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Atualizando valores de buckets vazados no coletor de mídia ASF](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Tópicos relacionados](#related-topics)

## <a name="the-leaky-bucket"></a>O Bucket de vazamentos

Para entender o modelo de Bucket vazado, considere um Bucket com um pequeno orifício na parte inferior. Três parâmetros definem o Bucket:

-   A capacidade (B)
-   A taxa na qual a água flui para fora do Bucket (R)
-   A totalidade inicial do Bucket (F)

Nessa metáfora, o Bucket é o buffer:

![ilustração mostrando um buffer como um Bucket, taxa de entrada como água entrando no Bucket e a taxa de saída como água saindo por meio de um orifício no Bucket](images/asf-components03.png)

Se a água for desapareceda no Bucket com a taxa exata de *R*, o Bucket permanecerá em F, porque a taxa de entrada é igual à taxa de saída. Se a taxa de entrada aumentar enquanto *R* permanecer constante, o Bucket acumulará água. Se a taxa de entrada for maior que *R* por um período sustentado, eventualmente, o Bucket estourará. No entanto, a taxa de entrada pode variar em relação ao *R* sem estourar o Bucket, desde que a taxa de entrada média não exceda a capacidade do Bucket. Quanto maior a capacidade, mais a taxa de entrada pode variar dentro de um determinado período de tempo.

No ASF, o Bucket de vazamento é definido por três parâmetros:

-   A taxa média de bits, em bytes por segundo, que corresponde à taxa de saída (*R*)
-   A janela de buffer, medida em milissegundos, que corresponde à capacidade do Bucket (*B*).
-   A totalidade do buffer inicial, que geralmente é definida como zero.

A taxa de bits mede o número médio de bits por segundo no fluxo codificado. A janela buffer mede o número de milissegundos de dados nessa taxa de bits que podem caber no buffer. O tamanho do buffer em bits é igual a R \* (B/1000).

Os dados de carga ASF podem inserir o Bucket de vazamento em horários irregulares e em quantidades irregulares, mas devem deixar o Bucket com uma taxa de bits positiva constante. Devido à janela de buffer, há um possível atraso entre a hora em que a carga entra no Bucket e quando ela sai. O atraso máximo que pode ocorrer é *B* / *R*. Os dados de carga que entram no Bucket são de acordo com a hora da apresentação e nunca devem exceder o Bucket. Além do tempo de apresentação, cada carga também tem um tempo de envio — a hora em que os dados de carga deixam o Bucket de acordo com a taxa de bits. A hora de envio deve ser anterior ao tempo de apresentação para garantir que, quando o Bucket de vazamentos ficar perto de estar cheio, cada carga deixará o Bucket antes ou em seu horário de apresentação. Para fazer isso, os tempos de apresentação são deslocados para frente pelo valor de *B* / *R* (o *rolo*) e os tempos de envio têm um início inicial a partir de zero. A hora de envio não deve ser posterior à hora da apresentação, pois isso indicaria que a carga inseriu o Bucket muito tarde e não pode ser incluída no objeto de dados. O valor de preroll está incluído no [objeto de cabeçalho ASF](asf-file-structure.md) .

Para o streaming sem problemas na rede, fluxos compactados dentro do conteúdo de mídia devem manter uma taxa de bits constante durante a duração da reprodução. O modelo de Bucket vazado do ASF garante que os dados de mídia sejam enviados pela rede a uma taxa de bits constante. Os parâmetros do Bucket de vazamento são especificados no objeto de propriedades de fluxo estendido do [objeto de cabeçalho ASF](asf-file-structure.md). No Microsoft Media Foundation, eles são definidos como atributos no tipo de mídia que representa o fluxo.

Os valores de Bucket de vazamento são definidos no coletor de arquivos ASF e no objeto multiplexador ASF subjacente e no codificador de mídia do Windows. Esses valores podem ser iguais ou diferentes. Por exemplo, considere um cenário de streaming, que exige que os exemplos de áudio sejam entregues mais tarde do que os exemplos de vídeo para que o arquivo possa ser transmitido sem latência. Para conseguir isso, o Bucket de vazamentos do fluxo de áudio no coletor de mídia pode ser definido como um valor maior do que o valor definido no codificador de áudio do Windows Media.

Para definir valores de B/R no codificador, o aplicativo deve definir as propriedades [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)e [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) . Para obter informações sobre como definir propriedades no codificador, consulte [Propriedades de codificação](configuring-the-encoder.md).

## <a name="the-bucket-in-use"></a>O Bucket em uso

O objetivo de um codificador é garantir que o conteúdo nunca flua o buffer. O codificador usa os valores de taxa de bits e de janela de buffer como guias. O número real de bits transmitidos em qualquer período de tempo igual à janela de buffer nunca pode ser maior do que o dobro do tamanho do buffer.

Considere o exemplo a seguir: você tem um Bucket de 3 litros com um orifício nele por meio do qual um litro pode fluir por minuto. Você coloca o Bucket sob uma bolsa e abre a válvula para deixar a água a uma taxa de 1 litro por minuto. A água flui para fora do Bucket tão rapidamente quanto ele entra, não deixando nenhum extra no Bucket. Em seguida, você aumenta o fluxo da bolsa para 2 galões por minuto. A cada minuto que a água flui nessa taxa, 2 galões entram no Bucket e um vazamento de 1 litro, deixando 1 litro no Bucket. No final de 3 minutos, 6 galões de água ficaram para o Bucket, 3 galões vazaram e o Bucket está cheio.

Na prática, a taxa de dados máxima teórica em um intervalo igual à janela de buffer nunca é obtida. O exemplo anterior assumiu uma taxa de dados constante. Considerando o mesmo Bucket de 3 litros, você poderia aumentar a taxa de fluxo da bolsa para 6 galões por minuto por um minuto e, em seguida, desligar a bolsa por dois minutos. Embora a quantidade total de água colocada no Bucket esteja dentro do máximo teórico da janela de buffer, a concentração dessa quantidade em uma parte da janela faz com que o Bucket ultrapasse o estouro. A 6 galões por minuto, os estouros de buckets de 3 litros logo após 30 segundos são aprovados. Portanto, a quantidade máxima real de dados que podem ser entregues ao buffer durante a duração de qualquer intervalo igual à configuração da janela de buffer depende do tamanho de exemplos individuais e quando eles são entregues.

Até agora, os exemplos só discutiam o buffer usado pelo decodificador, mas um buffer de buckets vazados também é usado pelo codificador que cria o conteúdo compactado. O codificador faz quaisquer ajustes necessários aos algoritmos de compactação para manter a taxa de bits das amostras compactadas dentro dos limites descritos pela janela taxa de bits e buffer, supondo que os exemplos serão entregues ao decodificador a uma taxa constante. Você pode considerar o Bucket do codificador como espelhamento do Bucket do decodificador. O Bucket do codificador é preenchido com uma taxa variável determinada pelo tamanho dos exemplos individuais e vazamentos a uma taxa constante igual à taxa média de bits.

Considere o exemplo a seguir de um codificador e um decodificador conectado em uma rede. Você codifica um arquivo de vídeo em 30 quadros por segundo com uma taxa de bits de 6.000 bits por segundo e uma janela de buffer de 3 segundos (um tamanho total de buffer de 18.000 bits). O primeiro exemplo é codificado como um quadro-chave e ocupa 7.000 bits. O buffer do codificador agora contém 7.000 bits. Os próximos 29 quadros são todos os quadros Delta que totalizam 3.000 bits. Portanto, o primeiro segundo de conteúdo (30 quadros) colocaria a totalidade do buffer em 10.000 bits se nada estivesse vazando. Sabemos que a taxa de bits do fluxo é de 6.000 bits por segundo, portanto, depois que o primeiro segundo de conteúdo codificado é colocado no buffer do codificador, a totalidade cai para 4.000 bits. No aplicativo de decodificação, esse fluxo é entregue ao buffer do decodificador em 6.000 bits por segundo. Depois de um segundo, o buffer contém 6.000 bits. O primeiro exemplo contém 7.000 bits, portanto, o buffer do decodificador deve ser preenchido mais antes que o decodificador comece a remover amostras.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Definindo valores de Bucket vazado para fluxos ASF

Em um cenário de codificação de arquivo, um aplicativo pode definir os valores de Bucket de vazamentos ao configurar os fluxos no [perfil ASF](asf-profile.md).

Depois de criar o fluxo e ter uma referência à interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) do fluxo, você pode definir os valores usando os seguintes atributos:

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (média de valores de Bucket de vazamento)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (máximo de valores de Bucket de vazamento)

Para obter informações sobre como adicionar fluxos e obter o ponteiro **IMFASFStreamConfig** , consulte [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md).

Esses valores contêm o seguinte conjunto de informações:

-   Taxa média de bits: Obtenha a taxa média de bits do tipo de mídia de saída selecionado durante a negociação do tipo de mídia. Use o atributo de [**\_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para fluxos de áudio) ou o atributo de média de taxa de [**\_ \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) (para fluxos de vídeo).
-   Janela de buffer: se você tiver uma instância do codificador e tiver os tipos de mídia de saída negociados, poderá atualizar esse valor posteriormente consultando o codificador para a interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e, em seguida, chamando [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib). Caso contrário, use o valor padrão de 3000 milissegundos.
-   Tamanho do buffer inicial: Defina como 0.

Os valores fornecidos pelo aplicativo dependem do tipo de codificação e do tipo de mídia do fluxo. Por exemplo, a [codificação de taxa de bits constante](constant-bit-rate-encoding.md) requer uma taxa de bits fixa predeterminada e uma janela de buffer. O aplicativo pode especificar esses valores de Bucket de vazamentos definindo a propriedade de codificação [**MFPKEY \_ VIDEOWINDOW**](mfpkey-videowindowproperty.md) e o atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) no fluxo. Os valores de janela de buffer especificados são usados para garantir que o arquivo codificado tenha os horários de envio corretos marcados nos pacotes de dados e que o valor de preversão apareça no objeto de cabeçalho ASF. É suficiente definir **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** porque esses valores especificados são copiados para o atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) .

Para modos de codificação de 2 passagens, você precisa definir ambos os atributos para especificar os valores médio e máximo.

Para a codificação de VBR, o aplicativo pode consultar os valores de Bucket de vazamentos usados pelo codificador somente após a conclusão da passagem de codificação. Portanto, ao configurar o coletor de mídia, o aplicativo pode optar por não definir os atributos ou propriedades relacionados a buckets vazados. Após a codificação, o aplicativo deve consultar o codificador para as propriedades [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)e [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) e defini-las no coletor de mídia para que os valores precisos sejam refletidos no objeto header. Para obter o exemplo de código sobre como atualizar os valores para a codificação de VBR, consulte "atualizar propriedades de codificação no coletor de arquivos", no [tutorial: 1-transmitir codificação de mídia do Windows](tutorial--1-pass-windows-media-encoding.md).

Se você estiver copiando o conteúdo do Windows Media do coletor de origem para mídia sem codificação, os valores de Bucket de vazamento devem ser definidos no coletor de mídia.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Valores de buckets vazados no Multiplexador de ASF

No Media Foundation, os valores de buckets vazados são usados pelo [Multiplexador de ASF](asf-multiplexer.md) para configurar os valores de buckets de vazamentos internos que ele usa para gerar pacotes de dados. A carga está contida em um exemplo de mídia e uma série de amostras de mídia constitui um pacote de dados ASF. Com base nos valores de buckets vazados e no tempo de apresentação, o multiplexador atribui um tempo de envio para cada exemplo de mídia, de modo que as taxas de bits dos pacotes que estão sendo enviados pela rede estejam em uma taxa de bits constante (*R*).

Um aplicativo não pode definir valores de buckets vazados diretamente no Multiplexador. Os valores devem ser fornecidos no coletor de mídia ASF, que define os valores apropriados no Multiplexador. Os valores definidos em [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) e [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) são usados pelo multiplexador para validar que os exemplos enviados ao coletor de mídia ASF são gerados usando os valores especificados.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Atualizando valores de buckets vazados no coletor de mídia ASF

Um aplicativo pode substituir os valores de Bucket de vazamento de nível de fluxo (definidos no perfil ASF durante a criação do fluxo) definindo a propriedade [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigida \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) no repositório de propriedades do coletor de mídia. Para obter uma referência ao repositório de propriedades, use o objeto ContentInfo implementado pelo coletor de mídia. Para obter mais informações, consulte [definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).

**Observação**  Esta operação só é permitida para fluxos de áudio.

Essa propriedade deve ser definida depois que você definir o tipo de saída no codificador. Com base na taxa de bits definida no tipo de mídia, o codificador calcula o tamanho do buffer para garantir que os exemplos de mídia gerados nunca estourem o buffer. O codificador faz os ajustes necessários durante a compactação para manter a taxa de bits das amostras compactadas dentro dos limites descritos pela janela taxa de bits e buffer.

Semelhante aos atributos de configuração de fluxo para buckets vazados, defina a taxa média de bits e o tamanho do buffer e a totalidade do buffer inicial em uma matriz de DWORDs. Para obter mais informações, consulte a seção "definindo valores de Bucket de vazamento para fluxos ASF" neste tópico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 
