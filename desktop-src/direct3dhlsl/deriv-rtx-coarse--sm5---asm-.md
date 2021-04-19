---
title: deriv_rtx_coarse (SM5-ASM)
description: Computa a taxa de alteração de componentes. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989162"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>derivar \_ RTX \_ grande (SM5-ASM)

Computa a taxa de alteração de componentes.



| deriva \_ RTX \_ de \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
|----------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução computa a taxa de alteração de conteúdo de cada componente float32 de *src0* (post-swizzle), com relação à direção de renderTarget x (RTX) ou à direção de renderTarget y (Confira [derivação de \_ rty \_ grande](deriv-rty-coarse--sm5---asm-.md)). Apenas um único par derivado x, y é calculado para cada carimbo 2x2 de pixels.

Os dados na invocação do sombreador de pixel atual podem ou não participar do cálculo da derivação solicitada, porque o derivativo será calculado apenas uma vez por 2x2 Quad. Por exemplo, a derivação x pode ser um Delta da linha superior de pixels e a direção y ([derivada de \_ rty \_ ](deriv-rty-coarse--sm5---asm-.md)) poderia ser um Delta da coluna esquerda de pixels. O cálculo exato é até o fornecedor do hardware. Também não há nenhuma especificação que determine como as quatro quádruplas de 2x2 serão alinhadas ou colocadas em um primitivo.

Os derivativos são calculados em um nível mais baixo, uma vez por quatro por 2x2 pixels. Essa instrução e [o \_ rty \_ de derivação](deriv-rty-coarse--sm5---asm-.md) são alternativas para [derivar \_ RTX \_ bem](deriv-rtx-fine--sm5---asm-.md) e [derivar \_ rty \_ ](deriv-rty-fine--sm5---asm-.md). Essas \_ \_ instruções derivadas mais altas e finas são uma substituição para **derivar \_ rtxderiv \_ rty** de modelos de sombreador anteriores.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





