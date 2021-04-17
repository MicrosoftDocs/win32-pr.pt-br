---
description: Define uma malha definida por patches de Bézier. A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105811394"
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

 

 



