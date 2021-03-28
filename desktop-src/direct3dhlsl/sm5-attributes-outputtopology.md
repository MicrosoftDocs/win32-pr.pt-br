---
title: outputtopology
description: Define o tipo primitivo de saída para o Tessellator.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916877"
---
# <a name="outputtopology"></a>outputtopology

Define o tipo primitivo de saída para o Tessellator.


```
outputtopology(X)      
```



## <a name="remarks"></a>Comentários

X deve ser [**ponto**](dx-graphics-hlsl-geometry-shader.md), **linha**, **triângulo ou \_** **semiangular e deve \_ estar** entre aspas. Aqui estão as opções válidas para este atributo:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Esse atributo tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos do Shader Model 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




