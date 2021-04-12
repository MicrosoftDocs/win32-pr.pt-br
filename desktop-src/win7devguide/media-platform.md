---
title: Plataforma de mídia
description: O Media Foundation e o DirectShow fornecem a base para o suporte de mídia no Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499134"
---
# <a name="media-platform"></a>Plataforma de mídia

O [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) e o [DirectShow](/windows/desktop/DirectShow/directshow) fornecem a base para o suporte de mídia no Windows. Media Foundation foi introduzido no Windows Vista como a substituição do DirectShow. No Windows 7, o Media Foundation foi aprimorado para fornecer melhor suporte ao formato, incluindo *MPEG-4*, bem como suporte para dispositivos de captura de vídeo e codecs de hardware.

## <a name="format-support"></a>Suporte de formato

No Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) fornece amplo suporte de formato que inclui codecs para o *H. 264* Video, *MJPEG* e *mp3*; novas fontes para *MP4*, *3GP*, *AAC* audio e *AVI*; e novos coletores de arquivo para *MP4*, *3GP* e *mp3*. (Consulte [formatos de mídia com suporte no Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).)

## <a name="hardware-devices"></a>Dispositivos de hardware

O [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) agora dá suporte aos seguintes tipos de dispositivos de hardware no pipeline de áudio/vídeo:

-   Dispositivos de captura de vídeo do *UVC 1,1* , como webcams
-   Dispositivos de captura de áudio
-   Codificadores de hardware e decodificadores
-   Processadores de vídeo de hardware, como conversores de espaço de cor

Os codecs de hardware podem executar transcodificação de vídeo muito rápida. Por exemplo, suponha que você deseja transferir um arquivo de *vídeo do Windows Media (WMV)* para um telefone celular que dá suporte apenas a arquivos *3GP* . Com um codificador de hardware, o arquivo pode ser transcodificado "conforme necessário" imediatamente antes de transferi-lo para o dispositivo.

Os dispositivos de hardware são representados em [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) por um objeto proxy e são usados no pipeline, assim como os componentes baseados em software. (Consulte [o que há de novo para Media Foundation](../medfound/whats-new-for-media-foundation.md).)

## <a name="simplified-programming-model"></a>Modelo de programação simplificado

No Windows Vista, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) expôs um conjunto de APIs relativamente baixo. Essas APIs são flexíveis, mas podem não ser apropriadas para executar tarefas. O Windows 7 adiciona novas APIs de alto nível que simplificam a gravação de aplicativos de mídia em *C++*. Essas novas APIs de alto nível incluem:

-   **MFPlay**. Essas APIs são projetadas para reprodução de áudio e vídeo. Eles dão suporte às operações de reprodução típicas (parar, pausar, reproduzir, buscar, controle de taxa, volume de áudio e assim por diante), ao mesmo tempo em que oculta os detalhes das APIs de nível inferior (a sessão e as camadas de topologia).
-   **Leitor de origem**. Você pode usar essas APIs para efetuar pull de dados brutos ou decodificados de um arquivo de mídia, sem saber nada sobre o formato subjacente. Por exemplo, você pode obter um bitmap em miniatura de um arquivo de vídeo ou obter quadros de vídeo ao vivo de uma webcam.
-   **Gravador de coletor**. Você pode usar essas APIs para criar arquivos de mídia passando dados não compactados ou codificados. Por exemplo, você pode codificar novamente ou remix um arquivo de vídeo.
-   **Transcodificar**. Essas APIs visam os cenários mais comuns de codificação de áudio e vídeo.

## <a name="platform-improvements"></a>Aprimoramentos da plataforma

O Windows 7 inclui vários aprimoramentos para as APIs de plataforma de [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) subjacentes. Os aplicativos avançados podem usar essas APIs diretamente; outros aplicativos obterão os benefícios indiretamente. Esses benefícios incluem:

-   Aprimoramentos no pipeline de vídeo para reduzir o consumo de energia e o uso de memória de vídeo.
-   Novas APIs de processamento de vídeo *DVXA* , que usam um modelo de composição mais flexível e são mais adequadas para formatos de vídeo *HD* .
-   Melhorias na forma como os plug-ins (fontes e decodificadores) são enumerados e gerenciados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo para Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 