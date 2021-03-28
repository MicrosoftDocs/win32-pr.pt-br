---
title: deriv_rty (sm4-ASM)
description: Equivalente de render-destino y de derivar \_ RTX.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823436"
---
# <a name="deriv_rty-sm4---asm"></a>derivar \_ rty (sm4-ASM)

Equivalente de render-destino y de [derivar \_ RTX](deriv-rtx--sm4---asm-.md).



| deriva \_ rty \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
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
-   [derivar \_ RTX](deriv-rtx--sm4---asm-.md) é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada y do Quad. Em seguida, o resultado é calculado como: *src0*(x estranho)- *src0*(até mesmo x pixel) \[ por componente\]
-   **derivar \_ rty** é computado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada x do Quad. Em seguida, o resultado é calculado como: *src0*(y x-pixel)- *src0*(mesmo y pixel) \[ por componente\]

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

 

 





