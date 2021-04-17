---
description: Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764088"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="0df41-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="0df41-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="0df41-104">Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="0df41-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="0df41-105">Duplicatas resultam quando um vértice fica em um grupo de suavização ou em um limite de material.</span><span class="sxs-lookup"><span data-stu-id="0df41-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="0df41-106">A finalidade deste modelo é permitir que o carregador determine quais vértices que apresentam parâmetros periféricos diferentes são, na verdade, os mesmos vértices no modelo.</span><span class="sxs-lookup"><span data-stu-id="0df41-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="0df41-107">Determinados aplicativos (simplificação de malha, por exemplo) podem fazer uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="0df41-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="0df41-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="0df41-108">Where:</span></span>

-   <span data-ttu-id="0df41-109">nIndices-número de índices de vértice.</span><span class="sxs-lookup"><span data-stu-id="0df41-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="0df41-110">Este é o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="0df41-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="0df41-111">nOriginalVertices-número de vértices na malha antes de qualquer duplicação ocorrer.</span><span class="sxs-lookup"><span data-stu-id="0df41-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="0df41-112">Os índices de valor \[ n \] contêm o índice de vértices que o vértice \[ n \] na matriz de vértices para a malha teria tido se nenhuma duplicação tivesse ocorrido.</span><span class="sxs-lookup"><span data-stu-id="0df41-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="0df41-113">Os índices nessa matriz são os mesmos, portanto, indicam vértices duplicados.</span><span class="sxs-lookup"><span data-stu-id="0df41-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="0df41-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="0df41-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df41-115">Modelos</span><span class="sxs-lookup"><span data-stu-id="0df41-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



