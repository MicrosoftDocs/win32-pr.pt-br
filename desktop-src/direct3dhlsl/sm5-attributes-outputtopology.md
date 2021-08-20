---
title: outputtopology
description: Define o tipo primitivo de saída para o mosaico.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d718b11c23fcf77f452e224a51439f7d6f422d3c81d5238167cbf87c7c3014a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725410"
---
# <a name="outputtopology"></a>outputtopology

Define o tipo primitivo de saída para o mosaico.


```
outputtopology(X)      
```



## <a name="remarks"></a>Comentários

X deve ser [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle \_ cw** ou **triangle \_ ccw** e deve estar entre aspas. Aqui estão as opções válidas para esse atributo:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Esse atributo tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos do modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




