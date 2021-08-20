---
description: Media Foundation fornece a fonte de mídia ASF que um aplicativo pode usar para representar um arquivo ASF na camada de pipeline da arquitetura.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: Fonte de mídia do ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3222f32649aa5cb3f4d1d4688a9f7fb7402167e7831377fd8b04d6c879e23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881147"
---
# <a name="asf-media-source"></a>Fonte de mídia do ASF

Media Foundation fornece a fonte de mídia ASF que um aplicativo pode usar para representar um arquivo ASF na camada de pipeline da arquitetura.

Para reproduzir um arquivo ASF, um aplicativo pode usar a fonte de mídia ASF para alimentar dados em um pipeline de reprodução. Em um cenário de codificação, o aplicativo pode usar a fonte de mídia ASF como a origem para converter em outro formato ou para converter um arquivo de taxa de bits mais alta em um arquivo de taxa de bits mais baixa sem alterar formatos. A fonte de mídia ASF deve ser usada na camada de pipeline, ou seja, um aplicativo deve usar a Sessão de Mídia para controlar a operação. Esse nível de acesso permite que os aplicativos recebam eventos enquanto a Sessão de Mídia está em andamento. Para obter acesso de nível inferior ao conteúdo do ASF, um aplicativo deve usar os componentes DOF da Camada WMContainer.

A fonte de mídia ASF implementa a interface [**IMFMediaSource,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que é a interface genérica para fontes de mídia no Media Foundation. Como qualquer outra fonte de mídia, a fonte de mídia do ASF fornece um descritor de apresentação que descreve principalmente o objeto de header ASF. Além disso, a fonte de mídia do ASF fornece descritores de fluxo que representam cada fluxo no conteúdo de mídia. Para obter mais informações, consulte [Estrutura de arquivos ASF](asf-file-structure.md).

-   [Criando a fonte de mídia do ASF](#creating-the-asf-media-source)
-   [Configuração Configurações para a fonte de mídia do ASF](#configuration-settings-for-the-asf-media-source)
-   [Modelo de objeto de origem de mídia ASF](#asf-media-source-object-model)
-   [Serviços de Origem de Mídia do ASF](#asf-media-source-services)
    -   [Conversão de código de tempo](#timecode-translation)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-the-asf-media-source"></a>Criando a fonte de mídia do ASF

Para criar a fonte de mídia ASF, o aplicativo deve usar o [Resolvedor de Origem](source-resolver.md). Para criar a fonte de mídia ASF, o aplicativo deve fornecer a origem para a qual o resolvedor de origem cria a fonte de mídia ASF. As informações de origem devem ser fornecidas especificando a URL do arquivo de origem ou o fluxo de byte que contém a mídia. Se o aplicativo optar por criar a fonte de mídia ASF especificando a URL, ele deverá chamar [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para operação síncrona ou **IMFSourceResolver::Begin... EndCreateObjectFromURL** para operação assíncrona. O processo para criar a fonte de mídia de um fluxo de byte é semelhante. O aplicativo deve chamar [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) para operação síncrona ou **IMFSourceResolver::Begin... EndCreateObjectFromBytestream** para operação assíncrona. Essas chamadas devem especificar MF \_ RESOLUTION \_ MEDIASOURCE no *parâmetro dwFlags.* Para obter mais informações sobre como usar esse sinalizador, consulte Usando o resolvedor de origem.

Se o aplicativo especificar uma URL, para um arquivo local, a cadeia de caracteres de URL poderá conter o caminho do arquivo de mídia ou pode ser prefixada com o "arquivo: "scheme. A extensão de nome de arquivo deve ser ".asf", ".wm", L".wma" ou ".wmv". Para um arquivo ASF na rede, o resolvedor de origem cria a Fonte de Rede [,](network-source-features.md)que usa a fonte de mídia ASF.

Durante o processo de criação do objeto, o resolvedor de origem procura a lista de manipuladores de esquema e os manipuladores de fluxo de byte no registro do sistema e carrega o manipulador correspondente mais próximo que pode analisar o conteúdo de mídia e também criar o objeto de origem de mídia abaixo. Independentemente do método usado para criar a fonte de mídia (URL e fluxo de byte), o resolvedor de origem cria um fluxo de byte e lê o conteúdo da mídia de origem no fluxo de byte. Para obter mais informações, consulte [Manipuladores de esquema e Byte-Stream manipuladores](scheme-handlers-and-byte-stream-handlers.md).

Para ver um exemplo de código sobre como criar uma fonte de mídia, consulte [Usando o Resolvedor de Origem](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Configuração Configurações para a fonte de mídia do ASF

O resolvedor de origem consulta os recursos do fluxo de byte subjacente e determina que as operações são permitidas na fonte de mídia recém-criada. Uma dessas funcionalidades é buscar. Se uma operação de busca for permitida, o aplicativo poderá especificar o modo de busca que a fonte de mídia usa ao buscar um ponto específico na apresentação.

Um aplicativo pode definir o modo de busca, para a fonte de mídia a ser usada, durante a criação do objeto. Depois que a fonte de mídia ASF é criada com o modo de busca especificado, ela não pode ser modificada na fonte de mídia ou alterada dinamicamente durante uma apresentação. As preferências de busca são especificadas como propriedades na chamada do aplicativo para os métodos de resolvedor de origem relevantes usados para criar a fonte de mídia. Esses conjunto de propriedades são definidos em um armazenamento de propriedades e passados para o *parâmetro pProps.* Se essas propriedades não são passadas, a fonte de mídia funciona com as configurações padrão. Para obter mais informações sobre como definir essas propriedades, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

Se a busca for permitida, a fonte de mídia do ASF dá suporte aos seguintes modos de busca:

-   Busca exata: nesse modo, a fonte de mídia do ASF depende do objeto de índice ASF do arquivo ASF. Se o arquivo não tiver o Objeto de Índice, a busca exata será desabilitada e um dos outros modos será usado dependendo das propriedades especificadas pelo aplicativo definidas na fonte de mídia.
-   Busca aproximada: esse modo é solicitado pelo aplicativo passando [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) no armazenamento de propriedades para os métodos de resolvedor de origem relevantes. No entanto, a busca aproximada só será usada se o fluxo de byte não dá suporte à busca baseada em tempo. Nesse modo, a fonte de mídia determina uma hora de início relativamente mais próxima da hora de busca. Se o arquivo ASF contiver um objeto de índice ASF, ele será usado para calcular a hora de início. A busca aproximada é menos precisa, mas mais rápida do que a busca exata porque o tempo de renderização da primeira amostra na hora de início predeterminada é mais rápido.
-   Busca iterativa: para definir esse modo, o aplicativo deve definir a propriedade [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex.](mfpkey-asfmediasource-iterativeseekifnoindex.md) A busca iterativa é um algoritmo para encontrar uma posição em um arquivo ASF que não contém nenhum objeto de índice ASF. Nesse modo, a fonte de mídia determina uma estimativa aproximada do ponto de busca lendo o deslocamento de fluxo de byte. Ele usa uma série de aproximações, com base na taxa média de bits, para se aproximar progressivamente do tempo de busca de destino. (O algoritmo é semelhante a uma pesquisa binária.) A busca iterativa pode levar mais tempo do que a busca usando o Objeto de Índice, portanto, é desabilitada por padrão. Se você definir essa propriedade, use as seguintes propriedades para definir os parâmetros de pesquisa: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance in \_ \_ MilliSecond](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Essas propriedades configuram o número máximo de ierções e a tolerância, respectivamente. O algoritmo é interrompido quando atinge o número máximo de ierções ou quando encontra um pacote cuja distância do tempo de busca está dentro da tolerância especificada.

Em resumo, o aplicativo tem a opção de escolher busca aproximada ou iterativa quando o arquivo ASF não contém um objeto de índice ASF.

## <a name="asf-media-source-object-model"></a>Modelo de objeto de origem de mídia ASF

A fonte de mídia do ASF implementa a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) e expõe as interfaces a seguir. Um aplicativo pode obter uma referência a essas interfaces chamando **IMFMediaSource::QueryInterface** na fonte de mídia do ASF.



| Interface                                                | Descrição                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Necessário para todas as fontes de mídia.                                                                                                                    |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Necessário para todas as fontes de mídia. Permite que os aplicativos recebam eventos da fonte de mídia por meio da Sessão de Mídia.                                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Consulta a fonte de mídia para a interface de serviço especificada.                                                                                      |
| [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Define e obtém propriedades na fonte de mídia. Cada propriedade contém um nome descritivo e um valor.                                               |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Descreve os metadados para o arquivo ASF.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Recupera uma coleção de metadados, para uma apresentação inteira ou para um fluxo na apresentação.                                      |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Consulta o intervalo de taxas de reprodução com suporte, incluindo reprodução inversa.                                                                |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Obtém ou define a taxa de reprodução.                                                                                                                    |
| [**IMFTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Obtém o ITA para cada um dos fluxos ASF contidos na origem.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Permite que uma fonte de mídia receba um ponteiro para a interface [**IMFPMPHost,**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) que é usada para criar objetos no processo PMP. |
| [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Converte entre os códigos de tempo da SMPTE (Society of Motion Picture e engenheiros de tv) e unidades de tempo de 100 nanossegundos.                              |



 

## <a name="asf-media-source-services"></a>Serviços de Origem de Mídia do ASF

A fonte de mídia ASF fornece vários serviços com escopo para o arquivo ASF. Para obter um ponteiro para um serviço específico, o aplicativo deve usar um dos seguintes identificadores de serviço em sua chamada para [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice). Para obter informações, consulte [Interfaces de serviço](service-interfaces.md).



| Identificador de Serviço               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVIÇO DE CONTROLE \_ DE TAXA \_ DE MF \_       | Usando esse identificador, um aplicativo pode obter um ponteiro para interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) ou [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Usando o objeto de suporte de taxa implementado pela fonte de mídia, o aplicativo pode verificar se há suporte para uma taxa específica pelo arquivo de mídia ASF subjacente também obter a taxa mais rápida e mais lenta. Usando o objeto de controle de taxa, o aplicativo pode obter e definir a taxa de reprodução. Se o aplicativo especificar uma taxa específica para reprodução, a fonte de mídia do ASF primeiro verificará se a taxa solicitada está dentro dos limites de taxa (determinados pelas taxas mais rápidas e mais lentas) e definirá a taxa. Isso não verifica as condições de variável, pois a taxa de bits pode mudar a qualquer momento, dependendo da largura de banda da rede. Para obter mais informações, [Controle de taxa](rate-control.md). |
| SERVIÇO DE PROVEDOR \_ DE METADADOS MF \_ \_  | Usando esse identificador, o aplicativo pode obter um ponteiro para a interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) da fonte de mídia do ASF. Essa interface fornece acesso a informações sobre o arquivo ASF especificamente os Objetos de Título do ASF e os fluxos contidos no conteúdo de mídia. As informações de header são expostas por meio de atributos de descritor de apresentação e as informações de fluxo são fornecidas por meio de atributos do descritor de fluxo. Para obter mais informações sobre esses atributos, [consulte Media Foundation atributos para objetos de header ASF](media-foundation-attributes-for-asf-header-objects.md). Além das informações expostas por meio de atributos, também existem metadados descritivos, que são definidos como propriedades.                                                                                                 |
| SERVIÇO MANIPULADOR \_ DE PROPRIEDADES \_ \_ MF   | Usando esse identificador, o aplicativo pode obter um ponteiro para a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) da fonte de mídia do ASF. O armazenamento de propriedades contém todos os metadados relacionados ao arquivo ASF. Esse identificador é novo no Windows 7 e substitui o SERVIÇO DE PROVEDOR DE METADADOS MF \_ para obter propriedades de \_ \_ metadados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SERVIÇO DE ESTATÍSTICAS MFNETSOURCE \_ \_ | Para obter mais informações, consulte Recuperando estatísticas de rede no log [do cliente.](client-logging.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SERVIÇO MF \_ TIMECODE \_            | Usando esse identificador, o aplicativo pode obter um ponteiro para a interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) da fonte de mídia. Essa implementação pode ser usada para executar traduções de código de tempo, como converter o código de tempo SMPTE em unidades de 100 nano segundos e voltar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Conversão de código de tempo

A fonte de mídia ASF fornece um serviço de tradução de código de hora que permite que seu aplicativo converta o código de hora SMPTE para o horário de apresentação mais próximo (na unidade de 100 nanossegundos). Por outro lado, o aplicativo também pode obter o código de hora para uma hora de apresentação solicitada. O serviço está disponível por meio da interface [**IMFTimecodeTranslate,**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) que a fonte de mídia do ASF implementa. As chamadas de método nesse ponteiro de interface são assíncronas que podem ser executados no thread do aplicativo principal sem bloquear a interface do usuário do aplicativo.

As etapas a seguir resumem o procedimento para tradução de código de hora:

1.  Obter ponteiro para a interface [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) da fonte de mídia ASF chamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e especificando o identificador **MF \_ TIMECODE \_ SERVICE.**
2.  Chame [**IMFTimecodeTranslate::BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) ou [**IMFTimecodeTranslate::BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) e especifique a hora que será traduzida.. Para **BeginConvertTimecodeToHNS,** o código de hora deve ser especificado como uma variável [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) com o tipo de **dados VT \_ I8.** O **método BeginConvertHNSToTimecode** requer o tempo em unidades de 100 nanossegundos como o [**tipo MFTIME.**](mftime.md)
3.  Conclua a operação assíncrona chamando [**IMFTimecodeTranslate::EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) ou **IMFTimecodeTranslate::EndConvertTimecodeToHNS** adequadamente.

Durante a criação da fonte de mídia, o resolvedor de origem cria um fluxo de byte para o arquivo do qual a fonte de mídia lê o conteúdo do ASF. Para que as conversões de tempo sejam bem-sucedidas, o fluxo de byte associado ao arquivo ASF deve ter funcionalidades de busca; caso contrário, o aplicativo obtém o erro MF \_ E \_ BYTESTREAM \_ NOT \_ SEEKABLE da chamada **Begin....** Outro requisito para conversões de tempo é que o arquivo ASF, representado pela fonte de mídia ASF, deve ter objetos de índice ASF. Os tempos de apresentação e os códigos de tempo são extraídos dos Objetos de Índice ASF que mantêm todos os índices e os pontos de busca correspondentes para o arquivo ASF. Para tradução de código de tempo de apresentação, o arquivo ASF deve conter um Objeto de Índice Simples; para a conversão de tempo de código para apresentação, o arquivo ASF deve ter um Objeto de Índice. As operações de conversão dependem do *indexador* subjacente (componente WMContainer) para analisar e ler o Objeto de Índice associado ao arquivo ASF. Se o arquivo não contém um Objeto de Índice, o aplicativo recebe de forma assíncrona o código de erro MF \_ E \_ NO \_ INDEX.

Para converter o tempo solicitado pelo aplicativo, a fonte de mídia enumera os fluxos dentro do arquivo e localiza o fluxo que contém o objeto de índice ASF apropriado. Se esse fluxo for encontrado, a fonte de mídia analisará os pacotes ASF do fluxo serão analisados até que o código de hora correto seja atingido. Depois de encontrar o exemplo correto, ele recupera a hora de apresentação correspondente ou o código de hora do exemplo e o retorna para o chamador.

### <a name="script-command-support"></a>Suporte a comandos de script

Quando você cria uma topologia ASF que contém um fluxo de script, um nó Fluxo de Script é adicionado à topologia. Esse nó enviará IMFSamples no momento apropriado. O IMFSample fornecido pelo nó de origem do script armazena os dados no IMFMediaBuffer associado ao exemplo. Você pode chamar CopyToBuffer no exemplo para obter um IMFMediaBuffer e, em seguida, chamar Bloquear no buffer para obter os dados. 

Os conteúdos de fluxo de script são empacotados no buffer como uma cadeia de caracteres de tipo, seguidos por NULL, seguidos pela cadeia de caracteres de comando, seguida por NULL. As cadeias de caracteres são Unicode no formato ASF.

Por exemplo, um payload pode ser parecido com o seguinte (em que \0 indica um caractere NULL):

*URL\0http://contoso.com\0*

*Text\0This is a caption\0*



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF em Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
