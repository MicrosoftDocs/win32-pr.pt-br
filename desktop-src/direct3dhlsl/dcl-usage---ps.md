---
title: dcl_semantics (sm3 – ps asm)
description: Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91a57ec2eabbef2cd62fec8fa95fbf9d2da47a5bfcdb339bf30ed8da5b11c9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792925"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>\_semântica dcl (sm3 – ps asm)

Declare a associação entre a saída do sombreador de vértice e a entrada do sombreador de pixel.

## <a name="syntax"></a>Sintaxe

dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]



 

Em que:

-   \_semantics: identifica o uso de dados pretendido e pode ser qualquer um dos valores em [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sem o prefixo D3DDECLUSAGE). \_ Além disso, um índice inteiro pode ser anexado à semântica para distinguir parâmetros que usam semântica semelhante.
-   \[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] é um modificador de instrução opcional. Há suporte para ele nas instruções de uso dcl que declaram os registros de entrada e as instruções de \_ lookup de textura. O centroide é anexado sem espaço.
-   dst: registro de destino. Consulte [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   máscara de gravação: o mesmo registro de saída pode ser declarado várias vezes, cada vez com uma máscara de gravação exclusiva (para que uma semântica diferente possa ser \_ aplicada a componentes individuais). No entanto, a mesma semântica não pode ser usada várias vezes em uma declaração. Isso significa que os vetores devem ser quatro componentes ou menos e não podem passar pelos limites de registro de quatro componentes (registros de saída individuais). Quando a \_ semântica de psize é usada, ela deve ter uma máscara de gravação completa porque é considerada escalar. Quando a \_ semântica de posição é usada, ela deve ter máscara de gravação completa porque todos os quatro componentes devem ser gravados.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| uso \_ de dcl            |      |      |      |      |      |      |       | x    | x     |



 

Todas as instruções de uso de dcl \_ devem aparecer antes da primeira instrução executável.

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

 

 
