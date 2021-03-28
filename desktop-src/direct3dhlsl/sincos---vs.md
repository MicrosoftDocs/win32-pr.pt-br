---
title: Sincos-vs
description: Computa seno e cosseno em radianos. | Sincos-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930476"
---
# <a name="sincos---vs"></a>Sincos-vs

Computa seno e cosseno em radianos.

## <a name="syntax"></a>Syntax

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 e vs \_ 2 \_ x



| Sincos DST. w.x.y.|Iar|XY}, src0. w.x.y.|Iar|z|w}, src1, src2 |
|------------------------------------------------------|



 

Em que:

-   o DST é o registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.
-   src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} é o swizzle de replicação necessário.
-   src1 e src2 são registradores de origem e devem ser dois registros de [flutuação de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) diferente (c \# ). Os valores de src1 e src2 devem ser das macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| Sincos DST. w.x.y.|Iar|XY}, src0. w.x.y.|Iar|z|Mostrar |
|------------------------------------------|



 

Em que:

-   o DST é um registro de destino e precisa ser um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). O registro de destino deve ter exatamente uma das três seguintes máscaras:. x \| . y \| . XY.
-   src0 é um registro de origem que fornece o ângulo de entrada, que deve estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} é o swizzle de replicação necessário.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| sincos                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>Comentários sobre o vs \_ 2 \_ e o vs \_ 2 \_ x

Para vs \_ 2 \_ 0 e vs \_ 2 \_ x, Sincos pode ser usado com predicação, mas com uma restrição para o swizzle do [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): somente replicar swizzle (. x. \| y \| . z \| . w) é permitido.

Para vs \_ 2 \_ 0 e vs \_ 2 \_ x, a instrução opera da seguinte maneira: (V = o valor escalar de src0 com um swizzle replicate):

-   Se a máscara de gravação for. x:
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. XY:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>vs \_ 3 \_ 0 comentários

Para o vs \_ 3 \_ 0, Sincos pode ser usado com predicação sem nenhuma restrição. Consulte [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).

Para \_ o vs 3 \_ 0, a instrução opera da seguinte maneira: (V = o valor escalar de src0 com um swizzle de replicação)

-   Se a máscara de gravação for. x:
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Se a máscara de gravação for. XY:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
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

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
