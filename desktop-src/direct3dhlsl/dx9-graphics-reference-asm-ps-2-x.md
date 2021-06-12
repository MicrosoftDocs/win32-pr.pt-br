---
title: ps_2_x
description: Saiba mais sobre o ps_2_x, um sombreador de pixel programável, que é composto de um conjunto de instruções que operam em dados de pixel.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010869"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [as \_ instruções do PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contêm uma lista das instruções disponíveis.
-   [os \_ registros PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.
-   A [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quais componentes do registro de destino são gravados.
-   [Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.
-   [O Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.

## <a name="dynamic-flow-control"></a>Controle de fluxo dinâmico

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa a profundidade de aninhamento das instruções de controle de fluxo dinâmico: [If](if-bool---ps.md), If [ \_ comp](if-comp---ps.md), [If \_ Pred](if-pred---ps.md), [Break-PS](break---ps.md)e [Break \_ comp-PS](break-comp---ps.md). O valor é igual à profundidade de aninhamento do bloco If \_ comp. Se esse limite for zero, o dispositivo não oferecerá suporte a instruções de controle de fluxo dinâmico.

## <a name="number-of-temporary-registers"></a>Número de registros temporários

O número de registros temporários com suporte pelo dispositivo. O intervalo é de 12 a 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidade de aninhamento de controle de fluxo estático

[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa a profundidade de aninhamento de dois tipos de instruções de controle de fluxo estático: Rep- [loop](loop---ps.md)  / [](rep---ps.md) e [chamar](call---ps.md)  / [callnz](callnz-bool---ps.md). instruções de/rep de loop podem ser aninhadas até **StaticFlowControlDepth** de profundidade. Independentemente, as instruções Call/callnz podem ser aninhadas até **StaticFlowControlDepth** Deep.

## <a name="number-of-instruction-slots"></a>Número de Slots de instrução

O número de Slots de instrução pode variar de 96 para um máximo de 512 e é especificado pelo [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0). O número total de instruções que podem ser executadas é definido por **MaxPixelShaderInstructionsExecuted**. Isso pode ser maior do que o número de Slots de instrução devido a chamadas de loop e sub-rotina.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrário

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, o swizzle arbitrário terá suporte. Consulte [registro de origem Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instruções de gradiente

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, as instruções de gradiente serão suportadas. Consulte [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)e [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Predicação

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ predicação**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, a instrução predicação terá suporte. Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite de leitura dependente

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, não haverá nenhum limite de leitura dependente.

## <a name="texture-instruction-limit"></a>Limite de instrução de textura

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, não haverá limite para instruções de textura.

## <a name="sampler-count"></a>Contagem de amostras

O número de amostragens de textura disponíveis é 16.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 