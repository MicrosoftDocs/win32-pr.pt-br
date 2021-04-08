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
# <a name="meshface"></a>MeshFace

Usado pelo modelo de [**malha**](mesh.md) para definir as faces de uma malha. Cada elemento da matriz nFaceVertexIndices faz referência a um vértice de malha usado para criar a face.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Em que:

-   nFaceVertexIndices-número de índices.
-   array DWORD faceVertexIndices \[ nFaceVertexIndices \] -matriz de índices.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



