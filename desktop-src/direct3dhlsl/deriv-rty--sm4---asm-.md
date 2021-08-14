---
title: deriv_rty (sm4 – asm)
description: Renderizar destino y equivalente a deriv \_ rtx.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb522076435b525252e8cab40590c649e5cc8af8a83023ebd6cace1695fbb729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515464"
---
# <a name="deriv_rty-sm4---asm"></a>deriv \_ rty (sm4 - asm)

Valor y de destino de renderização [equivalente a deriv \_ rtx.](deriv-rtx--sm4---asm-.md)



| deriv \_ rty \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] |
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
-   [deriv \_ rtx](deriv-rtx--sm4---asm-.md) é calculado escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada y do quad. Em seguida, o resultado é calculado como: *src0*(pixel ímpar x) – *src0*(até mesmo x pixel) \[ por componente\]
-   **A \_ derivação é** calculada escolhendo primeiro 2 pixels: o pixel atual e o outro pixel com a mesma coordenada x do quad. Em seguida, o resultado é calculado como: *src0*(pixel y ímpar) – *src0*(até mesmo y pixel) \[ por componente\]

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

 

 





