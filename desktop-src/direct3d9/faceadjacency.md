---
description: FaceAdjacency-este modelo é instanciado por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090504"
---
# <a name="faceadjacency"></a><span data-ttu-id="e07ce-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="e07ce-103">FaceAdjacency</span></span>

<span data-ttu-id="e07ce-104">Esse modelo é instanciado em uma base por malha, mantendo informações sobre quais vértices na malha são duplicados uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="e07ce-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="e07ce-105">Duplicatas resultam quando um vértice fica em um grupo de suavização ou em um limite de material.</span><span class="sxs-lookup"><span data-stu-id="e07ce-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="e07ce-106">A finalidade deste modelo é permitir que o carregador determine quais vértices que apresentam parâmetros periféricos diferentes são, na verdade, os mesmos vértices no modelo.</span><span class="sxs-lookup"><span data-stu-id="e07ce-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="e07ce-107">Determinados aplicativos (simplificação de malha, por exemplo) podem fazer uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="e07ce-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="e07ce-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="e07ce-108">Where:</span></span>

-   <span data-ttu-id="e07ce-109">nIndices-número de índices na malha.</span><span class="sxs-lookup"><span data-stu-id="e07ce-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="e07ce-110">índices \[ nIndices \] -matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="e07ce-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="e07ce-111">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e07ce-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07ce-112">Modelos</span><span class="sxs-lookup"><span data-stu-id="e07ce-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



