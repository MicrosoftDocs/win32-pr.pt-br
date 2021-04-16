---
description: Define uma malha definida por patches de Bézier. A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500260"
---
# <a name="patchmesh"></a>PatchMesh

Define uma malha definida por patches de Bézier. A primeira matriz é uma lista de vértices, e a segunda matriz define os patches para a malha por meio da indexação na matriz de vértice.

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

Em que:

-   nVertices-número de vértices.
-   vértices \[ nVertices \] -matriz de vértices. Consulte [**vector**](vector.md).
-   nPatches-número de patches.
-   patches \[ nPatches \] -matriz de patches. Consulte [**patch**](patch.md).
-   \[ ... \] -Qualquer modelo de arquivo. x pode ser usado aqui. Isso torna a arquitetura extensível.

Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch. Este é um modelo herdado. O modelo de malha de patch mais recente é [**PatchMesh9**](patchmesh9.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



