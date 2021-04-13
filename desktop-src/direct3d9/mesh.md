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
# <a name="mesh"></a>Malha

Define uma malha simples. A primeira matriz é uma lista de vértices, e a segunda matriz define as faces da malha indexando na matriz de vértice.

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

Em que:

-   nVertices-número de vértices.
-   vértices \[ de vetor de matriz nVertices \] -matriz de vértices, cada um do tipo Vector. Consulte [**vector**](vector.md).
-   nFaces-número de rostos.
-   matriz MeshFace faces \[ nFaces \] – matriz de rostos, cada um do tipo MeshFace. Consulte [**MeshFace**](meshface.md).
-   \[ ... \] -Qualquer modelo de arquivo. x pode ser usado aqui. Isso torna a arquitetura extensível. Os modelos [**material**](material.md) e [**TextureFilename**](texturefilename.md) normalmente são usados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



