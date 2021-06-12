---
title: vs_3_0
description: Saiba mais sobre vs_3_0, um sombreador de vértice programável, que é composto de um conjunto de instruções que operam em dados de vértice.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011069"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Um sombreador de vértice programável é composto de um conjunto de instruções que operam em dados de vértice. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

A versão do sombreador de vértice vs \_ 3 \_ 0 estende o conjunto de recursos com suporte do vs \_ 2 \_ x. Cada um dos recursos do vs \_ 2 \_ X que exige um limite definido, está disponível no vs \_ 3 \_ 0 sem a necessidade do limite.

-   [Instruções – vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contém uma lista das instruções disponíveis.
-   [Registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lista os diferentes tipos de registros usados pela alu do sombreador de vértice.
-   Os [modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md) são usados para modificar a maneira como uma instrução funciona.
-   [Modificadores de registro de origem do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.
-   [O Swizzling de registro de origem](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.
-   O [mascaramento do registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quais componentes do registro de destino são gravados.

## <a name="new-features"></a>Novos recursos

Os novos recursos da versão do sombreador de vértice vs \_ 3 \_ 0 estão listados nas seções a seguir.

### <a name="indexing-registers"></a>Registros de indexação

Nos modelos de sombreador anteriores, somente o banco de registro constante pode ser indexado. Nesse modelo, os seguintes bancos de registro podem ser indexados, usando o registro do contador de loop (aL):

-   Registro de entrada (v \# )
-   Registro de saída (o \# )

### <a name="vertex-textures"></a>Texturas de vértice

Este modelo de sombreador dá suporte à pesquisa de textura no sombreador de vértice usando texldl. O mecanismo de vértice tem quatro estágios de amostra de textura (distintos da amostra de mapa de deslocamento e dos exemplos de textura no mecanismo de pixel) que podem ser usados para exemplos de texturas definidas nesses estágios. Confira [texturas de vértice no vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Frequência de fluxo de vértice

Esse recurso permite que um subconjunto dos registros de entrada seja inicializado a uma taxa diferente de uma vez por vértice. Consulte [desenho de geometria não indexada](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).

### <a name="shader-output"></a>Saída de sombreador

Semelhante ao vs \_ 2 \_ 0, a saída do sombreador pode variar com o controle de fluxo estático. Tenha cuidado com a ramificação dinâmica, pois isso pode fazer com que as saídas de sombreador variem por vértice. Isso produzirá resultados imprevisíveis em hardwares diferentes.

### <a name="dynamic-flow-control"></a>Controle de fluxo dinâmico

Todas as instruções de controle de fluxo dinâmico têm suporte. O valor máximo de profundidade de aninhamento permitido é 24. (Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes.)

### <a name="temporary-registers"></a>Registros temporários

Há suporte para um total de 32 registros temporários (r \# ).

### <a name="static-flow-control"></a>Controle de fluxo estático

A profundidade máxima de aninhamento para [loop – vs](loop---vs.md) / [Rep-vs](rep---vs.md) é 4. A profundidade máxima de aninhamento para [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz Pred-vs](callnz-pred---vs.md) é 4. Para [se bool-vs](if-bool---vs.md), o valor máximo de profundidade de aninhamento permitido é 24. (Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obter detalhes.)

### <a name="predication"></a>Predicação

Há suporte para predicação de instrução. Use [setp \_ comp-vs](setp-comp---vs.md) para definir o registro de predicado.

### <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de vértice é permitido em qualquer lugar de 512 até o número de Slots em MaxVertexShader30InstructionSlots em [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). O número de instruções executadas pode ser muito maior devido ao suporte de loop/representante; no entanto, isso é limitado por MaxVShaderInstructionsExecuted no D3DCAPS9 que deve ser pelo menos 0xFFFF.

### <a name="device-caps"></a>Limites do dispositivo

Se houver \_ suporte para o sombreador de vértice 3 0, as seguintes caps têm suporte no hardware (no mínimo):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tampa</th>
<th>Funcionalidade</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Limites de sombreador</td>
<td><ul>
<li>DynamicFlowControlDepth é 24</li>
<li>NumTemps é 32</li>
<li>StaticFlowControlDepth é 4</li>
<li>Predicação tem suporte.</li>
</ul></td>
</tr>
<tr class="even">
<td>GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</td>
<td>8 K</td>
</tr>
<tr class="odd">
<td>VertexShaderVersion</td>
<td>3_0</td>
</tr>
<tr class="even">
<td>MaxVertexShaderConst</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>Suporte de neblina</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>VertexTextureFilterCaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>Os elementos de vértice em uma declaração de vértice podem compartilhar o mesmo deslocamento de fluxo.</td>
</tr>
<tr class="odd">
<td>Formatos de vértice</td>
<td><ul>
<li>D3DDECLTYPE_UBYTE4</li>
<li>D3DDECLTYPE_UBYTE4N</li>
<li>D3DDECLTYPE_SHORT2N</li>
<li>D3DDECLTYPE_SHORT4N</li>
<li>D3DDECLTYPE_FLOAT16_2</li>
<li>D3DDECLTYPE_FLOAT16_4</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de vértice](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 