---
description: Criando superfícies de vídeo de DXVA-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Criando superfícies de vídeo de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20dea8f34a275aab59b2d57f68ca76d46b1c1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102544"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Criando superfícies de vídeo de DXVA-HD

O aplicativo deve criar uma ou mais superfícies do Direct3D a serem usadas para os quadros de entrada. Eles devem ser alocados no pool de memória especificado pelo membro **InputPool** da estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Os seguintes tipos de superfície podem ser usados:

-   Uma superfície de vídeo criada chamando [**o \_ dispositivo IDXVAHD:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) e especificando o tipo de **\_ superfície DXVAHD \_ \_ \_ entrada de vídeo** ou tipo de superfície DXVAHD tipo de superfície **\_ \_ \_ \_ \_ privada entrada de vídeo** . Esse tipo de superfície é equivalente a uma superfície simples fora da tela.
-   Uma superfície de destino de renderização de decodificador, criada chamando [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) e especificando o tipo de superfície **DXVA2 \_ VideoDecoderRenderTarget** . Esse tipo de superfície é usado para a decodificação de DXVA.
-   Uma superfície simples fora da tela.

O código a seguir mostra como alocar uma superfície de vídeo, usando [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


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

 

 



