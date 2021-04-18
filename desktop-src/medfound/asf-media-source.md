---
description: Media Foundation fornece a fonte de mídia ASF que um aplicativo pode usar para representar um arquivo ASF na camada de pipeline da arquitetura.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Fonte de mídia ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75dc682d48339ce4ff707e7859a6962b9f5cfd92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782595"
---
# <a name="asf-media-source"></a>Fonte de mídia ASF

Media Foundation fornece a fonte de mídia ASF que um aplicativo pode usar para representar um arquivo ASF na camada de pipeline da arquitetura.

Para reproduzir um arquivo ASF, um aplicativo pode usar a fonte de mídia do ASF para alimentar dados em um pipeline de reprodução. Em um cenário de codificação, o aplicativo pode usar a fonte de mídia do ASF como a origem para converter em outro formato ou para converter um arquivo de taxa de bits maior em um arquivo de taxa de bits inferior sem alterar os formatos. A fonte de mídia do ASF deve ser usada na camada do pipeline, ou seja, um aplicativo deve usar a sessão de mídia para controlar a operação. Esse nível de acesso permite que os aplicativos obtenham eventos enquanto a sessão de mídia está em andamento. Para obter acesso de nível inferior ao conteúdo do ASF, um aplicativo deve usar os componentes ASF da camada WMContainer.

A origem de mídia do ASF implementa a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , que é a interface genérica para fontes de mídia no Media Foundation. Como qualquer outra fonte de mídia, a fonte de mídia ASF fornece um descritor de apresentação que descreve principalmente o objeto de cabeçalho ASF. Além disso, a fonte de mídia do ASF fornece descritores de fluxo que representam cada fluxo no conteúdo de mídia. Para obter mais informações, consulte [estrutura de arquivo ASF](asf-file-structure.md).

-   [Criando a fonte de mídia ASF](#creating-the-asf-media-source)
-   [Definições de configuração para a origem de mídia ASF](#configuration-settings-for-the-asf-media-source)
-   [Modelo de objeto de origem de mídia ASF](#asf-media-source-object-model)
-   [Serviços de origem de mídia ASF](#asf-media-source-services)
    -   [Conversão de código de](#timecode-translation)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-the-asf-media-source"></a>Criando a fonte de mídia ASF

Para criar a fonte de mídia do ASF, o aplicativo deve usar o [resolvedor de origem](source-resolver.md). Para criar a origem de mídia ASF, o aplicativo deve fornecer a origem para a qual o resolvedor de origem cria a origem de mídia do ASF. As informações de origem devem ser fornecidas por meio da especificação da URL do arquivo de origem ou do fluxo de bytes que contém a mídia. Se o aplicativo optar por criar a origem de mídia do ASF especificando a URL, ele deverá chamar [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para a operação síncrona ou **IMFSourceResolver:: Begin... EndCreateObjectFromURL** para operação assíncrona. O processo para criar a origem de mídia de um fluxo de bytes é semelhante. O aplicativo deve chamar [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) para a operação síncrona ou **IMFSourceResolver:: Begin... EndCreateObjectFromBytestream** para operação assíncrona. Essas chamadas devem especificar a \_ \_ mídia de resolução MF no parâmetro *dwFlags* . Para obter mais informações sobre como usar esse sinalizador, consulte usando o resolvedor de origem.

Se o aplicativo especificar uma URL, para um arquivo local, a cadeia de caracteres da URL poderá conter o caminho do arquivo de mídia ou poderá ser prefixada com o esquema "file:". A extensão de nome de arquivo deve ser ". ASF", ". WM", L ". WMA" ou ". wmv". Para um arquivo ASF na rede, o resolvedor de origem cria a [origem da rede](network-source-features.md), que usa a fonte de mídia do ASF.

Durante o processo de criação de objeto, o resolvedor de origem pesquisa a lista de manipuladores de esquema e os manipuladores de fluxo de bytes no registro do sistema e carrega o manipulador de correspondência mais próximo que pode analisar o conteúdo de mídia e também criar o objeto de origem de mídia abaixo. Independentemente do método usado para criar a origem da mídia (URL e fluxo de bytes), o resolvedor de origem cria um fluxo de bytes e lê o conteúdo da mídia de origem no fluxo de bytes. Para obter mais informações, consulte [manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Para obter um exemplo de código sobre como criar uma fonte de mídia, consulte [usando o resolvedor de origem](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Definições de configuração para a origem de mídia ASF

O resolvedor de origem consulta os recursos do fluxo de bytes subjacente e determina que as operações são permitidas na fonte de mídia recém-criada. Um desses recursos está procurando. Se uma operação de busca for permitida, o aplicativo poderá especificar o modo de busca que a fonte de mídia usa ao procurar um ponto específico na apresentação.

Um aplicativo pode definir o modo de busca para a origem de mídia a ser usada, durante a criação do objeto. Depois que a fonte de mídia do ASF é criada com o modo de busca especificado, ela não pode ser modificada na origem da mídia ou alterada dinamicamente durante uma apresentação. As preferências de busca são especificadas como propriedades na chamada do aplicativo para os métodos do resolvedor de origem relevantes que são usados para criar a origem da mídia. Esses conjuntos de propriedades são definidos em um repositório de propriedades e passados para o parâmetro *pProps* . Se essas propriedades não forem passadas, a origem da mídia funcionará com as configurações padrão. Para obter mais informações sobre como definir essas propriedades, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Se a busca for permitida, a origem da mídia ASF dará suporte aos seguintes modos de busca:

-   Busca exata: nesse modo, a fonte de mídia ASF depende do objeto de índice ASF do arquivo ASF. Se o arquivo não tiver o objeto index, a busca exata será desabilitada e um dos outros modos será usado dependendo das propriedades especificadas pelo aplicativo que são definidas na origem da mídia.
-   Busca aproximada: esse modo é solicitado pelo aplicativo passando [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) no repositório de propriedades para os métodos relevantes do resolvedor de origem. No entanto, a busca aproximada só será usada se o fluxo de bytes não oferecer suporte à busca baseada em tempo. Nesse modo, a origem da mídia determina uma hora de início relativamente mais próxima ao tempo de busca. Se o arquivo ASF contiver um objeto de índice ASF, ele será usado para calcular a hora de início. A busca aproximada é menos precisa, mas mais rápida que a busca exata, pois o tempo gasto processa o primeiro exemplo na hora de início predeterminada é mais rápido.
-   Busca iterativa: para definir esse modo, o aplicativo deve definir a propriedade [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) . A busca iterativa é um algoritmo para encontrar uma posição em um arquivo ASF que não contém nenhum objeto de índice ASF. Nesse modo, a origem da mídia determina uma estimativa aproximada do ponto de busca, lendo o deslocamento do fluxo de bytes. Ele usa uma série de aproximações, com base na taxa média de bits, para ficar progressivamente mais próximo do tempo de busca de destino. (O algoritmo é semelhante a uma pesquisa binária.) A busca iterativa pode levar mais tempo do que a busca por meio do objeto index, portanto, ela está desabilitada por padrão. Se você definir essa propriedade, use as seguintes propriedades para definir os parâmetros de pesquisa: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerante \_ em \_ milissegundo](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Essas propriedades definem o número máximo de iterações e a tolerância, respectivamente. O algoritmo é interrompido quando atinge o número máximo de iterações ou quando encontra um pacote cuja distância do tempo de busca está dentro da tolerância especificada.

Resumindo, o aplicativo tem a opção de escolher a busca aproximada ou iterativa quando o arquivo ASF não contém um objeto de índice ASF.

## <a name="asf-media-source-object-model"></a>Modelo de objeto de origem de mídia ASF

A origem de mídia do ASF implementa a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) e expõe as interfaces a seguir. Um aplicativo pode obter uma referência a essas interfaces chamando **IMFMediaSource:: QueryInterface** na fonte de mídia do ASF.



| Interface                                                | Descrição                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Necessário para todas as fontes de mídia.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Necessário para todas as fontes de mídia. Permite que os aplicativos obtenham eventos da origem da mídia por meio da sessão de mídia.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Consulta a origem da mídia para a interface de serviço especificada.                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Define e obtém as propriedades na origem da mídia. Cada propriedade contém um nome descritivo e um valor.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Descreve os metadados para o arquivo ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Recupera uma coleção de metadados, seja para uma apresentação inteira ou para um fluxo na apresentação.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Consulta o intervalo de taxas de reprodução com suporte, incluindo reprodução reversa.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Obtém ou define a taxa de reprodução.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Obtém o ITA para cada um dos fluxos de ASF contidos na origem.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Permite que uma fonte de mídia receba um ponteiro para a interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , que é usada para criar objetos no processo do PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Converte entre os códigos de tempo da sociedade de imagem de movimento e dos engenheiros de televisão (SMPTE) e as unidades de hora de 100-nanossegundos.                              |



 

## <a name="asf-media-source-services"></a>Serviços de origem de mídia ASF

A fonte de mídia do ASF fornece vários serviços com escopo para o arquivo ASF. Para obter um ponteiro para um serviço específico, o aplicativo deve usar um dos seguintes identificadores de serviço em sua chamada para [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Para obter informações, consulte [interfaces de serviço](service-interfaces.md).



| Identificador de serviço               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_serviço de \_ controle de taxa MF \_       | Usando esse identificador, um aplicativo pode obter um ponteiro para as interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) ou [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . Usando o objeto de suporte de taxa implementado pela origem de mídia, o aplicativo pode verificar se uma taxa específica tem suporte pelo arquivo de mídia ASF subjacente também obtém a taxa mais rápida e mais lenta. Usando o objeto de controle de taxa, o aplicativo pode obter e definir a taxa de reprodução. Se o aplicativo especificar uma taxa específica para reprodução, a origem de mídia ASF primeiro verificará se a taxa solicitada está dentro dos limites de taxa (determinado pelas tarifas mais lentas e mais baixas) e, em seguida, definirá a taxa. Isso não verifica as condições variáveis, pois a taxa de bits pode mudar a qualquer momento, dependendo da largura de banda da rede. Para obter mais informações, [controle de taxa](rate-control.md). |
| \_serviço do \_ provedor de metadados MF \_  | Usando esse identificador, o aplicativo pode obter um ponteiro para a interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) da fonte de mídia do ASF. Essa interface fornece acesso a informações sobre o arquivo ASF especificamente os objetos de cabeçalho ASF e os fluxos contidos no conteúdo de mídia. As informações de cabeçalho são expostas por meio de atributos de descritor de apresentação e as informações de fluxo são fornecidas por meio de atributos Para obter mais informações sobre esses atributos, consulte [atributos de Media Foundation para objetos de cabeçalho ASF](media-foundation-attributes-for-asf-header-objects.md). Além das informações expostas por meio de atributos, também existem metadados descritivos, que são definidos como propriedades.                                                                                                 |
| \_serviço de \_ manipulador de propriedades MF \_   | Usando esse identificador, o aplicativo pode obter um ponteiro para a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) da fonte de mídia do ASF. O armazenamento de propriedades contém todos os metadados relacionados ao arquivo ASF. Esse identificador é novo no Windows 7 e substitui o \_ \_ \_ serviço de provedor de metadados MF para obter propriedades de metadados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_serviço de estatísticas do MFNETSOURCE \_ | Para obter mais informações, consulte Recuperando estatísticas de rede no [log do cliente](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_serviço de código de caso MF \_            | Usando esse identificador, o aplicativo pode obter um ponteiro para a interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) da fonte de mídia. Essa implementação pode ser usada para executar traduções de código de tempo, como converter o código de tempo SMPTE para unidades de 100 e Nanos Second e voltar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Conversão de código de

A fonte de mídia do ASF fornece um serviço de conversão de código de tempo que permite que seu aplicativo converta o código de tempo SMPTE para o tempo de apresentação mais próximo (na unidade de 100 a nanossegundos). Por outro lado, o aplicativo também pode obter o código de tempo para um tempo de apresentação solicitado. O serviço está disponível por meio da interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) , que a origem de mídia do ASF implementa. As chamadas de método nesse ponteiro de interface são assíncronas que podem ser executadas de seu thread de aplicativo principal sem bloquear a interface do usuário do seu aplicativo.

As etapas a seguir resumem o procedimento para conversão de código de tempo:

1.  Obtenha o ponteiro para a interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) da fonte de mídia do ASF chamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e especificando o identificador do **\_ \_ serviço de código** de execução MF.
2.  Chame [**IMFTimecodeTranslate:: BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) ou [**IMFTimecodeTranslate:: BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) e especifique o tempo que deve ser traduzido. Para **BeginConvertTimecodeToHNS** , o código de tempo deve ser especificado como uma variável [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) com o tipo de dados **VT \_ i8** . O método **BeginConvertHNSToTimecode** requer o tempo em unidades de 100 nanossegundos como o tipo [**MFTIME**](mftime.md) .
3.  Conclua a operação assíncrona chamando [**IMFTimecodeTranslate:: EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) ou **IMFTimecodeTranslate:: EndConvertTimecodeToHNS** adequadamente.

Durante a criação da origem de mídia, o resolvedor de origem cria um fluxo de bytes para o arquivo do qual a origem da mídia lê o conteúdo do ASF. Para que as conversões de tempo sejam bem-sucedidas, o fluxo de bytes associado ao arquivo ASF deve ter recursos de busca; caso contrário, o aplicativo obterá \_ o \_ erro MF E bytes \_ não \_ pesquisável da chamada **begin...** . Outro requisito de conversões de tempo é que o arquivo ASF, representado pela fonte de mídia do ASF, deve ter objetos de índice ASF. Os tempos de apresentação e os códigos de tempo são extraídos dos objetos de índice ASF que mantêm todos os índices e os pontos de busca correspondentes para o arquivo ASF. Para a conversão de código em tempo de apresentação, o arquivo ASF deve conter um objeto de índice simples; para a conversão de tempo de código para a apresentação, o arquivo ASF deve ter um objeto index. As operações de conversão dependem do *indexador* subjacente (componente WMContainer) para analisar e ler o objeto de índice associado ao arquivo asf. Se o arquivo não contiver um objeto de índice, o aplicativo receberá de forma assíncrona o \_ código de erro MF E \_ no \_ index.

Para converter o tempo solicitado pelo aplicativo, a origem da mídia enumera os fluxos dentro do arquivo e localiza o fluxo que contém o objeto de índice ASF apropriado. Se esse fluxo for encontrado, a fonte de mídia analisa os pacotes ASF do fluxo são analisados até que o código de tempo correto seja atingido. Depois de encontrar o exemplo correto, ele recupera o tempo de apresentação correspondente ou o código de tempo do exemplo e o retorna ao chamador.

### <a name="script-command-support"></a>Suporte a comandos de script

Quando você cria uma topologia de ASF que contém um fluxo de script, um nó de fluxo de script é adicionado à topologia. Esse nó enviará IMFSamples no momento apropriado. O IMFSample fornecido pelo nó de origem do script armazena os dados no IMFMediaBuffer associado ao exemplo. Você pode chamar CopyToBuffer no exemplo para obter um IMFMediaBuffer e, em seguida, chamar o bloqueio no buffer para obter os dados. 

Cargas de fluxo de script são empacotadas no buffer como uma cadeia de caracteres de tipo, seguido por NULL, seguidos pela cadeia de caracteres de comando, seguido por NULL. As cadeias de caracteres são Unicode no formato ASF.

Por exemplo, uma carga pode ser parecida com a seguinte (onde \ 0 indica um caractere nulo):

*URL\0http://contoso.com\0*

*Text\0This é um caption\0*



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
