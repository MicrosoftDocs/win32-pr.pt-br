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
# <a name="meshnormals"></a>MeshNormals

Define normais para uma malha. A primeira matriz de vetores são os próprios vetores normais, e a segunda matriz é uma matriz de índices que especifica quais normais devem ser aplicados a uma determinada face. O valor do membro nFaceNormals deve ser igual ao número de faces em uma malha.

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

Em que:

-   nNormals-número de normais.
-   Vetor de matriz Normals \[ nNormals \] -matriz de Normals. Consulte [**vector**](vector.md).
-   nFaceNormals-número de normalidades de face.
-   array MeshFace faceNormals \[ nFaceNormals \] -array of mesh face normal. Consulte [**MeshFace**](meshface.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



