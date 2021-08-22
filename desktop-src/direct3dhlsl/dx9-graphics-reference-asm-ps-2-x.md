---
title: ps_2_x
description: Saiba mais ps_2_x, um sombreador de pixel programável, que é feito de um conjunto de instruções que operam em dados de pixel.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37bc9709effeb865651ca920a155094946b88753586174ecf6e1ab06eabd2fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489406"
---
# <a name="ps_2_x"></a>ps \_ 2 \_ x

Um sombreador de pixel programável é feito de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora do ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [Ps \_ 2 \_ x Instruções](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contém uma lista das instruções disponíveis.
-   [ps \_ 2 \_ x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lista os diferentes tipos de registros usados pelo ALU do sombreador de vértice.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.
-   [A Máscara de Gravação do Registro de](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) Destino determina quais componentes do registro de destino são gravados.
-   [Modificadores de Registro de Origem do Sombreador de Pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados do registro de origem antes da instrução ser executado.
-   [O Swizzling do Registro de Origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.

## <a name="dynamic-flow-control"></a>Controle Flow dinâmico

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa a profundidade de aninhamento das instruções de controle de fluxo [dinâmico:](if-bool---ps.md)se , se [ \_ comp](if-comp---ps.md), se [ \_ pred](if-pred---ps.md), [break - ps](break---ps.md)e [break comp - \_ ps](break-comp---ps.md). O valor é igual à profundidade de aninhamento do bloco se \_ comp. Se esse limite for zero, o dispositivo não dá suporte a instruções de controle de fluxo dinâmico.

## <a name="number-of-temporary-registers"></a>Número de registros temporários

O número de registros temporários com suporte pelo dispositivo. O intervalo é de 12 a 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidade de aninhamento Flow controle estático

[**StaticFlowControlDepth representa**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) a profundidade de aninhamento de dois tipos de instruções de controle de fluxo estático: [loop](loop---ps.md)  / [rep](rep---ps.md) e [](call---ps.md)  / [callnz .](callnz-bool---ps.md) As instruções de loop /rep podem ser aninhadas até **StaticFlowControlDepth** profunda. Independentemente, as instruções call /callnz podem ser aninhadas até **StaticFlowControlDepth** profunda.

## <a name="number-of-instruction-slots"></a>Número de slots de instrução

O número de slots de instrução pode variar de 96 a um máximo de 512 e é especificado pelo [**MaxPixelShaderInstructionSlots.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) O número total de instruções que podem ser executados é definido por **MaxPixelShaderInstructionsExecuted.** Isso pode ser maior que o número de slots de instrução devido a looping e chamadas de sub-rotina.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrário

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) estiver definido, há suporte para swizzle arbitrário. Consulte [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instruções de gradiente

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) estiver definido, há suporte para instruções de gradiente. Consulte [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)e [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Predicação

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, há suporte para a predicação de instrução. Consulte [Registro de predicado.](dx9-graphics-reference-asm-ps-registers-predicate.md)

## <a name="dependent-read-limit"></a>Limite de leitura dependente

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) estiver definido, não haverá limites de leitura dependentes.

## <a name="texture-instruction-limit"></a>Limite de instrução de textura

Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) estiver definido, não haverá limite nas instruções de textura.

## <a name="sampler-count"></a>Contagem de amostras

O número de amostras de textura disponíveis é 16.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 