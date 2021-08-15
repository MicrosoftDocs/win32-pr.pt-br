---
title: deriv_rtx (sm4 – asm)
description: Taxa de alteração do conteúdo de cada componente float32 de src0 (pós-swizzle), em relação à direção RenderTarget x (rtx) ou RenderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a9697372964135e5ecb3cb5e916b0509a6a6a860ff8fa01ea0daeb1b8be4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986646"
---
# <a name="deriv_rtx-sm4---asm"></a>deriv \_ rtx (sm4 - asm)

Taxa de alteração do conteúdo de cada componente float32 de *src0* (pós-swizzle), em relação à direção RenderTarget x (rtx) ou RenderTarget y.



| deriv \_ rtx \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 abs \[ \_ \] \[ .swizzle, \] |
|--------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Somente um único par derivado x,y é calculado para cada carimbo de 2x2 de pixels.

Essa operação depende do hardware.

Implementação de rasterizador de referência para triângulos:

-   O Sombreador de Pixel sempre executa o Sombreador em 2x2 quádruplo de pixels em lockstep (mesmo por meio do controle de fluxo, mascaramento de pixels desabilitados).
-   Os quads sempre têm coordenadas de pixel numeradas (x e y) para o pixel superior esquerdo.
-   Pixels fictícios são executados primitivos se primitivos são muito pequenos para preencher um quádruplo 2x2.
-   **deriv \_ rtx** é calculado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada y do quad. Em seguida, o resultado é calculado como: *src0*(pixel ímpar x) – *src0*(até mesmo x pixel) \[ por componente\]
-   [A \_ derivação é](deriv-rty--sm4---asm-.md) calculada escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada x do quad. Em seguida, o resultado é calculado como: *src0*(pixel y ímpar) – *src0*(até mesmo y pixel) \[ por componente\]

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





