---
title: Diferenças de sombreador de vértice
description: Diferenças de sombreador de vértice
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007679"
---
# <a name="vertex-shader-differences"></a>Diferenças de sombreador de vértice

## <a name="instruction-slots"></a>Slots de instrução

Cada versão dá suporte a um número diferente de Slots de instrução máximos.



| Versão  | Número máximo de Slots de instrução                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | mínimo de 512 e até o número de Slots em D3DCAPS9. MaxVertexShader30InstructionSlots. Consulte [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Para obter informações sobre as limitações de sombreadores de software, consulte [sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Limites de aninhamento de controle de fluxo

-   Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>vs \_ 1 \_ 1 recursos

Novas instruções:

Consulte [as instruções – vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Novos registros:

Consulte [registros-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>Recursos do vs \_ 2 \_ 0

Novos recursos:

-   Controle de fluxo estático
-   Todos os quatro componentes do [registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md) (a0) estão disponíveis.

Novas instruções:

-   Instruções de instalação- [DEFB-vs](defb---vs.md), [defi-vs](defi---vs.md)
-   Instruções aritméticas- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [mova-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [pow-vs](pow---vs.md), [sgn-vs](sgn---vs.md), [Sincos-vs](sincos---vs.md)
-   Instruções de controle de fluxo estático- [Call-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [senão-vs](else---vs.md), [endif-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [se bool-vs](if-bool---vs.md), [Label-](label---vs.md)vs, [loop](loop---vs.md)-vs, [Rep-vs](rep---vs.md), [RET-vs](ret---vs.md)

Novos registros:

-   [Registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al)

## <a name="vs_2_x-features"></a>Recursos do vs \_ 2 \_ x

Novos recursos (D3DCAPS9. VS20Caps):

-   Controle de fluxo dinâmico
-   Aninhamento de instruções de controle de fluxo dinâmicos e estáticas
-   Número de s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentado
-   Predicação

Novas instruções:

-   Instruções de controle de fluxo dinâmico- [Break-vs](break---vs.md), [Break \_ comp-vs](break-comp---vs.md), [breakp-vs](breakp---vs.md), [callnz Pred-vs](callnz-pred---vs.md), [se \_ comp-vs](if-comp---vs.md), [se Pred-vs](if-pred---vs.md), [setp \_ comp-vs](setp-comp---vs.md)

Novos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)

## <a name="vs_3_0-features"></a>Recursos do vs \_ 3 \_ 0

Novos recursos:

-   Pesquisa de textura
-   Registros de [saída](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indexáveis (o \# )
-   Número de s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) aumentado para 32

Novas instruções:

-   Instrução de instalação [- \_ defaultsampletype (SM3-vs ASM)](dcl-samplertype---vs.md)
-   Instrução de textura- [texldl-vs](texldl---vs.md)

Novos registros:

-   [Amostra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 