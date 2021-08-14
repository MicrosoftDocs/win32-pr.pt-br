---
title: ps_3_0
description: Saiba mais ps_3_0, um sombreador de pixel programável, que é feito de um conjunto de instruções que operam em dados de pixel.
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
# <a name="ps_3_0"></a>ps \_ 3 \_ 0

Um sombreador de pixel programável é feito de um conjunto de instruções que operam em dados de pixel. Registra dados de transferência dentro e fora do ALU. Controle adicional pode ser aplicado para modificar a instrução, os resultados ou quais dados são gravados.

-   [ps \_ 3 \_ 0 Instruções](dx9-graphics-reference-asm-ps-instructions-ps-3-0.md) contém uma lista das instruções disponíveis.
-   [ps \_ 3 \_ 0 Registros lista](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) os diferentes tipos de registros usados pelo ALU do sombreador de pixel.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) São usados para modificar a maneira como uma instrução funciona.
-   [A Máscara de Gravação do Registro de](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) Destino determina quais componentes do registro de destino são gravados.
-   [Modificadores de Registro de Origem do Sombreador de Pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alteram os dados do registro de origem antes da instrução ser executado.
-   [O Swizzling do Registro de Origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornece controle adicional sobre quais componentes de registro são lidos, copiados ou gravados.

## <a name="new-features"></a>Novos recursos

Adicione um registro facial. Adicione um registro de posição. Registros de cores (v ) agora são um ponto totalmente flutuante e os registros de coordenadas de textura \# (t \# ) foram consolidados. As declarações de entrada têm os nomes de uso e vários usos são permitidos para componentes de um determinado registro.

## <a name="dynamic-flow-control"></a>Controle Flow dinâmico

O dispositivo dá suporte ao controle de fluxo dinâmico ([se bool - ps](if-bool---ps.md), [break - ps](break---ps.md)e [break comp - \_ ps](break-comp---ps.md)). A profundidade do aninhamento varia de 0 a 24.

## <a name="number-of-temporary-registers"></a>Número de registros temporários

O número de registros temporários com suporte é 32.

## <a name="static-flow-control-nesting-depth"></a>Profundidade de aninhamento Flow controle estático

A [chamada - ps](call---ps.md) / [callnz](callnz-bool---ps.md)  / [call \_ pred](callnz-pred---ps.md) pode ser aninhada a uma profundidade máxima de 4. Independentemente, [loop – ps](loop---ps.md)rep – as instruções / [ps](rep---ps.md) podem ser aninhadas a uma profundidade máxima de 4.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrário

Há suporte para swizzle arbitrário. Consulte [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Instruções de gradiente

Há suporte para instruções de gradiente. Consulte [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)e [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Predicação

Há suporte para a predicação de instrução. Consulte [Registro de predicado.](dx9-graphics-reference-asm-ps-registers-predicate.md)

## <a name="dependent-read-limit"></a>Limite de leitura dependente

Não há limites de leitura dependentes.

## <a name="texture-instruction-limit"></a>Limite de instrução de textura

Não há limite para instruções de textura.

## <a name="instruction-count"></a>Contagem de instruções

Cada sombreador de pixel é permitido em qualquer lugar, desde 512 até o número de slots em MaxPixelShader30InstructionSlots (não superior a 32768). O número de instruções em executar pode ser muito maior devido ao suporte a looping. MaxPShaderInstructionsExecuted deve ser pelo menos 2^16.

## <a name="sampler-count"></a>Contagem de amostras

O número de amostras de textura disponíveis é 16.

## <a name="device-caps"></a>Limites do dispositivo

Se há suporte para ps 3 0, há suporte para as seguintes \_ \_ maiúsculas no hardware (no mínimo):



| Tampa                                                                                                          | Valor                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MaxTextureWidth, MaxTextureHeight                                                                            | 4K cada                                                                                                                                                                                                                                                                                               |
| MaxTextureRepeat                                                                                             | 8 K                                                                                                                                                                                                                                                                                                    |
| Max Ltda                                                                                                | 16                                                                                                                                                                                                                                                                                                    |
| PixelShaderVersion                                                                                           | 3 \_ 0                                                                                                                                                                                                                                                                                                  |
| MaxPixelShader30InstructionSlots                                                                             | 512                                                                                                                                                                                                                                                                                                   |
| Os seguintes limites primitivos são definidos:                                                                        | D3DPMISCCAPS \_ BLENDOP, D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS, D3DPMISCCAPS \_ CLIPTLVERTS, D3DPMISCCAPS \_ CULLCCW, \_ D3DPMISCCAPS CULLCW, D3DPMISCCAPS \_ CULLNONE, D3DPMISCCAPS \_ BLENDINFVF, D3DPMISCCAPS \_ MASKZZ                                                                                               |
| Os seguintes limites de raster estão definidos:                                                                           | D3DPRASTERCAPS \_ MIPMAPLODBIAS, D3DPRASTERCAPS \_ ANISOLANTAY, D3DPRASTERCAPS \_ COLORPERSPECTIVE, D3DPRASTERCAPS \_ SCISSORTEST em D3DCAPS9                                                                                                                                                                  |
| Suporte completo para desvio de profundidade, incluindo:                                                                       | D3DPRASTERCAPS \_ SLOPESCALEDEPTHBIAS, D3DPRASTERCAPS \_ DEPTHBIAS                                                                                                                                                                                                                                        |
| Conjunto completo de comparações de profundidade e teste alfa, incluindo:                                                  | Todos os D3DPCMPCAPS em D3DCAPS9.                                                                                                                                                                                                                                                                      |
| Modos de mesclagem de origem                                                                                        | Todos os modos de mesclagem têm suporte como fonte (exceto D3DPBLENDCAPS \_ SRCALPHASAT, D3DPBLENDCAPS \_ BOTHSRCALPHA e D3DPBLENDCAPS \_ BOTHINVSRCALPHA).                                                                                                                                                    |
| Há suporte para as seguintes tampas de textura:                                                                    | D3DPTEXTURECAPS \_ CUBEMAP, D3DPTEXTURECAPS \_ MIPCUBEMAP, D3DPTEXTURECAPS \_ MIPMAP, D3DPTEXTURECAPS \_ MIPVOLUMEMAP, D3DPTEXTURECAPS \_ PERSPECTIVE, D3DPTEXTURECAPS \_ PROJECTED, D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE, D3DPTEXTURECAPS \_ VOLUMEMAP                                                        |
| Há suporte para os seguintes recursos em maiúsculas de filtro de textura, em maiúsculas de filtro de textura de volume e em maiúsculas de filtro de textura de cubo: | D3DPTFILTERCAPS \_ MINFPOINT, D3DPTFILTERCAPS \_ MINFLINEAR, D3DPTFILTERCAPS MINFANISFILTER (isso não é necessário para \_ VolumeTextureFilterCaps e CubeTextureFilterCaps ), \_ D3DPTFILTERCAPS MIPFPOINT, D3DPTFILTERCAPS \_ MIPFLINEAR, D3DPTFILTERCAPS \_ MAGFPOINT, D3DPTFILTERCAPS \_ MAGFLINEAR             |
| Os seguintes modos de endereço de textura têm suporte em estágios de vértice e pixel:                                | D3DPTADDRESSCAPS \_ WRAP, D3DPTADDRESSCAPS \_ MIRROR, D3DPTADDRESSCAPS \_ FIX, D3DPTADDRESSCAPS \_ BORDER, D3DPTADDRESSCAPS \_ INDEPENDENTUV, D3DPTADDRESSCAPS \_ MIRRORONCE                                                                                                                                    |
| Há suporte para todos os limites do sombreador de pixel.                                                                     | DynamicFlowControlDepth = 24, NumTemps = 32, StaticFlowControlDepth = 4, NumInstructionSlots = 512. Há suporte para os seguintes recursos: predicação, swizzles arbitrários e instruções de gradiente. Não há limite de leitura dependente e nenhum limite na combinação de textura e instruções matemáticas. |
| Todas as operações de estêncil têm suporte. Isso inclui dois esêncil laterais.                                   | Consulte [ **D3DSTENCIOPE**](/windows/desktop/direct3d9/d3dstencilop)                                                                                                                                                                                                                                                        |
| Tamanho do ponto de suporte do dispositivo por vértice                                                                         | PSIZE D3DFVFCAPS \_ em D3DCAPS9                                                                                                                                                                                                                                                                         |
| Sem potência de 2 suporte à textura.                                                                              | Suporte completo ou suporte condicional não pow-2; O dispositivo não deve ter a limitação somente de textura quadrada, como em D3DPTEXTURECAPS \_ SQUAREONLY.                                                                                                                                                    |
| Se o dispositivo dá suporte a vários rendertargets, há suporte para os seguintes limites:                             | D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS, D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING                                                                                                                                                                                                                         |
| Se \_ versus \_ 3 0 tiver suporte                                                                                     | MaxUserClipPlanes em D3DCAPS9 é 6                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sombreadores de pixel](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 