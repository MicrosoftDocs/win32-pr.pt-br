---
description: Define uma malha definida por patches de Bézier. A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105811394"
---
# <a name="patchmesh9"></a><span data-ttu-id="1abdb-104">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="1abdb-104">PatchMesh9</span></span>

<span data-ttu-id="1abdb-105">Define uma malha definida por patches de Bézier.</span><span class="sxs-lookup"><span data-stu-id="1abdb-105">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="1abdb-106">A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.</span><span class="sxs-lookup"><span data-stu-id="1abdb-106">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

<span data-ttu-id="1abdb-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="1abdb-107">Where:</span></span>

-   <span data-ttu-id="1abdb-108">Tipo de malha de patch tipo: retângulo, triângulo ou N-patch.</span><span class="sxs-lookup"><span data-stu-id="1abdb-108">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="1abdb-109">Grau-grau das variáveis na equação de curva.</span><span class="sxs-lookup"><span data-stu-id="1abdb-109">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="1abdb-110">Tipo base de uma superfície de patch de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="1abdb-110">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="1abdb-111">nVertices-número de vértices.</span><span class="sxs-lookup"><span data-stu-id="1abdb-111">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="1abdb-112">vértices \[ nVertices \] -matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="1abdb-112">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="1abdb-113">Consulte [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="1abdb-113">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="1abdb-114">nPatches-número de patches.</span><span class="sxs-lookup"><span data-stu-id="1abdb-114">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="1abdb-115">patches \[ nPatches \] -matriz de patches.</span><span class="sxs-lookup"><span data-stu-id="1abdb-115">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="1abdb-116">Consulte [**patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="1abdb-116">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="1abdb-117">\[ ... \] -Qualquer modelo de arquivo. x pode ser usado aqui.</span><span class="sxs-lookup"><span data-stu-id="1abdb-117">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="1abdb-118">Isso torna a arquitetura extensível.</span><span class="sxs-lookup"><span data-stu-id="1abdb-118">This makes the architecture extensible.</span></span>

<span data-ttu-id="1abdb-119">Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch.</span><span class="sxs-lookup"><span data-stu-id="1abdb-119">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="1abdb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1abdb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abdb-121">Modelos</span><span class="sxs-lookup"><span data-stu-id="1abdb-121">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



