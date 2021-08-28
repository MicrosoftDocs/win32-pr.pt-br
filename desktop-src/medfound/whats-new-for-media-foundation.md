---
description: Microsoft Media Foundation foi introduzido no Windows Vista como substituição para DirectShow. é claro que DirectShow ainda tem suporte no Windows 7, mas os desenvolvedores são incentivados a usar Media Foundation em seus novos aplicativos de mídia digital.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Novidades para Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd2cd2b70ce23968ba9a302e4ab4e825914931ebffff651b534ee0974d75cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012056"
---
# <a name="whats-new-for-media-foundation"></a>O que há de novo para Media Foundation

Microsoft Media Foundation foi introduzido no Windows Vista como substituição para DirectShow. é claro que DirectShow ainda tem suporte no Windows 7, mas os desenvolvedores são incentivados a usar Media Foundation em seus novos aplicativos de mídia digital.

Os aprimoramentos para Media Foundation podem ser resumidos da seguinte maneira:

-   Melhor suporte a formato, incluindo MPEG-4
-   Suporte para dispositivos de captura e codecs de hardware
-   Um modelo de programação simplificado
-   Melhorias na plataforma

## <a name="better-format-support"></a>Melhor suporte a formato

a Media Foundation pipeline de áudio/vídeo foi implementada no Windows Vista, mas há suporte para um conjunto limitado de formatos e contêineres de arquivos, o que significa que alguns aplicativos precisavam voltar a tecnologias mais antigas, como DirectShow. no Windows 7, Media Foundation inclui os seguintes codecs novos, fontes de mídia e coletores de mídia:

-   Decodificador AAC
-   Codificador AAC
-   Fonte de arquivo AVI/WAVE
-   Decodificador de vídeo DV
-   Decodificador de vídeo H. 264
-   Codificador de vídeo H. 264
-   Decodificador de MJPEG
-   Coletor de arquivos MP3\*
-   Origem do arquivo MP4/3GP
-   Coletor de arquivos MP4/3GP

> [!Note]  
> O coletor de arquivos MP3 não inclui um codificador de áudio MP3.

 

Para obter mais informações, consulte [formatos de mídia com suporte no Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Suporte a dispositivos de hardware

O Media Foundation agora dá suporte aos seguintes tipos de dispositivos de hardware no pipeline de áudio/vídeo:

-   Dispositivos de captura de vídeo do UVC 1,1, como webcams
-   Dispositivos de captura de áudio
-   Codificadores de hardware e decodificadores
-   Processadores de vídeo de hardware, como conversores de espaço de cor

Os codecs de hardware podem executar transcodificação de vídeo muito rápida. por exemplo, um aplicativo pode transferir arquivos de vídeo de mídia Windows (WMV) para um telefone celular que dá suporte apenas a arquivos 3GP. Usando um codificador de hardware, o aplicativo pode transcodificar o arquivo no backgound, logo antes de transferi-lo para o dispositivo.

Os dispositivos de hardware são representados em Media Foundation por um objeto proxy e são usados no pipeline, assim como os componentes baseados em software.

## <a name="simplified-programming-model"></a>Modelo de programação simplificado

no Windows Vista, Media Foundation expor um conjunto de APIs relativamente baixo. Essas APIs são flexíveis, mas muito complexas para tarefas simples. o Windows 7 adiciona novas APIs de alto nível que simplificam a gravação de aplicativos de mídia em C++. Essas novas APIs de alto nível incluem o seguinte.



| API                                | Descrição                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Leitor de origem](source-reader.md) | O leitor de origem recebe dados brutos ou decodificados de um arquivo de mídia. Por exemplo, você pode usar o leitor de origem para obter bitmaps em miniatura de um arquivo de vídeo ou para analisar os dados de formato de onda em um arquivo de áudio. Você também pode usar o leitor de origem para obter dados dinâmicos de um dispositivo de captura de áudio ou vídeo. <br/> |
| [Gravador do coletor](sink-writer.md)     | O gravador do coletor permite que você crie arquivos de mídia passando dados não compactados ou codificados. Por exemplo, você pode usá-lo para codificar novamente um arquivo de vídeo ou capturar o vídeo ao vivo de uma webcam para um arquivo.                                                                                                         |
| [API de transcodificação](transcode-api.md) | Esse recurso dá suporte aos cenários de codificação de áudio/vídeo mais comuns.<br/>                                                                                                                                                                                                                               |



 

Você ainda pode usar as APIs de nível inferior no Media Foundation. Você pode fazer isso se precisar de mais controle sobre o pipeline de áudio/vídeo.

## <a name="platform-improvements"></a>Aprimoramentos da plataforma

o Windows 7 inclui vários aprimoramentos para as APIs de plataforma de Media Foundation subjacentes. Os aplicativos avançados podem usar essas APIs diretamente; outros aplicativos obterão os benefícios indiretamente. As melhorias incluem:

-   Alterações no pipeline de vídeo para reduzir o consumo de energia e o uso de memória de vídeo.
-   [DXVA-HD](dxva-hd.md): o Microsoft DirectX Video Acceleration High Definition (DXVA-HD) é uma nova API para processamento de vídeo acelerado por hardware. O DXVA-HD oferece um modelo de composição mais flexível do que a API de processamento de vídeo de DXVA anterior e é mais adequada para formatos de vídeo de alta definição.
-   Um novo mecanismo para enumerar fontes e decodificadores, que inclui valores de mérito e uma lista preferida/bloqueada. Esse recurso melhora a confiabilidade geral do sistema. Para obter mais informações, consulte estes tópicos:
    -   [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Mérito do codec](codec-merit.md)

## <a name="sdk-changes"></a>Alterações do SDK

-   Novos cabeçalhos e arquivos de biblioteca: [cabeçalhos e bibliotecas de Media Foundation](media-foundation-headers-and-libraries.md)
-   alterações de DLL e. lib: [alterações de biblioteca no Windows 7](media-foundation-headers-and-libraries.md)
-   Novos exemplos de SDK:
    -   [Exemplo de clipe de áudio](audio-clip-sample.md)
    -   [Exemplo de DXVA-HD](dxva-hd-sample.md)
    -   [Exemplo de MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Exemplo de MFCaptureToFile](mfcapturetofile-sample.md)
    -   [Exemplo de transcodificação](transcode-sample.md)
    -   [Exemplo de VideoThumbnail](videothumbnail-sample.md)
-   Melhorias no [TopoEdit](topoedit.md):
    -   Suporte para transcodificação. Consulte criando uma [topologia de transcodificação com TopoEdit](building-a-transcode-topology-with-topoedit.md).
    -   Suporte para captura de áudio e vídeo. Consulte o [menu de topologia](topology-menu.md).

## <a name="new-in-windows-8"></a>Novo no Windows 8

algumas das novas atualizações para Media Foundation com Windows 8 são:

-   O [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) controla um ou mais dispositivos de captura. Consulte os [atributos do mecanismo de captura](capture-engine-attributes.md) para obter uma lista de atributos. Outras interfaces relacionadas à captura de mídia novas são [**IMFCapturePhotoSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**IMFCaptureRecordSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**IMFCaptureSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)e [**IMFCaptureSource**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   As seguintes extensões de classe de Media Foundation são novas para o Windows 8:
    -   [**IMFMediaEngineEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**IMFSinkWriterEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**IMFSourceReaderEx**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**IMFWorkQueueServicesEx**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   A [API de vídeo do Direct3D 11](direct3d-11-video-apis.md) é nova para Windows 8. Windows 8 os aplicativos da área de trabalho ainda podem usar a [api de vídeo do direct3d 9](direct3d-video-apis.md), mas Windows aplicativos da loja devem usar a nova api de vídeo do direct3d 11. Para obter informações sobre mais informações sobre o vídeo do Microsoft Direct3D 11, consulte [dando suporte à decodificação de vídeo do Direct3D 11 em Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Houve atualizações e melhorias para Media Foundation filas de trabalho. Consulte [aprimoramentos na fila de trabalho e threading](media-foundation-work-queue-and-threading-improvements.md) para obter mais informações.
-   [Codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).
-   para obter uma lista da API de Media Foundation que pode ser usada com aplicativos da Windows store [, consulte Win32 e COM para aplicativos da Windows Store (multimídia)](media-foundation-headers-and-libraries.md).
-   O Media Foundation não está incluído nas edições N e KN do Windows 8. para obter mais informações, consulte [Microsoft Windows Media Feature Pack para versões N e KN de todas as edições do Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




