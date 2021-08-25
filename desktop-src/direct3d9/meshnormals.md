---
description: Define normais para uma malha.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02a261dd8dbd46cf26116657b983eca4f693603869a80bf2fb110c0f165221ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846456"
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

 

 



