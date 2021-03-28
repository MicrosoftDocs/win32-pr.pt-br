---
title: dcl_semantics (SM3-PS ASM)
description: Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084702"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>semântica de DCL \_ (SM3-PS ASM)

Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.

## <a name="syntax"></a>Syntax



|                                                   |
|---------------------------------------------------|
| \_máscara de hora de Verão da semântica DCL \[ \_ centróide \] \[ . Write \_\] |



 

Em que:

-   \_semântica: identifica o uso de dados pretendido e pode ser qualquer um dos valores em [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sem o \_ prefixo D3DDECLUSAGE). Além disso, um índice inteiro pode ser anexado à semântica para distinguir parâmetros que usam semântica semelhante.
-   \[\_[Centróide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] é um modificador de instrução opcional. Há suporte para as instruções de \_ uso do DCL que declaram os registros de entrada e as instruções de pesquisa de textura. O centróide é acrescentado sem espaço.
-   DST: registro de destino. Consulte [registros do PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   \_máscara de gravação: o mesmo registro de saída pode ser declarado várias vezes, cada vez com uma máscara de gravação exclusiva (de modo que uma semântica diferente pode ser aplicada a componentes individuais). No entanto, a mesma semântica não pode ser usada várias vezes em uma declaração. Isso significa que os vetores devem ter quatro componentes ou menos, e não podem passar pelos limites de registro de quatro componentes (registros de saída individuais). Quando a \_ semântica psize é usada, ela deve ter uma máscara de gravação completa porque é considerada uma escalar. Quando a \_ semântica de posição é usada, ela deve ter uma máscara de gravação completa porque todos os quatro componentes precisam ser escritos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| uso de DCL \_            |      |      |      |      |      |      |       | x    | x     |



 

Todas as \_ instruções de uso de DCL devem aparecer antes da primeira instrução executável.

## <a name="declaration-examples"></a>Exemplos de declaração


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Exemplo de antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 