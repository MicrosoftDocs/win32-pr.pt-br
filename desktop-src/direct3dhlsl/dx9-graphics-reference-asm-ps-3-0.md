---
title: ps_3_0
description: Saiba mais sobre o ps_3_0, um sombreador de pixel programável, que é composto de um conjunto de instruções que operam em dados de pixel.
ms.assetid: 3eabf173-9d9d-45b2-bc30-de857428f3ee
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79145936709e43fab9b87602233225567a0067528a31036aacc11c5b425c0dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512885"
---
# <a name="ps_3_0"></a>PS \_ 3 \_ 0

Um sombreador de pixel programável é composto de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora da ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [as \_ instruções do PS 3 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) contêm uma lista das instruções disponíveis.
-   [os \_ registros do PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) listam os diferentes tipos de registros usados pela alu do sombreador de pixel.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.
-   A [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quais componentes do registro de destino são gravados.
-   [Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados de registro de origem antes da execução da instrução.
-   [O Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.

## <a name="new-features"></a>Novos recursos

Adicione um registro facial. Adicione um registro de posição. Os registros de cor (v \# ) agora são totalmente flutuantes e os registros de coordenadas de textura (t \# ) foram consolidados. As declarações de entrada usam os nomes de uso e vários usos são permitidos para os componentes de um determinado registro.

## <a name="dynamic-flow-control"></a>controle de Flow dinâmico

O dispositivo dá suporte ao controle de fluxo dinâmico ([se bool-PS](if-bool---ps.md), [Break-PS](break---ps.md)e [Break \_ comp-PS](break-comp---ps.md)). A profundidade dos intervalos de aninhamento de 0 a 24.

## <a name="number-of-temporary-registers"></a>Número de registros temporários

O número de registros temporários com suporte é 32.

## <a name="static-flow-control-nesting-depth"></a>profundidade de aninhamento de controle de Flow estático

A chamada callnz do [PS de chamada](call---ps.md) / [](callnz-bool---ps.md)  / [ \_ Pred](callnz-pred---ps.md) pode ser aninhada a uma profundidade máxima de 4. De modo independente, as instruções do PS-PS do [pt de loop](loop---ps.md) / [](rep---ps.md) podem ser aninhadas a uma profundidade máxima de 4.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrário

Há suporte para swizzle arbitrários. Consulte [registro de origem Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instruções de gradiente

Há suporte para instruções de gradiente. Consulte [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)e [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Predicação

Há suporte para predicação de instrução. Consulte [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite de leitura dependente

Não há limites de leitura dependentes.

## <a name="texture-instruction-limit"></a>Limite de instrução de textura

Não há limite para instruções de textura.

## <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de pixel é permitido em qualquer lugar de 512 até o número de Slots em MaxPixelShader30InstructionSlots (não mais de 32768). O número de instruções executadas pode ser muito maior devido ao suporte a looping. MaxPShaderInstructionsExecuted deve ser pelo menos 2 ^ 16.

## <a name="sampler-count"></a>Contagem de amostras

O número de amostragens de textura disponíveis é 16.

## <a name="device-caps"></a>Limites do dispositivo

Se \_ o PS 3 \_ 0 tiver suporte, as seguintes caps têm suporte no hardware (no mínimo):



| Tampa                                                                                                          | Valor                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4K cada                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 K                                                                                                                                                                                                                                                                                                    |
| MaxAnisotropy                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| As seguintes tampas primitivas estão definidas:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, D3DPMISCCAPS \_ CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ FOGINFVF, D3DPMISCCAPS \_ MASKZ                                                                                               |
| As seguintes Caps de rasterização estão definidas:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOTROPY, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS SCISSORTEST \_ in D3DCAPS9                                                                                                                                                                  |
| Suporte completo para ajuste de profundidade, incluindo:                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Conjunto completo de comparações para o teste de profundidade e alfa, incluindo:                                                  | Todos os D3DPCMPCAPS em D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modos de mesclagem de origem                                                                                        | Todos os modos de mesclagem têm suporte como uma origem (exceto D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA e D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Há suporte para as seguintes Caps de textura:                                                                    | D3DPTEXTURECAPS \_ CUBEMAP, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ Perspective, D3DPTEXTURECAPS \_ projetod, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, \_ D3DPTEXTURECAPS VOLUMEMAP                                                        |
| Os itens a seguir têm suporte em limites de filtro de textura, limites de filtro de textura de volume e limites de filtro de textura de cubo: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS MINFANISOTROPIC \_ (isso não é necessário para VolumeTextureFilterCaps e CUBETEXTUREFILTERCAPS), D3DPTFILTERCAPS \_ MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, \_ \_ D3DPTFILTERCAPS MAGFPOINT, D3DPTFILTERCAPS MAGFLINEAR             |
| Os seguintes modos de endereço de textura têm suporte em estágios de vértice e pixel:                                | D3DPTADDRESSCAPS \_ Wrap, \_ espelho D3DPTADDRESSCAPS, D3DPTADDRESSCAPS \_ fixe, D3DPTADDRESSCAPS \_ Border, D3DPTADDRESSCAPS INDEPENDENTUV \_ , D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Todas as tampas de sombreador de pixel têm suporte.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Há suporte para os seguintes recursos: predicação, swizzles arbitrário e instruções de gradiente. Não há nenhum limite de leitura dependente e nenhum limite na mistura de instruções de textura e matemática. |
| Todas as operações de estêncil têm suporte. Isso inclui dois estênceis de lado.                                   | Consulte [ **D3DSTENCILOP**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Tamanho do ponto de suporte do dispositivo por vértice                                                                         | D3DFVFCAPS \_ PSIZE D3DCAPS9                                                                                                                                                                                                                                                                         |
| Sem energia de 2 suporte a textura.                                                                              | Suporte completo ou não pow-2 condicional; o dispositivo não deve ter a única limitação quadrada como em D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Se o dispositivo der suporte a vários rendertargets, haverá suporte para as seguintes Caps:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Se o vs \_ 3 \_ 0 tiver suporte                                                                                     | MaxUserClipPlanes em D3DCAPS9 é 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 