---
description: Define normais para uma malha.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163806"
---
# <a name="meshnormals"></a><span data-ttu-id="d77e9-103">MeshNormals</span><span class="sxs-lookup"><span data-stu-id="d77e9-103">MeshNormals</span></span>

<span data-ttu-id="d77e9-104">Define normais para uma malha.</span><span class="sxs-lookup"><span data-stu-id="d77e9-104">Defines normals for a mesh.</span></span> <span data-ttu-id="d77e9-105">A primeira matriz de vetores são os próprios vetores normais, e a segunda matriz é uma matriz de índices que especifica quais normais devem ser aplicados a uma determinada face.</span><span class="sxs-lookup"><span data-stu-id="d77e9-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="d77e9-106">O valor do membro nFaceNormals deve ser igual ao número de faces em uma malha.</span><span class="sxs-lookup"><span data-stu-id="d77e9-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

<span data-ttu-id="d77e9-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="d77e9-107">Where:</span></span>

-   <span data-ttu-id="d77e9-108">nNormals-número de normais.</span><span class="sxs-lookup"><span data-stu-id="d77e9-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="d77e9-109">Vetor de matriz Normals \[ nNormals \] -matriz de Normals.</span><span class="sxs-lookup"><span data-stu-id="d77e9-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="d77e9-110">Consulte [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="d77e9-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="d77e9-111">nFaceNormals-número de normalidades de face.</span><span class="sxs-lookup"><span data-stu-id="d77e9-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="d77e9-112">array MeshFace faceNormals \[ nFaceNormals \] -array of mesh face normal.</span><span class="sxs-lookup"><span data-stu-id="d77e9-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="d77e9-113">Consulte [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="d77e9-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d77e9-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="d77e9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77e9-115">Modelos</span><span class="sxs-lookup"><span data-stu-id="d77e9-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



