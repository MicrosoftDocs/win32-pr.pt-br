---
description: Usado pelo modelo de Malha para definir os rostos de uma malha. Cada elemento da matriz nFaceVertexIndices faz referência a um vértice de malha usado para criar o rosto.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563526"
---
# <a name="meshface"></a>MeshFace

Usado pelo modelo [**de**](mesh.md) Malha para definir os rostos de uma malha. Cada elemento da matriz nFaceVertexIndices faz referência a um vértice de malha usado para criar o rosto.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Em que:

-   nFaceVertexIndices – número de índices.
-   array DWORD faceVertexIndices \[ nFaceVertexIndices \] – Matriz de índices.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



