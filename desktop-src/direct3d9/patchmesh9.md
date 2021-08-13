---
description: PatchMesh9 define uma malha definida por patches de Bézier, incluindo uma lista de vértices e os patches para a malha por meio da indexação na matriz de vértice.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20216bcfa33c3e3ef36dea999a6fef10384719254f4874a1da3907aa02551a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798532"
---
# <a name="patchmesh9"></a>PatchMesh9

Define uma malha definida por patches de Bézier. A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Em que:

-   Tipo de malha de patch tipo: retângulo, triângulo ou N-patch.
-   Grau-grau das variáveis na equação de curva.
-   Tipo base de uma superfície de patch de ordem superior.
-   nVertices-número de vértices.
-   vértices \[ nVertices \] -matriz de vértices. Consulte [**vector**](vector.md).
-   nPatches-número de patches.
-   patches \[ nPatches \] -matriz de patches. Consulte [**patch**](patch.md).
-   \[ ... \] -Qualquer modelo de arquivo. x pode ser usado aqui. Isso torna a arquitetura extensível.

Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



