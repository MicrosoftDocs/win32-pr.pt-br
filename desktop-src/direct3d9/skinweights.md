---
description: Esse modelo é instanciado em uma base por malha.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500258"
---
# <a name="skinweights"></a><span data-ttu-id="5e158-103">SkinWeights</span><span class="sxs-lookup"><span data-stu-id="5e158-103">SkinWeights</span></span>

<span data-ttu-id="5e158-104">Esse modelo é instanciado em uma base por malha.</span><span class="sxs-lookup"><span data-stu-id="5e158-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="5e158-105">Em uma malha, uma sequência de n instâncias desse modelo será exibida, em que n é o número de Bones (X quadros de arquivo) que influenciam os vértices na malha.</span><span class="sxs-lookup"><span data-stu-id="5e158-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="5e158-106">Cada instância do modelo basicamente define a influência de um Bone específico na malha.</span><span class="sxs-lookup"><span data-stu-id="5e158-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="5e158-107">Há uma lista de índices de vértice e uma lista correspondente de pesos.</span><span class="sxs-lookup"><span data-stu-id="5e158-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="5e158-108">Em que:</span><span class="sxs-lookup"><span data-stu-id="5e158-108">Where:</span></span>

-   <span data-ttu-id="5e158-109">O nome do Bone cuja influência está sendo definida é transformNodeName e nWeights é o número de vértices afetados por esse Bone.</span><span class="sxs-lookup"><span data-stu-id="5e158-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="5e158-110">Os vértices influenciados por esse Bone estão contidos em vertexIndices, e os pesos para cada um dos vértices influenciados por esse Bone estão contidos em pesos.</span><span class="sxs-lookup"><span data-stu-id="5e158-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="5e158-111">A matriz matrixOffset transforma os vértices de malha no espaço do Bone.</span><span class="sxs-lookup"><span data-stu-id="5e158-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="5e158-112">Quando concatenada com a transformação do Bone, isso fornece as coordenadas de espaço do mundo da malha, conforme afetado pelo Bone.</span><span class="sxs-lookup"><span data-stu-id="5e158-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="5e158-113">Consulte [**Matrix4x4**](matrix4x4.md).</span><span class="sxs-lookup"><span data-stu-id="5e158-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5e158-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e158-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e158-115">Modelos</span><span class="sxs-lookup"><span data-stu-id="5e158-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



