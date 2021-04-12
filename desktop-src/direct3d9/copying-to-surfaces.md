---
description: 'Ao usar IDirect3DDevice9:: UpdateSurface, passe um retângulo na superfície de origem ou use NULL para especificar toda a superfície.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Copiando para superfícies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457154"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="fdae4-103">Copiando para superfícies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fdae4-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="fdae4-104">Ao usar [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), passe um retângulo na superfície de origem ou use **NULL** para especificar toda a superfície.</span><span class="sxs-lookup"><span data-stu-id="fdae4-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="fdae4-105">Você também passa um ponto na superfície de destino até a qual a posição superior esquerda do retângulo na imagem de origem é copiada.</span><span class="sxs-lookup"><span data-stu-id="fdae4-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="fdae4-106">Este método não oferece suporte a recorte.</span><span class="sxs-lookup"><span data-stu-id="fdae4-106">This method does not support clipping.</span></span> <span data-ttu-id="fdae4-107">A operação falhará a menos que o retângulo de origem e o retângulo de destino correspondente estejam completamente contidos nas superfícies de origem e de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fdae4-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="fdae4-108">Este método não oferece suporte a mesclagem alfa, chaves de cor ou conversão de formato.</span><span class="sxs-lookup"><span data-stu-id="fdae4-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="fdae4-109">Observe que as superfícies de destino e origem devem ser distintas.</span><span class="sxs-lookup"><span data-stu-id="fdae4-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="fdae4-110">Para outras restrições ao usar UpdateSurface, consulte [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span><span class="sxs-lookup"><span data-stu-id="fdae4-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="fdae4-111">Os métodos a seguir também estão disponíveis em C++/C para copiar imagens para uma superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fdae4-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="fdae4-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="fdae4-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="fdae4-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="fdae4-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="fdae4-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="fdae4-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="fdae4-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="fdae4-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="fdae4-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="fdae4-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="fdae4-117">**IDirect3DDevice9::UpdateSurface**</span><span class="sxs-lookup"><span data-stu-id="fdae4-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="fdae4-118">Exemplo de UpdateSurface</span><span class="sxs-lookup"><span data-stu-id="fdae4-118">UpdateSurface Example</span></span>

<span data-ttu-id="fdae4-119">O exemplo a seguir copia dois retângulos da superfície de origem para uma superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="fdae4-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="fdae4-120">O primeiro retângulo é copiado de (0, 0, 50, 50) na superfície de origem para o mesmo local na superfície de destino e o segundo retângulo é copiado de (50, 50, 100, 100) na superfície de origem para (150, 150, 200, 200) na superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="fdae4-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="fdae4-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdae4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdae4-122">Superfícies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="fdae4-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="fdae4-123">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="fdae4-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
