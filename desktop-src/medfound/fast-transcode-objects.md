---
description: Este tópico descreveu como usar a API de transcodificação para codificar um arquivo de mídia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Usando a API de transcodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089740"
---
# <a name="using-the-transcode-api"></a>Usando a API de transcodificação

Este tópico descreveu como usar a API de transcodificação para codificar um arquivo de mídia.

-   [Visão geral](#overview)
-   [Criando uma origem de mídia](#creating-a-media-source)
-   [Criando um perfil transcodificar](#creating-a-transcode-profile)
    -   [Atributos de áudio](#audio-attributes)
    -   [Atributos de vídeo](#video-attributes)
    -   [Atributos de contêiner](#container-attributes)
-   [Criando uma topologia de transcodificação](#creating-a-transcode-topology)
-   [Executando a sessão de codificação](#running-the-encoding-session)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Antes de usar a API de transcodificação, o aplicativo deve ter as seguintes informações:

-   O caminho ou a URL para um arquivo de mídia existente que será codificado novamente.
-   O nome do arquivo de saída.
-   O tipo de contêiner para o arquivo de saída, como MP4 ou ASF (Advanced Streaming Format).
-   O formato de codificação. Essas informações incluem os tipos de mídia que descrevem os fluxos de áudio e vídeo codificados.

Para usar a API de transcodificação, um aplicativo executa as etapas a seguir.

1.  Crie uma origem de mídia para ler o arquivo de origem.
2.  Criar um perfil transcodificar. Adicione atributos que descrevem o fluxo de áudio, o fluxo de vídeo e o contêiner de arquivos.
3.  Use o perfil transcodificar para criar uma topologia de codificação. (Para obter mais informações sobre topologias, consulte [about topologias](about-topologies.md).)
4.  Defina a topologia na [sessão de mídia](media-session.md).
5.  Inicie a sessão de mídia e aguarde o evento [MESessionEnded](mesessionended.md) .

O restante deste tópico descreve essas etapas mais detalhadamente.

## <a name="creating-a-media-source"></a>Criando uma origem de mídia

Uma origem de mídia é um objeto que lê e analisa o arquivo de origem. Para criar uma fonte de mídia, use o [resolvedor de origem](source-resolver.md). Você pode encontrar um código de exemplo no tópico [usando o resolvedor de origem](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Criando um perfil transcodificar

Um *perfil transcodificar* descreve o formato e as configurações que são usadas para codificar o arquivo de saída. O perfil transcodificar contém três conjuntos de atributos:

-   Atributos de áudio: Descreva as configurações de formato de áudio de destino e codificador de áudio.
-   Atributos de vídeo: Descreva as configurações de formato de vídeo de destino e codificador de vídeo.
-   Atributos de contêiner: defina o tipo de contêiner de arquivo, bem como algumas configurações de codificação globais.

Para criar um perfil de transcodificação, chame a função [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) . Essa função retorna um ponteiro para a interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) . O objeto de perfil inicial está vazio; Ele não contém nenhum atributo. A próxima etapa é adicionar os atributos que definem o perfil.

### <a name="audio-attributes"></a>Atributos de áudio

Para adicionar atributos para o fluxo de áudio, chame [**IMFTranscodeProfile:: Setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Esses atributos especificam como o fluxo de áudio é codificado. Se o arquivo de saída não contiver um fluxo de áudio, omita esses atributos.

Os atributos de áudio se enquadram em duas categorias:

-   Atributos que especificam o formato do fluxo codificado
-   Atributos que especificam outros parâmetros de codificação.

Os atributos de formato são simplesmente atributos de tipo de mídia, conforme descrito na seção [tipos de mídia de áudio](audio-media-types.md). O conjunto exato de atributos de formato depende do codificador. (Consulte [formatos de mídia com suporte no Media Foundation](supported-media-formats-in-media-foundation.md).) Aqui está uma lista de atributos típicos de formato de áudio:



| Atributo de formato                                                                         | Descrição                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                           | O subtipo. Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md). |
| [\_canais de \_ número de áudio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)                   | O número de canais de áudio.                                    |
| [\_amostras de áudio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md)      | O número de amostras de áudio por segundo.                          |
| [\_alinhamento de \_ bloco de áudio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | O alinhamento do bloco.                                             |
| [áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | O número médio de bytes por segundo (a taxa de bits codificada).   |



 

Os parâmetros de codificação a seguir são definidos.



| Parâmetro de codificação                                                             | Descrição                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ \_ codificador de inserção do MF transcodificar não cercamento \_](mf-transcode-donot-insert-encoder.md) | Impede que a API de transcodificação Insira um codificador para o fluxo de áudio. |
| [\_ENCODINGPROFILE de transcodificação MF \_](mf-transcode-encodingprofile.md)             | Especifica o modelo de conformidade do dispositivo. (Aplica-se somente a arquivos ASF.)    |
| [\_QUALITYVSSPEED de transcodificação MF \_](mf-transcode-qualityvsspeed.md)               | Especifica a compensação entre a qualidade de codificação e a velocidade.                |



 

Você deve definir os atributos de formato. Os parâmetros de codificação são opcionais.

Uma maneira de encontrar um formato compatível com o codificador é chamar a função [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . O codificador desejado é especificado por subtipo. A função retorna uma coleção de tipos de mídia para esse codificador. Você pode selecionar um tipo na lista e copiar os atributos para o perfil. Para obter um exemplo de código que usa essa abordagem, consulte [tutorial: codificando um arquivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).

### <a name="video-attributes"></a>Atributos de vídeo

Para adicionar atributos para o fluxo de vídeo, chame [**IMFTranscodeProfile:: Setvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Esses atributos especificam como o fluxo de vídeo é codificado. Se o arquivo de saída não contiver um fluxo de vídeo, omita esses atributos.

Assim como acontece com os atributos de áudio, os atributos de vídeo se enquadram em duas categorias:

-   Atributos que especificam o formato do fluxo codificado
-   Atributos que especificam outros parâmetros de codificação.

Os atributos de formato são atributos de tipo de mídia, conforme descrito na seção [tipos de mídia de vídeo](video-media-types.md). Aqui está uma lista de atributos típicos de formato de vídeo:



| Atributo de formato                                                       | Descrição                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                         | O subtipo. Consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md). |
| [\_taxa de \_ quadros MF MT \_](mf-mt-frame-rate-attribute.md)                  | A taxa de quadros.                                                  |
| [\_tamanho do \_ quadro MF MT \_](mf-mt-frame-size-attribute.md)                  | O tamanho do quadro.                                                  |
| [**\_taxa de \_ \_ bits média de MF MT**](mf-mt-avg-bitrate-attribute.md)            | A taxa média de bits.                                            |
| [taxa de proporção de pixel do MF \_ MT \_ \_ \_](mf-mt-pixel-aspect-ratio-attribute.md) | A taxa de proporção de pixel.                                          |



 

Os parâmetros de codificação a seguir são definidos.



| Parâmetro de codificação                                                             | Descrição                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ \_ codificador de inserção do MF transcodificar não cercamento \_](mf-transcode-donot-insert-encoder.md) | Impede que a API de transcodificação Insira um codificador para o fluxo de vídeo. |
| [\_ENCODINGPROFILE de transcodificação MF \_](mf-transcode-encodingprofile.md)             | Especifica o modelo de conformidade do dispositivo. (Aplica-se somente a arquivos ASF.)    |
| [\_QUALITYVSSPEED de transcodificação MF \_](mf-transcode-qualityvsspeed.md)               | Especifica a compensação entre a qualidade de codificação e a velocidade.                |



 

Você deve definir os atributos de formato. Os parâmetros de codificação são opcionais.

### <a name="container-attributes"></a>Atributos de contêiner

Os atributos de contêiner definem as características de nível de arquivo do arquivo de saída. Para definir atributos de contêiner, chame [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Os atributos a seguir são definidos.



| Atributo                                                                          | Descrição                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_perfil de ajuste de transcodificação MF \_ \_](mf-transcode-adjust-profile.md)                  | Define as configurações de fluxo a serem usadas para a topologia de transcodificação. Você pode definir os sinalizadores para usar as configurações de fonte de entrada ou usar atributos de fluxo personalizados. |
| [\_contêinertype de transcodificação MF \_](mf-transcode-containertype.md)                     | Especifica o formato de arquivo do arquivo de saída, como MP4 ou ASF. Com base nesse valor, o coletor de mídia apropriado é adicionado à topologia.            |
| [\_transferência de \_ \_ metadados ignorar a transcodificação MF \_](mf-transcode-skip-metadata-transfer.md) | Especifica se os metadados da origem são copiados para o arquivo de saída.                                                                               |
| [\_topologymode de transcodificação MF \_](mf-transcode-topologymode.md)                       | Especifica se os codecs baseados em hardware podem ser usados durante a transcodificação.                                                                                |
| [\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_](mft-fieldofuse-unlock-attribute.md)          | Desbloqueia um codec que tem restrições de campo de uso. Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md).              |



 

O [atributo \_ \_ ContainerType de transcodificação MF](mf-transcode-containertype.md) é necessário. Os outros atributos de contêiner são opcionais.

## <a name="creating-a-transcode-topology"></a>Criando uma topologia de transcodificação

A topologia de transcodificação é uma topologia parcial que contém a origem da mídia, os codecs apropriados e o coletor de mídia. Para criar a topologia de transcodificação, chame para a função [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) . Essa função usa os seguintes parâmetros como entrada:

-   Um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.
-   O nome do arquivo de saída.
-   Um ponteiro para a interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) do perfil transcodificar.

A função retorna um ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .

## <a name="running-the-encoding-session"></a>Executando a sessão de codificação

Depois de criar a topologia, você estará pronto para codificar o arquivo. Você pode descartar o perfil neste momento.

1.  Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a sessão de mídia.
2.  Chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na sessão de mídia.
3.  Chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar a sessão de codificação.
4.  Aguarde o evento [MESessionEnded](mesessionended.md) .
5.  Chame [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a sessão de mídia.
6.  Aguarde o evento [MESessionClosed](mesessionclosed.md) .
7.  Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
8.  Chame [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

A maior parte do tempo gasto na codificação ocorre entre as etapas 3 e 4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de transcodificação](transcode-api.md)
</dt> <dt>

[Sobre a sessão de mídia](about-the-media-session.md)
</dt> </dl>

 

 



