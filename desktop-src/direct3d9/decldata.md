---
description: Descreve uma declaração de vértice.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5686e3344e4642483490c9bd2892cbc92ade290567107b702cc9c56ff351c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803231"
---
# <a name="decldata"></a>DeclData

Descreve uma declaração de vértice.

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Em que:

-   nElements-número de elementos de declaração de vértice.
-   Elements \[ nElements \] -matriz de elementos de declaração de vértice.
-   nDWords-número de DWORDs.
-   Data \[ nDWords \] -matriz de DWORDs que contêm os dados em cada elemento Vertex.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



