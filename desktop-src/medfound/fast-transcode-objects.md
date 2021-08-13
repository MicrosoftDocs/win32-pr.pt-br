---
description: Este tópico descreveu como usar a API de transcodificar para codificar um arquivo de mídia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Usando a API transcódigo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e32ea24ebd4803319713be5fe7789cf41c3a99733338bdfe5ad69baf7396bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742474"
---
# <a name="using-the-transcode-api"></a>Usando a API transcódigo

Este tópico descreveu como usar a API de transcodificar para codificar um arquivo de mídia.

-   [Visão geral](#overview)
-   [Criando uma fonte de mídia](#creating-a-media-source)
-   [Criando um perfil de transcodificar](#creating-a-transcode-profile)
    -   [Atributos de áudio](#audio-attributes)
    -   [Atributos de vídeo](#video-attributes)
    -   [Atributos de contêiner](#container-attributes)
-   [Criando uma topologia de transcodificar](#creating-a-transcode-topology)
-   [Executando a sessão de codificação](#running-the-encoding-session)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Antes de usar a API de transcodificar, o aplicativo deve ter as seguintes informações:

-   O caminho ou a URL para um arquivo de mídia existente que será codificado de novo.
-   O nome do arquivo de saída.
-   O tipo de contêiner para o arquivo de saída, como MP4 ou FORMATO DE STREAMING Avançado (ASF).
-   O formato de codificação. Essas informações incluem os tipos de mídia que descrevem os fluxos de áudio e vídeo codificados.

Para usar a API de transcodificar, um aplicativo executa as etapas a seguir.

1.  Crie uma fonte de mídia para ler o arquivo de origem.
2.  Crie um perfil de transcodificar. Adicione atributos que descrevem o fluxo de áudio, o fluxo de vídeo e o contêiner de arquivos.
3.  Use o perfil de transcodificar para criar uma topologia de codificação. (Para obter mais informações sobre topologias, consulte [Sobre topologias](about-topologies.md).)
4.  De definir a topologia na Sessão [de Mídia](media-session.md).
5.  Inicie a Sessão de Mídia e aguarde o [evento MESessionEnded.](mesessionended.md)

O restante deste tópico descreve essas etapas mais detalhadamente.

## <a name="creating-a-media-source"></a>Criando uma fonte de mídia

Uma fonte de mídia é um objeto que lê e analisar o arquivo de origem. Para criar uma fonte de mídia, use o [Resolvedor de Origem](source-resolver.md). Você pode encontrar o código de exemplo no tópico [Usando o Resolvedor de Origem](using-the-source-resolver.md).

## <a name="creating-a-transcode-profile"></a>Criando um perfil de transcodificar

Um *perfil de transcódigo* descreve o formato e as configurações que são usadas para codificar o arquivo de saída. O perfil de transcodificar contém três conjuntos de atributos:

-   Atributos de áudio: descreva o formato de áudio de destino e as configurações do codificador de áudio.
-   Atributos de vídeo: descreva o formato de vídeo de destino e as configurações do codificador de vídeo.
-   Atributos de contêiner: defina o tipo de contêiner de arquivo, bem como algumas configurações de codificação global.

Para criar um perfil de transcodificar, chame a [**função MFCreateTranscodeProfile.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) Essa função retorna um ponteiro para a interface [**IMFTranscodeProfile.**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) O objeto de perfil inicial está vazio; ele não contém atributos. A próxima etapa é adicionar os atributos que definem o perfil.

### <a name="audio-attributes"></a>Atributos de áudio

Para adicionar atributos para o fluxo de áudio, chame [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes). Esses atributos especificam como o fluxo de áudio é codificado. Se o arquivo de saída não conter um fluxo de áudio, omita esses atributos.

Os atributos de áudio se enquadram em duas categorias:

-   Atributos que especificam o formato do fluxo codificado
-   Atributos que especificam outros parâmetros de codificação.

Atributos de formato são simplesmente atributos de tipo de mídia, conforme descrito na seção [Tipos de Mídia de Áudio](audio-media-types.md). O conjunto exato de atributos de formato depende do codificador. (Consulte [Formatos de mídia com suporte Media Foundation](supported-media-formats-in-media-foundation.md).) Aqui está uma lista de atributos típicos de formato de áudio:



| Atributo format                                                                         | Descrição                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [SUBTIPO \_ MF MT \_](mf-mt-subtype-attribute.md)                                           | O subtipo. Consulte [GUIDs de subtipo de áudio.](audio-subtype-guids.md) |
| [CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_](mf-mt-audio-num-channels-attribute.md)                   | O número de canais de áudio.                                    |
| [AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md)      | O número de amostras de áudio por segundo.                          |
| [ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT](mf-mt-audio-block-alignment-attribute.md)             | O alinhamento do bloco.                                             |
| [BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | O número médio de bytes por segundo (a taxa de bits codificada).   |



 

Os parâmetros de codificação a seguir são definidos.



| Parâmetro de codificação                                                             | Descrição                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ TRANSCODE \_ DONOT \_ INSERT \_ ENCODER](mf-transcode-donot-insert-encoder.md) | Impede que a API de transcodificar insira um codificador para o fluxo de áudio. |
| [MF \_ TRANSCODE \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Especifica o modelo de conformidade do dispositivo. (Aplica-se somente a arquivos ASF.)    |
| [MF \_ TRANSCODE \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Especifica a diferença entre a qualidade e a velocidade da codificação.                |



 

Você deve definir os atributos de formato. Os parâmetros de codificação são opcionais.

Uma maneira de encontrar um formato compatível com o codificador é chamar a função [**MFTranscodeGetAudioOutputAvailableTypes.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) O codificador desejado é especificado por subtipo. A função retorna uma coleção de tipos de mídia para esse codificador. Você pode selecionar um tipo na lista e copiar os atributos para o perfil. Para exemplo de código que usa essa [abordagem, consulte Tutorial: Codificando um arquivo WMA.](tutorial--converting-an-mp3-file-to-a-wma-file.md)

### <a name="video-attributes"></a>Atributos de vídeo

Para adicionar atributos para o fluxo de vídeo, chame [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes). Esses atributos especificam como o fluxo de vídeo é codificado. Se o arquivo de saída não conter um fluxo de vídeo, omita esses atributos.

Assim como nos atributos de áudio, os atributos de vídeo se enquadram em duas categorias:

-   Atributos que especificam o formato do fluxo codificado
-   Atributos que especificam outros parâmetros de codificação.

Atributos de formato são atributos de tipo de mídia, conforme descrito na seção [Tipos de Mídia de Vídeo](video-media-types.md). Aqui está uma lista de atributos típicos de formato de vídeo:



| Atributo format                                                       | Descrição                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [SUBTIPO \_ MF MT \_](mf-mt-subtype-attribute.md)                         | O subtipo. Consulte [GUIDs de subtipo de vídeo.](video-subtype-guids.md) |
| [TAXA DE \_ QUADROS MT \_ \_ MF](mf-mt-frame-rate-attribute.md)                  | A taxa de quadros.                                                  |
| [TAMANHO DO \_ QUADRO MT MF \_ \_](mf-mt-frame-size-attribute.md)                  | O tamanho do quadro.                                                  |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)            | A taxa média de bits.                                            |
| [TAXA DE \_ PROPORÇÃO DO PIXEL MT \_ \_ \_ MF](mf-mt-pixel-aspect-ratio-attribute.md) | A taxa de proporção de pixel.                                          |



 

Os parâmetros de codificação a seguir são definidos.



| Parâmetro de codificação                                                             | Descrição                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MF \_ TRANSCODE \_ DONOT \_ INSERT \_ ENCODER](mf-transcode-donot-insert-encoder.md) | Impede que a API de transcodificar insira um codificador para o fluxo de vídeo. |
| [MF \_ TRANSCODE \_ ENCODINGPROFILE](mf-transcode-encodingprofile.md)             | Especifica o modelo de conformidade do dispositivo. (Aplica-se somente a arquivos ASF.)    |
| [MF \_ TRANSCODE \_ QUALITYVSSPEED](mf-transcode-qualityvsspeed.md)               | Especifica a diferença entre a qualidade e a velocidade da codificação.                |



 

Você deve definir os atributos de formato. Os parâmetros de codificação são opcionais.

### <a name="container-attributes"></a>Atributos de contêiner

Os atributos de contêiner definem características de nível de arquivo do arquivo de saída. Para definir atributos de contêiner, chame [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Os atributos a seguir são definidos.



| Atributo                                                                          | Descrição                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PERFIL DE AJUSTE \_ DE TRANSCÓDIGO MF \_ \_](mf-transcode-adjust-profile.md)                  | Define as configurações de fluxo a ser usadas para a topologia de transcodificar. Você pode definir os sinalizadores para usar as configurações de origem de entrada ou usar atributos de fluxo personalizados. |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                     | Especifica o formato de arquivo do arquivo de saída, como MP4 ou ASF. Com base nesse valor, o sink de mídia apropriado é adicionado à topologia.            |
| [MF \_ TRANSCODE \_ SKIP \_ METADATA \_ TRANSFER](mf-transcode-skip-metadata-transfer.md) | Especifica se os metadados da origem são copiados para o arquivo de saída.                                                                               |
| [MF \_ TRANSCODE \_ TOPOLOGYMODE](mf-transcode-topologymode.md)                       | Especifica se codecs baseados em hardware podem ser usados durante a transcodificação.                                                                                |
| [Atributo MFT \_ FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)          | Desbloqueia um codec que tem restrições de campo de uso. Para obter mais informações, consulte [Restrições de campo de uso.](field-of-use-restrictions.md)              |



 

O [atributo \_ \_ CONTAINERTYPE MF TRANSCODE](mf-transcode-containertype.md) é necessário. Os outros atributos de contêiner são opcionais.

## <a name="creating-a-transcode-topology"></a>Criando uma topologia de transcodificar

A topologia de transcódigo é uma topologia parcial que contém a fonte de mídia, os codecs apropriados e o sink de mídia. Para criar a topologia de transcodificar, chame a [**função MFCreateTranscodeTopology.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) Essa função assume os seguintes parâmetros como entrada:

-   Um ponteiro para a [**interface IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.
-   O nome do arquivo de saída.
-   Um ponteiro para a interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) do perfil de transcódigo.

A função retorna um ponteiro para a interface [**IMFTopology.**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="running-the-encoding-session"></a>Executando a sessão de codificação

Depois de criar a topologia, você estará pronto para codificar o arquivo. Você pode descartar o perfil neste ponto.

1.  Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a Sessão de Mídia.
2.  Chame [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na Sessão de Mídia.
3.  Chame [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar a sessão de codificação.
4.  Aguarde o [evento MESessionEnded.](mesessionended.md)
5.  Chame [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a Sessão de Mídia.
6.  Aguarde o [evento MESessionClosed.](mesessionclosed.md)
7.  Chame [**IMFMediaSource::Shutdown.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)
8.  Chame [**IMFMediaSession::Shutdown.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)

A maior parte do tempo gasto na codificação ocorre entre as etapas 3 e 4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de transcodificar](transcode-api.md)
</dt> <dt>

[Sobre a sessão de mídia](about-the-media-session.md)
</dt> </dl>

 

 



