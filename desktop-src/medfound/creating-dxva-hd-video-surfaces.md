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
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="2c910-103">Criando superfícies de vídeo de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="2c910-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="2c910-104">O aplicativo deve criar uma ou mais superfícies do Direct3D a serem usadas para os quadros de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c910-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="2c910-105">Eles devem ser alocados no pool de memória especificado pelo membro **InputPool** da estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="2c910-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="2c910-106">Os seguintes tipos de superfície podem ser usados:</span><span class="sxs-lookup"><span data-stu-id="2c910-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="2c910-107">Uma superfície de vídeo criada chamando [**o \_ dispositivo IDXVAHD:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) e especificando o tipo de **\_ superfície DXVAHD \_ \_ \_ entrada de vídeo** ou tipo de superfície DXVAHD tipo de superfície **\_ \_ \_ \_ \_ privada entrada de vídeo** .</span><span class="sxs-lookup"><span data-stu-id="2c910-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="2c910-108">Esse tipo de superfície é equivalente a uma superfície simples fora da tela.</span><span class="sxs-lookup"><span data-stu-id="2c910-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="2c910-109">Uma superfície de destino de renderização de decodificador, criada chamando [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) e especificando o tipo de superfície **DXVA2 \_ VideoDecoderRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="2c910-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="2c910-110">Esse tipo de superfície é usado para a decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="2c910-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="2c910-111">Uma superfície simples fora da tela.</span><span class="sxs-lookup"><span data-stu-id="2c910-111">An off-screen plain surface.</span></span>

<span data-ttu-id="2c910-112">O código a seguir mostra como alocar uma superfície de vídeo, usando [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span><span class="sxs-lookup"><span data-stu-id="2c910-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2c910-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c910-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c910-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="2c910-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



