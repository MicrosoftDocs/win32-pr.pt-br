---
description: Usando o sink de mídia EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Usando o sink de mídia EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ced80b4f9ee17093a00436a26f3f142281907597191791712fd6900520926ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826286"
---
# <a name="using-the-evr-media-sink"></a>Usando o sink de mídia EVR

O sink de mídia EVR (renderização de vídeo) aprimorado pode ser usado como um componente autônomo. No entanto, com mais frequência, um aplicativo criará o sink de mídia EVR dentro de uma topologia e, em seguida, usará a Sessão de Mídia para controlar a reprodução.

Há duas maneiras de criar o sink de mídia EVR:

-   A [**função MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) cria o sink de mídia.

-   A [**função MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) cria um objeto de ativação para o sink de mídia.

O sink de mídia EVR inicialmente tem um sink de fluxo, que corresponde ao fluxo de referência. Para adicionar novos sinks de fluxo, chame [**IMFMediaSink::AddStreamSink.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo aprimorada](enhanced-video-renderer.md)
</dt> <dt>

[Sinks de mídia](media-sinks.md)
</dt> </dl>

 

 



