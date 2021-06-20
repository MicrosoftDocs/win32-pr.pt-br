---
description: PatchMesh9 define uma malha definida por patches Bézier, incluindo uma lista de vértices e os patches da malha indexando na matriz de vértices.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404699"
---
# <a name="patchmesh9"></a>PatchMesh9

Define uma malha definida por patches Bézier. A primeira matriz é uma lista de vértices e a segunda matriz define os patches da malha indexando na matriz de vértices.

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

-   Tipo – Patch de tipo de malha: retângulo, triângulo ou N-patch.
-   Grau – grau das variáveis na equação de curva.
-   Base – tipo de base de uma superfície de patch de alta ordem.
-   nVertices – número de vértices.
-   vértices \[ nVertices \] – matriz de vértices. Consulte [**Vetor**](vector.md).
-   nPatches – número de patches.
-   patches \[ nPatches \] – matriz de patches. Consulte [**Patch**](patch.md).
-   \[ ... \] - Qualquer modelo de arquivo .x pode ser usado aqui. Isso torna a arquitetura extensível.

Os patches usam os vértices na matriz de vértices como os pontos de controle para cada patch.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



