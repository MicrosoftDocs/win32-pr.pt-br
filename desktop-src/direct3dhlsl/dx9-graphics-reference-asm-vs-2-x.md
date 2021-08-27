---
title: vs_2_x
description: Saiba mais vs_2_x, um sombreador de vértice programável, que é feito de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a412c7980ef12bfd8814933cd9d3de07db27fac353a636406e96e1377cd57829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023966"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Um sombreador de vértice programável é feito de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora do ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

A versão do sombreador de vértice \_ versus 2 x estende o conjunto de recursos com suporte em \_ \_ versus \_ 2 0. Cada recurso adicional é representado por um limite correspondente na estrutura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) em [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps). Para usar qualquer um dos recursos aprimorados representados por esses limites, a versão do sombreador de vértice deve ser especificada como \_ vs. 2 \_ x.

-   [Instruções – vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contém uma lista das instruções disponíveis.
-   [Registros – vs \_ 2 \_ x lista](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) os diferentes tipos de registros usados pelo ALU do sombreador de vértice.
-   [Modificadores de registro de sombreador de](dx9-graphics-reference-asm-vs-registers-modifiers.md) vértice são usados para modificar a maneira como uma instrução funciona.
-   [Modificadores de Registro de Origem do Sombreador de Vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da instrução ser executado.
-   [O Swizzling do Registro de Origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.
-   [O Mascaramento do Registro de](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) Destino determina quais componentes do registro de destino são gravados.

## <a name="new-features"></a>Novos recursos

Os novos recursos são os seguinte:

### <a name="dynamic-flow-control"></a>Controle Flow dinâmico

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, há suporte para as seguintes instruções de controle de fluxo dinâmico:

-   [if \_ comp - vs](if-comp---vs.md)
-   [break - vs](break---vs.md)
-   [break \_ comp – vs](break-comp---vs.md)

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) também estiver definido, há suporte para as seguintes instruções adicionais de controle de fluxo:

-   [setp \_ comp - vs](setp-comp---vs.md)
-   [se pred - vs](if-pred---vs.md)
-   [callnz pred – vs](callnz-pred---vs.md)
-   [breakp – vs](breakp---vs.md)

O intervalo de valores para a profundidade do controle de fluxo dinâmico é de 0 a 24 e é igual à profundidade de aninhamento das instruções de controle de fluxo dinâmico (consulte [limites](dx9-graphics-reference-asm-vs-instructions-flow-control.md) de aninhamento de controle Flow para obter detalhes). Se esse limite for zero, o dispositivo não dá suporte a instruções de controle de fluxo dinâmico.

### <a name="number-of-temporary-registers"></a>Número de registros temporários

[D3DVS20CAPS representa](/windows/desktop/direct3d9/d3dvs20caps) o número de Registros [Temporários](dx9-graphics-reference-asm-vs-registers-temporary.md)com suporte pelo dispositivo. O intervalo de valores para esse limite é de 12 a 32.

### <a name="static-flow-control-nesting-depth"></a>Profundidade de aninhamento Flow controle estático

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa a profundidade de aninhamento de dois tipos de instruções de controle de fluxo estático: [loop - vs](loop---vs.md)rep - vs e chamada - vs callnz bool - vs se bool - vs . loop - vs/rep - as instruções podem ser aninhadas até / [](rep---vs.md) [](call---vs.md) / [](callnz-bool---vs.md) / [](if-bool---vs.md)D3DVS20CAPS de profundidade. Independentemente, chamar – vs/callnz bool – versus instruções podem ser aninhadas até D3DVS20CAPS de profundidade. Se D3DVS20CAPS também estiver definido, [callnz pred –](callnz-pred---vs.md) vs será contado em direção à profundidade de aninhamento da chamada – vs/callnz bool – vs/if bool – vs (consulte limites de aninhamento de controle do [Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes).

### <a name="predication"></a>Predicação

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) estiver definido, o dispositivo será compatível [com a predicação setp \_ comp - vs](setp-comp---vs.md) e de instrução. Se D3DVS20CAPS também for maior que 0, as seguintes instruções adicionais de controle de fluxo dinâmico serão suportadas:

-   [se pred - vs](if-pred---vs.md)
-   [callnz pred – vs](callnz-pred---vs.md)
-   [breakp – vs](breakp---vs.md)

### <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de vértice pode ter até 256 instruções armazenadas. O número de instruções executados pode ser muito maior (devido ao suporte de loop/rep) e é limitado por [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), que deve ser pelo menos 0xFFFF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 