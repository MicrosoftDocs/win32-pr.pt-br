---
title: Diferenças de sombreador de pixel
description: Diferenças de sombreador de pixel
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366201"
---
# <a name="pixel-shader-differences"></a>Diferenças de sombreador de pixel

## <a name="instruction-slots"></a>Slots de instrução

Cada versão dá suporte a um número diferente de Slots de instrução máximos.



| Versão  | Número máximo de Slots de instrução                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| PS \_ 1 \_ 1 | 4 texturas aritméticas + 8                                                                                              |
| PS \_ 1 \_ 2 | 4 texturas aritméticas + 8                                                                                              |
| PS \_ 1 \_ 3 | 4 texturas aritméticas + 8                                                                                              |
| PS \_ 1 \_ 4 | 6 texturas + 8 aritméticas por fase                                                                                    |
| PS \_ 2 \_ 0 | 32 textura + aritmética de 64                                                                                            |
| PS \_ 2 \_ x | mínimo de 96 e até o número de Slots em D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots. Consulte D3DPSHADERCAPS2 \_ 0. |
| PS \_ 3 \_ 0 | mínimo de 512 e até o número de Slots em D3DCAPS9. MaxPixelShader30InstructionSlots. Consulte D3DPSHADERCAPS2 \_ 0.      |



 

Para obter informações sobre as limitações de sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Limites de aninhamento de controle de fluxo

-   Consulte [limitações de controle de fluxo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>\_recursos PS 1 \_ x

Novas instruções:

Consulte [ \_ \_ as instruções PS 1 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).

Novos registros:

Consulte [PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="ps_2_0-features"></a>Recursos do PS \_ 2 \_ 0

Novos recursos:

-   Três novas swizzles-. yzxw,. zxyw,. wzyx
-   Número de [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) aumentado para 12
-   Número de registros de [registro float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) aumentado para 32
-   Número de s (t) [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# aumentado para 8

Novas instruções:

-   Instruções de instalação- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ SampleType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)
-   Instruções aritméticas [-ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [FRC-PS](frc---ps.md), [log-PS](log---ps.md), [M3X2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md), [m4x4-](m4x4---ps.md)PS, [Max-](max---ps.md)PS, [min-PS](min---ps.md), [NRM-PS](nrm---ps.md), [pow-PS](pow---ps.md), [rcp-PS](rcp---ps.md), [RSQ-PS](rsq---ps.md), [Sincos-PS](sincos---ps.md)
-   Instruções de textura- [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md) (sintaxe diferente), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)

Novos registros:

-   [Amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )

## <a name="ps_2_x-features"></a>Recursos do PS \_ 2 \_ x

Novos recursos (consulte [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):

-   Controle de fluxo dinâmico
-   Controle de fluxo estático
-   Aninhamento de instruções de controle de fluxo dinâmicos e estáticas
-   Número de s de [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) aumentado
-   Swizzle de origem arbitrária
-   Instruções de gradiente
-   Predicação
-   Nenhum limite de leitura de textura dependente
-   Nenhum limite de instrução de textura

Novas instruções:

-   Instruções de controle de fluxo estático- [se bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [Rep-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [rótulo-PS](label---ps.md), [RET-PS](ret---ps.md)
-   Instruções de controle de fluxo dinâmico- [Break-PS](break---ps.md), [Break \_ comp-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz Pred-PS](callnz-pred---ps.md), [se \_ comp-PS](if-comp---ps.md), [se for Pred-PS](if-pred---ps.md), [setp \_ comp-PS](setp-comp---ps.md)
-   Instruções aritméticas- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)
-   Instrução de textura- [texldd-PS](texldd---ps.md)

Novos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)

## <a name="ps_3_0-features"></a>Recursos do PS \_ 3 \_ 0

Novos recursos:

-   10 [registros de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidados s (v \# )
-   Registro de [cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) indexável (v \# ) com o [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al)
-   Número de s de [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) aumentado para 32
-   Número de [registros float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) aumentados para 224

Novas instruções:

-   Instrução de instalação [- \_ semântica DCL (SM3-PS ASM)](dcl-usage---ps.md)
-   Instruções de fluxo estático- [loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)
-   Instrução aritmética- [Sincos-PS](sincos---ps.md) (nova sintaxe)
-   Instrução de textura- [texldl-PS](texldl---ps.md)

Novos registros:

-   [Registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Registro de posição](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)
-   [Registro facial](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 