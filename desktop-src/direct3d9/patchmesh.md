---
description: PatchMesh define uma malha definida por patches bézier, incluindo uma lista de vértices e os patches para a malha indexando na matriz de vértices.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404709"
---
# <a name="patchmesh"></a><span data-ttu-id="b3bdd-103">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="b3bdd-103">PatchMesh</span></span>

<span data-ttu-id="b3bdd-104">Define uma malha definida por patches Bézier.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="b3bdd-105">A primeira matriz é uma lista de vértices e a segunda matriz define os patches da malha indexando na matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="b3bdd-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="b3bdd-106">Where:</span></span>

-   <span data-ttu-id="b3bdd-107">nVertices – número de vértices.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="b3bdd-108">vértices \[ nVertices \] – matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="b3bdd-109">Consulte [**Vetor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="b3bdd-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="b3bdd-110">nPatches – número de patches.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="b3bdd-111">patches \[ nPatches \] – matriz de patches.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="b3bdd-112">Consulte [**Patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="b3bdd-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="b3bdd-113">\[ ... \] - Qualquer modelo de arquivo .x pode ser usado aqui.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="b3bdd-114">Isso torna a arquitetura extensível.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="b3bdd-115">Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="b3bdd-116">Esse é um modelo herdado.</span><span class="sxs-lookup"><span data-stu-id="b3bdd-116">This is a legacy template.</span></span> <span data-ttu-id="b3bdd-117">O modelo de malha de patch mais recente [**é PatchMesh9.**](patchmesh9.md)</span><span class="sxs-lookup"><span data-stu-id="b3bdd-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b3bdd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3bdd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bdd-119">Modelos</span><span class="sxs-lookup"><span data-stu-id="b3bdd-119">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



