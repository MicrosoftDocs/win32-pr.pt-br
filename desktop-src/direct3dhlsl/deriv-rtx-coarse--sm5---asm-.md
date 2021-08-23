---
title: deriv_rtx_coarse (sm5 – asm)
description: Calcula a taxa de alteração de componentes. | deriv_rtx_coarse (sm5 – asm)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50066fe58c3d0a0cdd903de9fbb479a8fbab2c3a20c622ebca138c0937aaf0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986636"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>deriv \_ rtx \_ coarse (sm5 - asm)

Calcula a taxa de alteração de componentes.



| deriv \_ rtx \_ coarse sat \[ \_ \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] |
|----------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução calcula a taxa de alteração do conteúdo de cada componente float32 de *src0* (pós-swizzle), com relação à direção RenderTarget x (rtx) ou RenderTarget y (consulte [ \_ derivar rty \_ coarse](deriv-rty-coarse--sm5---asm-.md)). Somente um único par derivado x,y é calculado para cada carimbo de 2x2 de pixels.

Os dados na invocação do sombreador de pixel atual podem ou não participar do cálculo do derivado solicitado, pois o derivado será calculado apenas uma vez por 2x2 quad. Por exemplo, o derivado x pode ser um delta da linha superior de pixels e a direção y ( derivada[ \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md)) pode ser um delta da coluna esquerda de pixels. O cálculo exato é até o fornecedor do hardware. Também não há nenhuma especificação que dita como os quads 2x2 serão alinhados ou lado a lado sobre um primitivo.

Os derivados são calculados em um nível alto, uma vez por quad de 2x2 pixels. Essa instrução [e \_ o rty rty \_ deriv são](deriv-rty-coarse--sm5---asm-.md) alternativas para [derivar \_ rtx \_ fine](deriv-rtx-fine--sm5---asm-.md) [e \_ derivar rty \_ fine.](deriv-rty-fine--sm5---asm-.md) Essas \_ instruções \_ derivadas finas e finas são uma substituição para **\_ derivar rtxderiv \_ rty** de modelos de sombreador anteriores.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





