---
description: Usado pelo modelo de malha para definir as faces de uma malha. Cada elemento da matriz nFaceVertexIndices faz referência a um vértice de malha usado para criar a face.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087247"
---
# <a name="meshface"></a><span data-ttu-id="a2c9a-104">MeshFace</span><span class="sxs-lookup"><span data-stu-id="a2c9a-104">MeshFace</span></span>

<span data-ttu-id="a2c9a-105">Usado pelo modelo de [**malha**](mesh.md) para definir as faces de uma malha.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="a2c9a-106">Cada elemento da matriz nFaceVertexIndices faz referência a um vértice de malha usado para criar a face.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="a2c9a-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="a2c9a-107">Where:</span></span>

-   <span data-ttu-id="a2c9a-108">nFaceVertexIndices-número de índices.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="a2c9a-109">array DWORD faceVertexIndices \[ nFaceVertexIndices \] -matriz de índices.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2c9a-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2c9a-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c9a-111">Modelos</span><span class="sxs-lookup"><span data-stu-id="a2c9a-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



