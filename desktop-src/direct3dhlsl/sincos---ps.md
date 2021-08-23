---
title: Sincos-PS
description: Computa seno e cosseno em radianos. | Sincos-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95f61c3a1cfc15f699e0e637dce8d58b9517ffe58ef36e529ec297661bff6a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671566"
---
# <a name="sincos---ps"></a>Sincos-PS

Computa seno e cosseno em radianos.

## <a name="syntax"></a>Syntax

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x



| Sincos DST. w.x.y.|Iar|XY}, src0. w.x.y.|Iar|z|w}, src1, src2 |
|------------------------------------------------------|



 

Em que:

-   o DST é o registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.
-   src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} é o swizzle de replicação necessário.
-   src1 e src2 são registros de origem e devem ser dois s de [registro float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)diferente (c \# ). Os valores de src1 e src2 devem ser das macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0



| Sincos DST. w.x.y.|Iar|XY}, src0. w.x.y.|Iar|z|Mostrar |
|------------------------------------------|



 

Em que:

-   o DST é um registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.
-   src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} é o swizzle de replicação necessário.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sincos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

Para \_ o PS 2 \_ 0 e o PS \_ 2 \_ x, Sincos pode ser usado com predicação, mas com uma restrição para o swizzle do [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): somente replicar swizzle (. x. \| y \| . z \| . w) é permitido.

Para \_ o PS 2 \_ 0 e \_ o PS 2 \_ x, a instrução funciona da seguinte maneira (V = o valor escalar de src0 com um swizzle replicate):

-   Se a máscara de gravação for. x:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. XY:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Para o PS \_ 3 \_ 0, Sincos pode ser usado com predicação sem nenhuma restrição. Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).

Para \_ o PS 3 \_ 0, a instrução funciona da seguinte maneira (V = o valor escalar de src0 com um swizzle de replicação):

-   Se a máscara de gravação for. x:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. XY:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

O aplicativo pode mapear um ângulo arbitrário (em radianos) para o intervalo \[ -PI, + PI \] usando o pseudocódigo de sombreador a seguir:


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
