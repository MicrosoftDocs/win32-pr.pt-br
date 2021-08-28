---
title: vs_3_0
description: Saiba mais vs_3_0, um sombreador de vértice programável, que é feito de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd10f6d726118679f395f01714233c7096fd5189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476412"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Um sombreador de vértice programável é feito de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora do ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

A versão do sombreador de vértice versus 3 0 estende o conjunto de recursos \_ \_ com suporte em \_ versus 2 \_ x. Cada um dos recursos em vs 2 X que exige que um limite seja definido, está disponível em \_ \_ versus \_ \_ 3 0 sem a necessidade do limite.

-   [Instruções – vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contém uma lista das instruções disponíveis.
-   [Registros – vs \_ 3 \_ 0 lista](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) os diferentes tipos de registros usados pelo ALU do sombreador de vértice.
-   [Modificadores de registro de sombreador de](dx9-graphics-reference-asm-vs-registers-modifiers.md) vértice são usados para modificar a maneira como uma instrução funciona.
-   [Modificadores de Registro de Origem do Sombreador de Vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da instrução ser executado.
-   [O Swizzling do Registro de Origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.
-   [O Mascaramento do Registro de](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) Destino determina quais componentes do registro de destino são gravados.

## <a name="new-features"></a>Novos recursos

Novos recursos da versão do sombreador de vértice \_ \_ versus 3 0 são listados nas seções a seguir.

### <a name="indexing-registers"></a>Registros de indexação

Nos modelos de sombreador anteriores, somente o banco de registro constante poderia ser indexado. Nesse modelo, os bancos de registro a seguir podem ser indexados usando o registro do contador de loops (aL):

-   Registro de entrada (v \# )
-   Registro de saída (o \# )

### <a name="vertex-textures"></a>Texturas de vértice

Esse modelo de sombreador dá suporte à aparência de textura no sombreador de vértice usando o texldl. O mecanismo de vértice tem quatro estágios de amostra de textura (diferentes do amostrador de mapa de deslocamento e dos amostradores de textura no mecanismo de pixel) que podem ser usados para amostra de texturas definidas nesses estágios. Consulte [Texturas de vértice em vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Frequência de fluxo de vértice

Esse recurso permite que um subconjunto dos registros de entrada seja inicializado a uma taxa diferente de uma vez por vértice. Consulte [Desenhando geometria não indexada.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)

### <a name="shader-output"></a>Saída do sombreador

Semelhante a \_ 2 \_ 0, a saída do sombreador pode variar com o controle de fluxo estático. Tenha cuidado com a ramificação dinâmica, pois isso pode fazer com que as saídas do sombreador variem de acordo com o vértice. Isso produzirá resultados imprevisíveis em um hardware diferente.

### <a name="dynamic-flow-control"></a>Controle de fluxo dinâmico

Há suporte para todas as instruções de controle de fluxo dinâmico. O valor máximo de profundidade de aninhamento permitido é 24. (Consulte [Flow limites de aninhamento de controle para](dx9-graphics-reference-asm-vs-instructions-flow-control.md) obter detalhes.)

### <a name="temporary-registers"></a>Registros temporários

Há suporte para um total de 32 registros temporários \# (r).

### <a name="static-flow-control"></a>Controle Flow estático

A profundidade máxima de aninhamento para [loop – vs](loop---vs.md)rep – / [vs](rep---vs.md) é 4. A profundidade máxima de aninhamento [para chamada - vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred - vs](callnz-pred---vs.md) é 4. Para [se bool - vs](if-bool---vs.md), o valor máximo de profundidade de aninhamento permitido é 24. (Consulte [Flow limites de aninhamento de controle para](dx9-graphics-reference-asm-vs-instructions-flow-control.md) obter detalhes.)

### <a name="predication"></a>Predicação

Há suporte para a predicação de instrução. Use [setp \_ comp – vs para](setp-comp---vs.md) definir o registro de predicado.

### <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de vértice é permitido em qualquer lugar, desde 512 até o número de slots em MaxVertexShader30InstructionSlots [**em D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) O número de instruções em executar pode ser muito maior devido ao suporte de loop/rep; no entanto, isso é limitado por MaxVShaderInstructionsExecuted em D3DCAPS9, que deve ser pelo menos 0xFFFF.

### <a name="device-caps"></a>Limites do dispositivo

Se houver suporte para o Sombreador de Vértice 3 0, as seguintes maiúsculas serão suportadas no \_ hardware (no mínimo):




| Tampa | Funcionalidade | 
|-----|------------|
| Limites do sombreador | <ul><li>DynamicFlowControlDepth é 24</li><li>NumTemps é 32</li><li>StaticFlowControlDepth é 4</li><li>Há suporte para a predicação.</li></ul> | 
| GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom | 8 K | 
| VertexShaderVersion | 3_0 | 
| MaxVertexShaderConst | 256 | 
| MaxVertexShader30InstructionSlots | 512 | 
| Suporte a 10000 | D3DPRASTERCAPS_FOGVERTEX | 
| VertexTextureFilterCaps | <ul><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li></ul> | 
| <a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a> | Os elementos de vértice em uma declaração de vértice podem compartilhar o mesmo deslocamento de fluxo. | 
| Formatos de vértice | <ul><li>D3DDECLTYPE_UBYTE4</li><li>D3DDECLTYPE_UBYTE4N</li><li>D3DDECLTYPE_SHORT2N</li><li>D3DDECLTYPE_SHORT4N</li><li>D3DDECLTYPE_FLOAT16_2</li><li>D3DDECLTYPE_FLOAT16_4</li></ul> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
