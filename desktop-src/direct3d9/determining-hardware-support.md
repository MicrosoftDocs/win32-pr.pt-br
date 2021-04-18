---
description: O Direct3D fornece as seguintes funções para determinar o suporte de hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinando o suporte de hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808337"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="e5dbf-103">Determinando o suporte de hardware (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e5dbf-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="e5dbf-104">O Direct3D fornece as seguintes funções para determinar o suporte de hardware.</span><span class="sxs-lookup"><span data-stu-id="e5dbf-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="e5dbf-105">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="e5dbf-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="e5dbf-106">Usado para verificar se um formato de superfície pode ser usado como uma textura, se um formato de superfície pode ser usado como uma textura e um destino de renderização, ou se um formato de superfície pode ser usado como um buffer de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e5dbf-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="e5dbf-107">Além disso, esse método é usado para verificar o suporte ao formato do buffer de profundidade e o suporte ao formato de buffer de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e5dbf-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="e5dbf-108">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="e5dbf-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="e5dbf-109">Usado para verificar a capacidade de um dispositivo de executar aceleração de hardware, a capacidade de um dispositivo de criar uma cadeia de permuta para apresentação ou a capacidade de um dispositivo de renderizar para o formato de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="e5dbf-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="e5dbf-110">**IDirect3D9::CheckDepthStencilMatch**</span><span class="sxs-lookup"><span data-stu-id="e5dbf-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="e5dbf-111">Usado para verificar se um formato de buffer de profundidade/estêncil é compatível com um formato de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="e5dbf-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="e5dbf-112">Observe que, antes de chamar esse método, o aplicativo deve chamar [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) nos formatos de profundidade e de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="e5dbf-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5dbf-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5dbf-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5dbf-114">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="e5dbf-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
