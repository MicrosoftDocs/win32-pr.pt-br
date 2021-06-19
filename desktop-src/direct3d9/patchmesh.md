---
description: PatchMesh define uma malha definida por patches bézier, incluindo uma lista de vértices e os patches para a malha indexando na matriz de vértices.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404709"
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

 

 



