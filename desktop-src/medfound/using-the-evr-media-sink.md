---
description: Usando o coletor de mídia do EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Usando o coletor de mídia do EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105785265"
---
# <a name="using-the-evr-media-sink"></a>Usando o coletor de mídia do EVR

O coletor de mídia EVR (processador de vídeo avançado) pode ser usado como um componente autônomo. No entanto, com mais frequência, um aplicativo criará o coletor de mídia do EVR dentro de uma topologia e, em seguida, usará a sessão de mídia para controlar a reprodução.

Há duas maneiras de criar o coletor de mídia do EVR:

-   A função [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) cria o coletor de mídia.

-   A função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) cria um objeto de ativação para o coletor de mídia.

Inicialmente, o coletor de mídia EVR tem um coletor de fluxo, que corresponde ao fluxo de referência. Para adicionar novos coletores de fluxo, chame [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> <dt>

[Coletores de mídia](media-sinks.md)
</dt> </dl>

 

 



