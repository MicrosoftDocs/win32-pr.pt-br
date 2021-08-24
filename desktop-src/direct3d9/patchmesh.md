---
description: PatchMesh define uma malha definida por patches Bézier, incluindo uma lista de vértices e os patches para a malha indexando na matriz de vértices.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3bc3c243fb42014ba18aac134ea008d5818e249a601858be6724d5a0fd7310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746916"
---
# <a name="patchmesh"></a>PatchMesh

Define uma malha definida por patches Bézier. A primeira matriz é uma lista de vértices e a segunda matriz define os patches da malha indexando na matriz de vértices.

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

-   nVertices – número de vértices.
-   vértices \[ nVertices \] – matriz de vértices. Consulte [**Vetor**](vector.md).
-   nPatches – número de patches.
-   patches \[ nPatches \] – matriz de patches. Consulte [**Patch**](patch.md).
-   \[ ... \] - Qualquer modelo de arquivo .x pode ser usado aqui. Isso torna a arquitetura extensível.

Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch. Esse é um modelo herdado. O modelo de malha de patch mais recente [**é PatchMesh9.**](patchmesh9.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



