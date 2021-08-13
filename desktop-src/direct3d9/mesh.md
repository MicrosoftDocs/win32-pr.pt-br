---
description: Define uma malha simples. A primeira matriz é uma lista de vértices e a segunda matriz define os rostos da malha indexando na matriz de vértices.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Malha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce4cf6fb6a3eee3417a7d0fe1594164c1e22df9d118f4f995955f8070fc015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240736"
---
# <a name="mesh"></a>Malha

Define uma malha simples. A primeira matriz é uma lista de vértices e a segunda matriz define os rostos da malha indexando na matriz de vértices.

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

-   nVertices – número de vértices.
-   array Vector vértices \[ nVertices \] – Matriz de vértices, cada um do tipo Vector. Consulte [**Vetor**](vector.md).
-   nFaces – número de faces.
-   array MeshFace faces \[ nFaces \] - Matriz de faces, cada um do tipo MeshFace. Consulte [**MeshFace**](meshface.md).
-   \[ ... \] - Qualquer modelo de arquivo .x pode ser usado aqui. Isso torna a arquitetura extensível. [**Os**](material.md) modelos [**Material e TextureFilename**](texturefilename.md) normalmente são usados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



