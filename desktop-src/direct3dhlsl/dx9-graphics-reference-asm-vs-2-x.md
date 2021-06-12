---
title: vs_2_x
description: Saiba mais sobre vs_2_x, um sombreador de vértice programável, que é composto de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010710"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

A versão do sombreador de vértice vs \_ 2 \_ x estende o conjunto de recursos com suporte do vs \_ 2 \_ 0. Cada recurso adicional é representado por uma Cap correspondente na estrutura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dentro de [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps). Para usar qualquer um dos recursos aprimorados representados por esses limites, a versão do sombreador de vértice deve ser especificada como vs \_ 2 \_ x.

-   [Instruções – vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contém uma lista das instruções disponíveis.
-   [Registros-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.
-   Os [modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md) são usados para modificar a maneira como uma instrução funciona.
-   [Modificadores de registro de origem do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.
-   [O Swizzling de registro de origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.
-   O [mascaramento do registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quais componentes do registro de destino são gravados.

## <a name="new-features"></a>Novos recursos

Os novos recursos são os seguintes:

### <a name="dynamic-flow-control"></a>Controle de fluxo dinâmico

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, as instruções de controle de fluxo dinâmico a seguir têm suporte:

-   [Se \_ comp-vs](if-comp---vs.md)
-   [interrupção vs](break---vs.md)
-   [interromper \_ comp-vs](break-comp---vs.md)

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) também for definido, as seguintes instruções adicionais de controle de fluxo têm suporte:

-   [setp \_ comp-vs](setp-comp---vs.md)
-   [se Pred-vs](if-pred---vs.md)
-   [callnz Pred – vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

O intervalo de valores para a profundidade do controle de fluxo dinâmico é de 0 a 24 e é igual à profundidade de aninhamento das instruções de controle de fluxo dinâmico (consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes). Se esse limite for zero, o dispositivo não oferecerá suporte a instruções de controle de fluxo dinâmico.

### <a name="number-of-temporary-registers"></a>Número de registros temporários

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa o número de s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)com suporte no dispositivo. O intervalo de valores para esse limite é de 12 a 32.

### <a name="static-flow-control-nesting-depth"></a>Profundidade de aninhamento de controle de fluxo estático

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa a profundidade de aninhamento de dois tipos de instruções de controle de fluxo estático: [loop-](loop---vs.md)vs e Call-vs-vs / [](rep---vs.md) [](call---vs.md) / [callnz bool-](callnz-bool---vs.md)vs / [se bool-vs](if-bool---vs.md). loop-vs/Rep-vs as instruções podem ser aninhadas até D3DVS20CAPS Deep. Independentemente, as instruções de Call-vs/callnz bool-vs podem ser aninhadas até D3DVS20CAPS Deep. Se D3DVS20CAPS também for definido, [callnz Pred-vs](callnz-pred---vs.md) será contado em direção à profundidade de aninhamento de Call-vs/callnz bool-vs/If bool-vs (consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes).

### <a name="predication"></a>Predicação

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) for definido, o dispositivo dará suporte a [setp \_ comp-vs](setp-comp---vs.md) e predicação de instrução. Se D3DVS20CAPS também for maior que 0, as instruções de controle de fluxo dinâmico adicionais a seguir têm suporte:

-   [se Pred-vs](if-pred---vs.md)
-   [callnz Pred – vs](callnz-pred---vs.md)
-   [breakp-vs](breakp---vs.md)

### <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de vértice pode ter até 256 instruções armazenadas. O número de instruções executadas pode ser muito maior (devido ao suporte de loop/Rep) e é limitado por [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), que deve ser pelo menos 0xFFFF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 