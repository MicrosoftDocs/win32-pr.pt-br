---
description: PatchMesh9 define uma malha definida por patches Bézier, incluindo uma lista de vértices e os patches da malha indexando na matriz de vértices.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404699"
---
# <a name="patchmesh9"></a><span data-ttu-id="8336d-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="8336d-103">PatchMesh9</span></span>

<span data-ttu-id="8336d-104">Define uma malha definida por patches Bézier.</span><span class="sxs-lookup"><span data-stu-id="8336d-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="8336d-105">A primeira matriz é uma lista de vértices e a segunda matriz define os patches da malha indexando na matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="8336d-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

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

<span data-ttu-id="8336d-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="8336d-106">Where:</span></span>

-   <span data-ttu-id="8336d-107">Tipo – Patch de tipo de malha: retângulo, triângulo ou N-patch.</span><span class="sxs-lookup"><span data-stu-id="8336d-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="8336d-108">Grau – grau das variáveis na equação de curva.</span><span class="sxs-lookup"><span data-stu-id="8336d-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="8336d-109">Base – tipo de base de uma superfície de patch de alta ordem.</span><span class="sxs-lookup"><span data-stu-id="8336d-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="8336d-110">nVertices – número de vértices.</span><span class="sxs-lookup"><span data-stu-id="8336d-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="8336d-111">vértices \[ nVertices \] – matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="8336d-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="8336d-112">Consulte [**Vetor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="8336d-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="8336d-113">nPatches – número de patches.</span><span class="sxs-lookup"><span data-stu-id="8336d-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="8336d-114">patches \[ nPatches \] – matriz de patches.</span><span class="sxs-lookup"><span data-stu-id="8336d-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="8336d-115">Consulte [**Patch**](patch.md).</span><span class="sxs-lookup"><span data-stu-id="8336d-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="8336d-116">\[ ... \] - Qualquer modelo de arquivo .x pode ser usado aqui.</span><span class="sxs-lookup"><span data-stu-id="8336d-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="8336d-117">Isso torna a arquitetura extensível.</span><span class="sxs-lookup"><span data-stu-id="8336d-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="8336d-118">Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch.</span><span class="sxs-lookup"><span data-stu-id="8336d-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="8336d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8336d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8336d-120">Modelos</span><span class="sxs-lookup"><span data-stu-id="8336d-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



