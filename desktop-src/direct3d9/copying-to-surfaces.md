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
# <a name="copying-to-surfaces-direct3d-9"></a>Copiando para superfícies (Direct3D 9)

Ao usar [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), passe um retângulo na superfície de origem ou use **NULL** para especificar toda a superfície. Você também passa um ponto na superfície de destino até a qual a posição superior esquerda do retângulo na imagem de origem é copiada. Este método não oferece suporte a recorte. A operação falhará a menos que o retângulo de origem e o retângulo de destino correspondente estejam completamente contidos nas superfícies de origem e de destino, respectivamente. Este método não oferece suporte a mesclagem alfa, chaves de cor ou conversão de formato. Observe que as superfícies de destino e origem devem ser distintas.

Para outras restrições ao usar UpdateSurface, consulte [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

Os métodos a seguir também estão disponíveis em C++/C para copiar imagens para uma superfície do Direct3D.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>Exemplo de UpdateSurface

O exemplo a seguir copia dois retângulos da superfície de origem para uma superfície de destino. O primeiro retângulo é copiado de (0, 0, 50, 50) na superfície de origem para o mesmo local na superfície de destino e o segundo retângulo é copiado de (50, 50, 100, 100) na superfície de origem para (150, 150, 200, 200) na superfície de destino.


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
