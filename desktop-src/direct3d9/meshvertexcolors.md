---
description: Especifica as cores de vértice para uma malha, em vez de aplicar um material por face ou por malha.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370128"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

Especifica as cores de vértice para uma malha, em vez de aplicar um material por face ou por malha.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Em que:

-   nVertexColors-número de cores. Isso corresponde ao número de vértices na malha.
-   array IndexColor vertexColors \[ nVertexColors \] -matriz de cores indexadas. Consulte [**IndexedColor**](indexedcolor.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



