---
description: Criando superfícies de vídeo DXVA-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Criando superfícies de vídeo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40058a02c179a8f9f0690eea9cce777bdd0563d5d27b36ddcb3d34f8fff8a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829046"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Criando superfícies de vídeo DXVA-HD

O aplicativo deve criar uma ou mais superfícies Direct3D para usar para os quadros de entrada. Eles devem ser alocados no pool de memória especificado pelo membro **InputPool** da estrutura [**DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Os seguintes tipos de superfície podem ser usados:

-   Uma superfície de vídeo criada chamando [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) e especificando o tipo de superfície **DXVAHD TIPO DE VÍDEO \_ \_ \_ \_ INPUT** ou **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ \_ PRIVATE.** Esse tipo de superfície é equivalente a uma superfície simples fora da tela.
-   Uma superfície de destino de renderização do decodificador, criada chamando [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) e especificando o tipo de superfície **\_ VideoDecoderRenderTarget DXVA2.** Esse tipo de superfície é usado para decodificação DXVA.
-   Uma superfície simples fora da tela.

O código a seguir mostra como alocar uma superfície de vídeo usando [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



