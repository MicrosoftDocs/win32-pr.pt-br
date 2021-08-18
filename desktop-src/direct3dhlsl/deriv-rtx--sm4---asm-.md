---
title: deriv_rtx (sm4-ASM)
description: Taxa de alteração de conteúdo de cada componente float32 de src0 (post-swizzle), com relação à direção de RenderTarget x (RTX) ou à direção de RenderTarget y.
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
# <a name="deriv_rtx-sm4---asm"></a>derivar \_ RTX (sm4-ASM)

Taxa de alteração de conteúdo de cada componente float32 de *src0* (post-swizzle), com relação à direção de renderTarget x (RTX) ou à direção de renderTarget y.



| deriva \_ RTX \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
|--------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Apenas um único par derivado x, y é calculado para cada carimbo 2x2 de pixels.

Esta operação é dependente de hardware.

Implementação do rasterizador de referência para triângulos:

-   O sombreador de pixel sempre executa o sombreador sobre 2x2 de quatro pixels em atrelada (até mesmo por meio do controle de fluxo, mascarando pixels desabilitados).
-   Os quatro processadores sempre têm coordenadas de pixel numeradas (x e y) para o pixel superior esquerdo.
-   Os pixels fictícios ficam inativos primitivos se o primitivo for muito pequeno para preencher um 2x2 quádruplo.
-   **derivar \_ RTX** é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada y do Quad. Em seguida, o resultado é calculado como: *src0*(x estranho)- *src0*(até mesmo x pixel) \[ por componente\]
-   [derivar \_ rty](deriv-rty--sm4---asm-.md) é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada x do Quad. Em seguida, o resultado é calculado como: *src0*(y x-pixel)- *src0*(mesmo y pixel) \[ por componente\]

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





