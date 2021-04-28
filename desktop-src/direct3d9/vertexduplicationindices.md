---
description: VertexDuplicationIndices-este modelo é instanciado por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090173"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="61ecb-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="61ecb-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="61ecb-104">Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="61ecb-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="61ecb-105">Duplicatas resultam quando um vértice fica em um grupo de suavização ou em um limite de material.</span><span class="sxs-lookup"><span data-stu-id="61ecb-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="61ecb-106">A finalidade deste modelo é permitir que o carregador determine quais vértices que apresentam parâmetros periféricos diferentes são, na verdade, os mesmos vértices no modelo.</span><span class="sxs-lookup"><span data-stu-id="61ecb-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="61ecb-107">Determinados aplicativos (simplificação de malha, por exemplo) podem fazer uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="61ecb-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="61ecb-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="61ecb-108">Where:</span></span>

-   <span data-ttu-id="61ecb-109">nIndices-número de índices de vértice.</span><span class="sxs-lookup"><span data-stu-id="61ecb-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="61ecb-110">Este é o número de vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="61ecb-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="61ecb-111">nOriginalVertices-número de vértices na malha antes de qualquer duplicação ocorrer.</span><span class="sxs-lookup"><span data-stu-id="61ecb-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="61ecb-112">Os índices de valor \[ n \] contêm o índice de vértices que o vértice \[ n \] na matriz de vértices para a malha teria tido se nenhuma duplicação tivesse ocorrido.</span><span class="sxs-lookup"><span data-stu-id="61ecb-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="61ecb-113">Os índices nessa matriz são os mesmos, portanto, indicam vértices duplicados.</span><span class="sxs-lookup"><span data-stu-id="61ecb-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="61ecb-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="61ecb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ecb-115">Modelos</span><span class="sxs-lookup"><span data-stu-id="61ecb-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



