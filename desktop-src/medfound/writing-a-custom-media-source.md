---
description: Este tópico descreve como implementar uma fonte de mídia personalizada no Microsoft Media Foundation.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Gravando uma fonte de mídia personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8769fa16d4dcbfd3438b66f9a9e78c34274735a5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105762343"
---
# <a name="writing-a-custom-media-source"></a>Gravando uma fonte de mídia personalizada

Este tópico descreve como implementar uma fonte de mídia personalizada no Microsoft Media Foundation. Ele contém as seções a seguir:

-   [Criando o descritor de apresentação](#creating-the-presentation-descriptor)
-   [Iniciando a origem da mídia](#starting-the-media-source)
    -   [Atingir](#seeking)
-   [Pausando a origem da mídia](#pausing-the-media-source)
-   [Gerando dados de origem](#generating-source-data)
    -   [Solicitações de amostra](#sample-requests)
    -   [Alocando amostras](#allocating-samples)
    -   [Lacunas no fluxo](#gaps-in-the-stream)
-   [Desligando a origem da mídia](#shutting-down-the-media-source)
-   [Fontes dinâmicas](#live-sources)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Criando o descritor de apresentação

O método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) retorna uma cópia do descritor de apresentação da origem. Para criar o descritor de apresentação, você deve saber o número de fluxos no conteúdo de origem e os formatos possíveis de cada fluxo. Para cada fluxo, crie um descritor de fluxo da seguinte maneira:

1.  Crie uma matriz de tipos de mídia. Cada tipo de mídia na matriz representa um formato possível para o fluxo. Para obter mais informações sobre como criar tipos de mídia, consulte [tipos de mídia](media-types.md).
2.  Chame [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) para criar o descritor de fluxo. Passe a matriz de tipos de mídia. A função retorna um ponteiro [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .
3.  Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obter o manipulador de tipo de mídia do descritor de fluxo.
4.  Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para definir o formato de fluxo padrão. Use um dos tipos de mídia que você criou na etapa 1. Em geral, você deve usar o formato com a qualidade mais alta.
5.  Opcionalmente, defina atributos no descritor de fluxo. Para obter uma lista de atributos que se aplicam aos descritores de fluxo, consulte [atributos de descritor de fluxo](stream-descriptor-attributes.md).

Agora, crie o descritor de apresentação:

1.  Chame [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) e transmita a matriz de descritores de fluxo. A função retorna um ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .
2.  Escolha a seleção de fluxo padrão chamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) para selecionar um ou mais fluxos. Pelo menos um fluxo deve ser selecionado na configuração padrão.
3.  Opcionalmente, defina atributos no descritor de apresentação. Para obter uma lista dos atributos que se aplicam aos descritores de fluxo, consulte [atributos do descritor de apresentação](presentation-descriptor-attributes.md).

Você deve criar o descritor de apresentação uma vez, na inicialização ou depois que a origem tiver analisado o suficiente dos dados de origem para determinar o conteúdo. O método [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) deve retornar uma cópia do descritor de apresentação. Para criar a cópia, chame [**IMFPresentationDescriptor:: clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). Retornar uma cópia impede que o cliente modifique o estado do descritor de apresentação original, como os atributos ou a seleção de fluxo. No entanto, lembre-se de que o **clone** cria uma cópia superficial, de modo que o cliente pode potencialmente modificar os descritores de fluxo subjacentes.

## <a name="starting-the-media-source"></a>Iniciando a origem da mídia

O método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia a origem da mídia ou busca uma nova posição. Uma chamada para **Start** faz com que uma *busca* quando o estado anterior fosse pausado ou em execução e uma nova hora de início seja especificada. Caso contrário, o método **Start** causará um *início*. Quando a operação de **inicialização** for concluída, envie os eventos a seguir.

1.  Envie um evento [MENewStream](menewstream.md) para cada novo fluxo — ou seja, cada fluxo que foi previamente desmarcado e agora está selecionado. Os dados do evento são um ponteiro para o fluxo.
2.  Envie um evento [MEUpdatedStream](meupdatedstream.md) para cada fluxo que foi selecionado anteriormente e ainda está selecionado. Os dados do evento são um ponteiro para o fluxo. (Não envie um evento para fluxos desmarcados.)
3.  Se a origem estiver procurando, envie um evento [MESourceSeeked](mesourceseeked.md) . Caso contrário, envie um evento [MESourceStarted](mesourcestarted.md) . Os dados do evento são a hora de início que foi especificada no método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) . Para o evento MESourceStarted, se a hora de início for VT \_ Empty, defina o atributo de [**\_ \_ \_ \_ início real da origem do evento MF**](mf-event-source-actual-start-attribute.md) no evento. O valor do atributo é a hora de início real.
4.  Para cada fluxo, se a origem estiver procurando, envie um evento [MEStreamSeeked](mestreamseeked.md) . Caso contrário, envie um evento [MEStreamStarted](mestreamstarted.md) . Os dados do evento são a hora de início. (A origem da mídia pode enfileirar um evento no fluxo chamando o método [**IMFMediaEventGenerator:: QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) do fluxo.)

Quando um fluxo é desmarcado, desligue o fluxo. O fluxo não deve enfileirar nenhum outro evento nesse ponto.

O formato de hora para o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é fornecido no parâmetro *pguidTimeFormat* . O formato de hora padrão, indicado por **GUID \_ NULL**, é unidades de 100 nanossegundos. Uma origem de mídia deve dar suporte a esse formato de hora.

### <a name="seeking"></a>Atingir

Ao procurar, a posição inicial solicitada pode não estar em um limite de amostra exato. Além disso, para conteúdo compactado, a posição inicial pode ficar entre os quadros-chave. Um fluxo deve fornecer exemplos do ponto mais antigo necessário para produzir uma amostra não compactada na posição inicial solicitada. Para vídeo, isso significa iniciar a partir do quadro de chave anterior. O pipeline é responsável por remover os quadros extras do decodificador, para que a reprodução comece no horário solicitado.

A hora de início fornecida nos eventos de origem ([MESourceStarted](mesourcestarted.md), [MESourceSeeked](mesourceseeked.md), [MEStreamStarted](mestreamstarted.md)e [MEStreamSeeked](mestreamseeked.md)) é a hora de início solicitada (o valor fornecido no método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) ), independentemente da posição inicial real.

Por exemplo, suponha que os primeiros quadros de um fluxo de vídeo tenham as seguintes características:



| Amostra     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Hora       | 33 MS | 66 MS | 100 ms | 133 MS |
| Quadro-chave? | Sim     | Não      | Não       | Sim      |



 

Se o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) for chamado com um valor de 100 milissegundos, a origem precisará gerar um vídeo a partir do quadro 1, o primeiro quadro-chave antes dessa hora. O evento iniciar ainda indicará 100 milissegundos nos dados do evento.

## <a name="pausing-the-media-source"></a>Pausando a origem da mídia

O método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) faz uma pausa na origem da mídia.

Enquanto a origem é pausada, um fluxo pode criar novos exemplos e armazená-los em uma fila, mas o fluxo não fornece os exemplos. Aqui estão algumas exceções a essa regra:

-   As fontes dinâmicas devem descartar os dados enquanto estiverem em pausa.
-   Se a origem obtém dados de uma rede, ele pode pausar o servidor.

Se o cliente chamar [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) enquanto a origem estiver pausada, a solicitação também será enfileirada até que a origem seja iniciada novamente. As solicitações não devem ser descartadas.

A pausa só é permitida a partir do estado iniciado. Caso contrário, [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) deve retornar **MF \_ E \_ \_ \_ transição de estado inválida**.

## <a name="generating-source-data"></a>Gerando dados de origem

Media Foundation usa um *modelo de pull*, o que significa que os fluxos geram e entregam amostras em resposta a solicitações do pipeline. Um fluxo pode fornecer exemplos quando a origem da mídia está em execução e o fluxo é selecionado. Um fluxo só fornece dados quando o cliente solicita um novo exemplo.

### <a name="sample-requests"></a>Solicitações de Amostra

O cliente solicita um novo exemplo chamando [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Aqui está a sequência de operações:

1.  O cliente chama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). O argumento é um ponteiro para um objeto de *token* opcional que o cliente usa para rastrear a solicitação. O cliente implementa o token. Os tokens devem expor a interface **IUnknown** . O cliente também pode passar um ponteiro nulo em vez de um token.
2.  Se o cliente forneceu um token, o fluxo de mídia chama **AddRef** no token e coloca o token em uma fila primeiro a entrar, primeiro a sair. O método retorna, e as etapas restantes ocorrem de forma assíncrona.

3.  Quando mais dados estiverem disponíveis, o fluxo de mídia criará um novo exemplo. (Essa etapa é descrita mais detalhadamente na próxima seção.)
4.  O fluxo de mídia efetua pull do primeiro token da fila.
5.  Se o token não for **nulo**, o fluxo de mídia definirá o atributo de [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) no exemplo de mídia. O valor do atributo é um ponteiro para o token.
6.  O fluxo de mídia envia um evento [MEMediaSample](memediasample.md) . Os dados do evento são um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) do exemplo.
7.  Se o cliente forneceu um token, o fluxo de mídia chama a **versão** no objeto de token.

Se o fluxo de mídia não puder atender à solicitação de [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) do cliente, ele extrairá o token da fila e chamará a **versão** no token, mas não enviará um evento [MEMediaSample](memediasample.md) .

O cliente pode usar o token para acompanhar o status da solicitação. Quando o cliente recebe o evento [MEMediaSample](memediasample.md) , ele pode obter o token do exemplo e fazer a correspondência com a solicitação original. O cliente também pode usar o token para detectar se a origem da mídia descartou a solicitação. Se a contagem de referência do token cair em zero e o fluxo de mídia não enviar um evento MEMediaSample, isso significa que a solicitação foi cancelada.

As etapas listadas aqui pressupõem que o método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) seja implementado como uma operação assíncrona. Se o método for síncrono, você não precisará colocar o token de solicitação em uma fila. No entanto, se a geração de dados levar qualquer quantidade significativa de tempo, uma abordagem assíncrona será recomendada, por exemplo, se a origem ler dados de um fluxo de bytes.

O fluxo é responsável por armazenar em buffer todos os dados que são acumulados entre chamadas para [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).

Quando o fluxo de mídia atingir o final do fluxo, ele enviará um evento [MEEndOfStream](meendofstream.md) após o último exemplo. Após a finalização de cada fluxo, a origem da mídia envia um evento [MEEndOfPresentation](meendofpresentation.md) . Depois que um fluxo de mídia envia o evento MEEndOfStream, o método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) retorna **MF \_ E \_ end \_ of \_ Stream** até que a origem seja reiniciada.

### <a name="allocating-samples"></a>Alocando amostras

Quando o fluxo está pronto para preencher uma solicitação de exemplo pendente, ele cria um novo exemplo e adiciona um ou mais buffers de mídia ao exemplo. Para obter mais informações sobre como criar buffers de mídia, consulte [buffers de mídia](media-buffers.md).

O fluxo deve definir o carimbo de data/hora e a duração, se conhecido. O carimbo de data/hora é relativo à origem. Na maioria dos casos, o início do conteúdo corresponde a um carimbo de data/hora igual a zero. Por exemplo, se a origem lê de um arquivo de mídia, o início do arquivo teria um carimbo de data/hora igual a zero.

O carimbo de data/hora no exemplo não é necessariamente igual ao tempo de apresentação. A sessão de mídia é traduzida do tempo de origem para o tempo de apresentação. Para dados compactados, o fluxo deve gerar dados a partir do quadro de chave mais próximo antes da hora de início. Isso permite que o decodificador entregue o quadro que aparece na hora de início solicitada. (Caso contrário, o decodificador precisaria aguardar até o quadro-chave a seguir.)

Se a taxa de reprodução for mais rápida ou mais lenta que 1,0, o pipeline ajustará a taxa do relógio de apresentação. A origem não ajusta os carimbos de data/hora em exemplos.

A fonte pode definir informações adicionais sobre o exemplo definindo atributos. Para obter uma lista de atributos de exemplo, consulte [atributos de exemplo](sample-attributes.md).

### <a name="gaps-in-the-stream"></a>Lacunas no fluxo

Se um fluxo contiver um intervalo de comprimento significativo, é recomendável que o fluxo envie um evento [MEStreamTick](mestreamtick.md) . Esse evento notifica o cliente de que um exemplo está ausente. Os dados do evento são o carimbo de data/hora do exemplo ausente, em unidades de 100 a nanossegundos (**VT \_ i8**). Esse evento pode salvar componentes downstream de esperar por exemplos que não serão recebidos. O fluxo pode enviar quantos eventos MEStreamTick forem necessários para abranger a lacuna no fluxo.

## <a name="shutting-down-the-media-source"></a>Desligando a origem da mídia

Quando o cliente é concluído usando a origem de mídia, ele chama [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). Dentro desse método, a origem da mídia deve interromper quaisquer contagens de referência circulares. Normalmente, haverá referências circulares entre a origem da mídia e os fluxos de mídia.

Se você estiver usando a fila de eventos para implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), chame [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) na fila de eventos. Esse método desliga a fila de eventos e sinaliza qualquer chamador que esteja aguardando um evento no momento.

Após o desligamento, todos os métodos na origem retornam **MF \_ E \_ Shutdown**, com exceção dos métodos **IUnknown** .

## <a name="live-sources"></a>Fontes dinâmicas

A partir do Windows 7, o Media Foundation oferece suporte automático a dispositivos de captura de áudio e vídeo. Para vídeo, o dispositivo deve fornecer um minidriver de streaming de kernel (KS) na categoria de captura de vídeo. Media Foundation usa o caminho PnP para enumerar o dispositivo. Para áudio, Media Foundation usa a API do dispositivo de multimídia do Windows (MMDevice) para enumerar dispositivos de ponto de extremidade de áudio. Se o dispositivo atender a esses critérios, não será necessário implementar uma fonte de mídia personalizada.

No entanto, talvez você queira implementar uma fonte de mídia personalizada para algum outro tipo de dispositivo ou outra fonte de dados ao vivo. Há apenas algumas diferenças entre uma fonte dinâmica e outras fontes de mídia:

-   No método [**IMFMediaSource:: getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) , retorne o **MFMEDIASOURCE \_ é \_** o sinalizador Live.
-   O primeiro exemplo deve ter um carimbo de data/hora igual a zero.
-   Os eventos e os Estados de streaming são tratados da mesma forma que as fontes de mídia, com exceção do estado em pausa.
-   Enquanto estiver em pausa, não coloque amostras na fila. Descarte todos os dados gerados enquanto estiverem em pausa.
-   As fontes dinâmicas normalmente não dão suporte a busca, reprodução reversa ou controle de taxa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Tutorial: escrevendo uma fonte de mídia personalizada](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



