---
title: expp-vs
description: Fornece precisão parcial exponencial 2x.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638870"
---
# <a name="expp---vs"></a>expp-vs

Fornece o exponencial de precisão parcial 2<sup>x</sup>.

## <a name="syntax"></a>Syntax



| expp DST, src. w.x.y.|Iar|z|Mostrar |
|----------------------------|



 

Em que:

-   DST é o registro de destino.
-   src é um registro de origem. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.
-   {x \| y \| z \| w} é o swizzle de replicação necessário no registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

A instrução [exp-vs](exp---vs.md) Opera de maneira diferente, dependendo das versões do sombreador de vértice.

No vs \_ 1 \_ 1, a instrução expp fornece os seguintes resultados:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



No vs \_ 2 \_ 0 e superior, a instrução expp fornece os seguintes resultados:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

No vs \_ 2 \_ 0 e superior, a instrução funciona da seguinte maneira:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



A instrução fornece pelo menos 10 bits de precisão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




