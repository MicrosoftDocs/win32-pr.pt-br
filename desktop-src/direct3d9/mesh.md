---
description: Define uma malha simples. A primeira matriz é uma lista de vértices, e a segunda matriz define as faces da malha indexando na matriz de vértice.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Malha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456369"
---
# <a name="mesh"></a><span data-ttu-id="46ad1-104">Malha</span><span class="sxs-lookup"><span data-stu-id="46ad1-104">Mesh</span></span>

<span data-ttu-id="46ad1-105">Define uma malha simples.</span><span class="sxs-lookup"><span data-stu-id="46ad1-105">Defines a simple mesh.</span></span> <span data-ttu-id="46ad1-106">A primeira matriz é uma lista de vértices, e a segunda matriz define as faces da malha indexando na matriz de vértice.</span><span class="sxs-lookup"><span data-stu-id="46ad1-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

<span data-ttu-id="46ad1-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="46ad1-107">Where:</span></span>

-   <span data-ttu-id="46ad1-108">nVertices-número de vértices.</span><span class="sxs-lookup"><span data-stu-id="46ad1-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="46ad1-109">vértices \[ de vetor de matriz nVertices \] -matriz de vértices, cada um do tipo Vector.</span><span class="sxs-lookup"><span data-stu-id="46ad1-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="46ad1-110">Consulte [**vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="46ad1-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="46ad1-111">nFaces-número de rostos.</span><span class="sxs-lookup"><span data-stu-id="46ad1-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="46ad1-112">matriz MeshFace faces \[ nFaces \] – matriz de rostos, cada um do tipo MeshFace.</span><span class="sxs-lookup"><span data-stu-id="46ad1-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="46ad1-113">Consulte [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="46ad1-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="46ad1-114">\[ ... \] -Qualquer modelo de arquivo. x pode ser usado aqui.</span><span class="sxs-lookup"><span data-stu-id="46ad1-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="46ad1-115">Isso torna a arquitetura extensível.</span><span class="sxs-lookup"><span data-stu-id="46ad1-115">This makes the architecture extensible.</span></span> <span data-ttu-id="46ad1-116">Os modelos [**material**](material.md) e [**TextureFilename**](texturefilename.md) normalmente são usados.</span><span class="sxs-lookup"><span data-stu-id="46ad1-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="46ad1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="46ad1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ad1-118">Modelos</span><span class="sxs-lookup"><span data-stu-id="46ad1-118">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



