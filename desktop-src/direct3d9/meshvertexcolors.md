---
description: Especifica as cores de vértice para uma malha, em vez de aplicar um material por face ou por malha.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370128"
---
# <a name="meshvertexcolors"></a><span data-ttu-id="716cb-103">MeshVertexColors</span><span class="sxs-lookup"><span data-stu-id="716cb-103">MeshVertexColors</span></span>

<span data-ttu-id="716cb-104">Especifica as cores de vértice para uma malha, em vez de aplicar um material por face ou por malha.</span><span class="sxs-lookup"><span data-stu-id="716cb-104">Specifies vertex colors for a mesh, instead of applying a material per face or per mesh.</span></span>

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

<span data-ttu-id="716cb-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="716cb-105">Where:</span></span>

-   <span data-ttu-id="716cb-106">nVertexColors-número de cores.</span><span class="sxs-lookup"><span data-stu-id="716cb-106">nVertexColors - Number of colors.</span></span> <span data-ttu-id="716cb-107">Isso corresponde ao número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="716cb-107">This matches the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="716cb-108">array IndexColor vertexColors \[ nVertexColors \] -matriz de cores indexadas.</span><span class="sxs-lookup"><span data-stu-id="716cb-108">array IndexColor vertexColors\[nVertexColors\] - Array of indexed colors.</span></span> <span data-ttu-id="716cb-109">Consulte [**IndexedColor**](indexedcolor.md).</span><span class="sxs-lookup"><span data-stu-id="716cb-109">See [**IndexedColor**](indexedcolor.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="716cb-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="716cb-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716cb-111">Modelos</span><span class="sxs-lookup"><span data-stu-id="716cb-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



