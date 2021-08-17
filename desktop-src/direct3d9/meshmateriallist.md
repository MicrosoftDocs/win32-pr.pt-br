---
description: Usado em um objeto de malha para especificar qual material se aplica a quais rostos. O membro nMaterials especifica quantos materiais estão presentes e os materiais especificam qual material aplicar.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ef1d200e5f6a6913f996c186e121a8390de01e8f3347b6dcbaeac8eeefa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798782"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Usado em um objeto de malha para especificar qual material se aplica a quais rostos. O membro nMaterials especifica quantos materiais estão presentes e os materiais especificam qual material aplicar.

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

-   nMaterials – A DWORD. O número de materiais.
-   nFaceIndexes – A DWORD. O número de índices.
-   faceIndexes \[ nFaceIndexes \] – uma matriz de DWORDs que contém os índices de face.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



