---
title: Plataforma de mídia
description: Media Foundation e DirectShow fornecem a base para o suporte de mídia no Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a4db7d84745f64f3fe80faed267e58d1f5ddbce4ab82ed75b38453f82b0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964575"
---
# <a name="media-platform"></a>Plataforma de mídia

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) e [DirectShow](/windows/desktop/DirectShow/directshow) fornecem a base para o suporte de mídia no Windows. Media Foundation foi introduzido no Windows Vista como substituição para DirectShow. no Windows 7, Media Foundation foi aprimorado para fornecer melhor suporte ao formato, incluindo *MPEG-4*, bem como suporte para dispositivos de captura de vídeo e codecs de hardware.

## <a name="format-support"></a>Suporte de formato

no Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) fornece amplo suporte de formato que inclui codecs para o *H. 264* video, *MJPEG* e *MP3*; novas fontes para *MP4*, *3GP*, *AAC* audio e *AVI*; e novos coletores de arquivo para *MP4*, *3GP* e *mp3*. (Consulte [formatos de mídia com suporte no Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).)

## <a name="hardware-devices"></a>Dispositivos de hardware

O [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) agora dá suporte aos seguintes tipos de dispositivos de hardware no pipeline de áudio/vídeo:

-   Dispositivos de captura de vídeo do *UVC 1,1* , como webcams
-   Dispositivos de captura de áudio
-   Codificadores de hardware e decodificadores
-   Processadores de vídeo de hardware, como conversores de espaço de cor

Os codecs de hardware podem executar transcodificação de vídeo muito rápida. por exemplo, suponha que você deseja transferir um arquivo de *vídeo de mídia Windows (WMV)* para um telefone celular que dá suporte apenas a arquivos *3GP* . Com um codificador de hardware, o arquivo pode ser transcodificado "conforme necessário" imediatamente antes de transferi-lo para o dispositivo.

Os dispositivos de hardware são representados em [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) por um objeto proxy e são usados no pipeline, assim como os componentes baseados em software. (Consulte [o que há de novo para Media Foundation](../medfound/whats-new-for-media-foundation.md).)

## <a name="simplified-programming-model"></a>Modelo de programação simplificado

no Windows Vista, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) expor um conjunto de APIs relativamente baixo. Essas APIs são flexíveis, mas podem não ser apropriadas para executar tarefas. o Windows 7 adiciona novas APIs de alto nível que simplificam a gravação de aplicativos de mídia em *C++*. Essas novas APIs de alto nível incluem:

-   **MFPlay**. Essas APIs são projetadas para reprodução de áudio e vídeo. Eles dão suporte às operações de reprodução típicas (parar, pausar, reproduzir, buscar, controle de taxa, volume de áudio e assim por diante), ao mesmo tempo em que oculta os detalhes das APIs de nível inferior (a sessão e as camadas de topologia).
-   **Leitor de origem**. Você pode usar essas APIs para efetuar pull de dados brutos ou decodificados de um arquivo de mídia, sem saber nada sobre o formato subjacente. Por exemplo, você pode obter um bitmap em miniatura de um arquivo de vídeo ou obter quadros de vídeo ao vivo de uma webcam.
-   **Gravador de coletor**. Você pode usar essas APIs para criar arquivos de mídia passando dados não compactados ou codificados. Por exemplo, você pode codificar novamente ou remix um arquivo de vídeo.
-   **Transcodificar**. Essas APIs visam os cenários mais comuns de codificação de áudio e vídeo.

## <a name="platform-improvements"></a>Aprimoramentos da plataforma

o Windows 7 inclui vários aprimoramentos para as APIs de plataforma de [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) subjacentes. Os aplicativos avançados podem usar essas APIs diretamente; outros aplicativos obterão os benefícios indiretamente. Esses benefícios incluem:

-   Aprimoramentos no pipeline de vídeo para reduzir o consumo de energia e o uso de memória de vídeo.
-   Novas APIs de processamento de vídeo *DVXA* , que usam um modelo de composição mais flexível e são mais adequadas para formatos de vídeo *HD* .
-   Melhorias na forma como os plug-ins (fontes e decodificadores) são enumerados e gerenciados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo para Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 