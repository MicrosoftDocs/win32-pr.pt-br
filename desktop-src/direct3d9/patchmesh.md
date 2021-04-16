---
description: Define uma malha definida por patches de Bézier. A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500260"
---
# <a name="patchmesh"></a><span data-ttu-id="9dfcd-104">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="9dfcd-104">PatchMesh</span></span>

<span data-ttu-id="9dfcd-105">Define uma malha definida por patches de Bézier.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="9dfcd-106">A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

<span data-ttu-id="9dfcd-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="9dfcd-107">Where:</span></span>

-   <span data-ttu-id="9dfcd-108">nVertices-número de vértices.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="9dfcd-109">vértices \[ nVertices \] -matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-109">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="9dfcd-110">Consulte [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcd-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="9dfcd-111">nPatches-número de patches.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-111">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="9dfcd-112">patches \[ nPatches \] -matriz de patches.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-112">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="9dfcd-113">Consulte [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcd-113">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="9dfcd-114">\[ ... \] -Qualquer modelo de arquivo. x pode ser usado aqui.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="9dfcd-115">Isso torna a arquitetura extensível.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-115">This makes the architecture extensible.</span></span>

<span data-ttu-id="9dfcd-116">Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-116">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="9dfcd-117">Este é um modelo herdado.</span><span class="sxs-lookup"><span data-stu-id="9dfcd-117">This is a legacy template.</span></span> <span data-ttu-id="9dfcd-118">O modelo de malha de patch mais recente é [**PatchMesh9**](patchmesh9.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcd-118">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9dfcd-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dfcd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfcd-120">Modelos</span><span class="sxs-lookup"><span data-stu-id="9dfcd-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



