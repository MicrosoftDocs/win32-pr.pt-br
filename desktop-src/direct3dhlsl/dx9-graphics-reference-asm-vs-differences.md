---
title: Diferenças do sombreador de vértice
description: Diferenças do sombreador de vértice
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 411a3a742fca508839651d56912fa00b2a6d8b82908b159694a3b1eff88f2318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982816"
---
# <a name="vertex-shader-differences"></a>Diferenças do sombreador de vértice

## <a name="instruction-slots"></a>Slots de instrução

Cada versão dá suporte a um número diferente de slots de instrução máximos.



| Versão  | Número máximo de slots de instrução                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | Mínimo de 512 e até o número de slots em D3DCAPS9. MaxVertexShader30InstructionSlots. Consulte [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Para obter informações sobre as limitações dos sombreadores de software, consulte [Sombreadores de software](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Flow Limites de aninhamento de controle

-   Consulte [Flow limites de aninhamento de controle.](dx9-graphics-reference-asm-vs-instructions-flow-control.md)

## <a name="vs_1_1-features"></a>Recursos \_ vs \_ 1 1

Novas instruções:

Consulte [Instruções – \_ versus 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Novos registros:

Consulte [Registros – vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>Recursos \_ vs \_ 2 0

Novos recursos:

-   Controle de fluxo estático
-   Todos os quatro [componentes](dx9-graphics-reference-asm-vs-registers-address.md) do Registro de Endereço (a0) estão disponíveis.

Novas instruções:

-   Instruções de instalação – [defb – versus](defb---vs.md), [defi – vs](defi---vs.md)
-   Instruções aritméticas - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), mova - [vs](mova---vs.md), [nrm - vs](nrm---vs.md), pow - [vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)
-   Instruções de controle de fluxo estático - call [- vs](call---vs.md), [callnz bool -](callnz-bool---vs.md)vs , else [-](else---vs.md)vs , [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), se [bool - vs](if-bool---vs.md), label - [vs](label---vs.md), loop [- vs](loop---vs.md), rep - [vs](rep---vs.md), [ret - vs](ret---vs.md)

Novos registros:

-   [Constante registro booliana](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)

## <a name="vs_2_x-features"></a>versus \_ 2 \_ x recursos

Novos recursos (D3DCAPS9. VS20Caps:

-   Controle de fluxo dinâmico
-   Aninhamento para instruções de controle de fluxo dinâmico e estático
-   Número de [Registros Temporários](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r \# ) aumentado
-   Predicação

Novas instruções:

-   Instruções de controle de fluxo dinâmico - [break - vs](break---vs.md), break comp - [ \_ vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), if comp - [ \_ vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp comp - \_ vs](setp-comp---vs.md)

Novos registros:

-   [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)

## <a name="vs_3_0-features"></a>versus \_ 3 \_ 0 Recursos

Novos recursos:

-   Lookup de textura
-   Registros de [saída indexáveis](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )
-   Número de [Registros Temporários](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r \# ) aumentado para 32

Novas instruções:

-   Instrução de instalação – [dcl \_ samplerType (sm3 – vs asm)](dcl-samplertype---vs.md)
-   Instrução de textura [– texldl – vs](texldl---vs.md)

Novos registros:

-   [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 