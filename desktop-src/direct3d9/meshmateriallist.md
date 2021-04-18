---
description: Usado em um objeto de malha para especificar qual material se aplica a quais faces. O membro nMaterials especifica quantos materiais estão presentes e os materiais especificam qual material deve ser aplicado.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105798187"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Usado em um objeto de malha para especificar qual material se aplica a quais faces. O membro nMaterials especifica quantos materiais estão presentes e os materiais especificam qual material deve ser aplicado.

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

Em que:

-   nMaterials-um DWORD. O número de materiais.
-   nFaceIndexes-um DWORD. O número de índices.
-   faceIndexes \[ nFaceIndexes \] – uma matriz de DWORDs que contém os índices de face.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



