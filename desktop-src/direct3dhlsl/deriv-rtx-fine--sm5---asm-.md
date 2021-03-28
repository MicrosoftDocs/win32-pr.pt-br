---
title: deriv_rtx_fine (SM5-ASM)
description: Computa a taxa de alteração de componentes. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989215"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>derivar \_ RTX \_ (SM5-ASM)

Computa a taxa de alteração de componentes.



| deriva \_ RTX \_ de \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
|--------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução computa a taxa de alteração de conteúdo de cada componente float32 de *src0* (post-swizzle), com relação à direção de renderTarget x (RTX) ou à direção de renderTarget y (Confira [derivação \_ rty \_ boa](deriv-rty-fine--sm5---asm-.md)). Cada pixel no carimbo 2x2 Obtém um par exclusivo de cálculos derivativos x/y

Os dados na invocação do sombreador de pixel atual sempre participam do cálculo do derivativo solicitado. No meio do 2x2 pixel em que o pixel atual cai, a derivada x é o Delta da linha de 2 pixels, incluindo o pixel atual. A derivada y é o Delta da coluna de 2 pixels, incluindo o pixel atual. Não há nenhuma especificação que informando como os quatro de 2x2 serão alinhados ou colocados em um primitivo.

Os derivativos são calculados em um nível refinado (cálculo exclusivo do par derivado x/y para cada pixel em um 2x2 Quad). Essa instrução e [o \_ rty \_ de derivação](deriv-rty-fine--sm5---asm-.md) são alternativas para [derivar \_ RTX \_ ](deriv-rtx-coarse--sm5---asm-.md) e derivar [ \_ rty \_ grande](deriv-rty-coarse--sm5---asm-.md). Essas \_ \_ instruções derivadas mais altas e refinadas são uma substituição para **derivar \_ RTX** essas \_ \_ instruções derivativas e exfinadas são uma substituição para **derivar \_ RTX** e **derivar \_ rty** de modelos de sombreador anteriores.

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

 

 





