---
title: deriv_rtx_fine (sm5 – asm)
description: Calcula a taxa de alteração de componentes. | deriv_rtx_fine (sm5 – asm)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6666750be76d673ddc6c5f0d66d23131096812c93b71be52eb7e0f6ebb403ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792646"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>deriv \_ rtx \_ fine (sm5 – asm)

Calcula a taxa de alteração de componentes.



| deriv \_ rtx \_ fine sat \[ \_ \] dest \[ \] .mask, \[ - \] src0 abs \[ \_ \] \[ .swizzle, \] |
|--------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução calcula a taxa de alteração do conteúdo de cada componente float32 de *src0* (pós-swizzle), com relação à direção RenderTarget x (rtx) ou RenderTarget y (consulte [ \_ derivar rty \_ fine](deriv-rty-fine--sm5---asm-.md)). Cada pixel no carimbo 2x2 obtém um par exclusivo de cálculos derivados x/y

Os dados na invocação do sombreador de pixel atual sempre participam do cálculo do derivado solicitado. No quad de 2x2 pixels em que o pixel atual se enquadra, o derivado x é o delta da linha de 2 pixels, incluindo o pixel atual. O derivado y é o delta da coluna de 2 pixels, incluindo o pixel atual. Não há nenhuma especificação que dita como os quads 2x2 serão alinhados ou lado a lado sobre um primitivo.

Os derivados são calculados em um nível fino (cálculo exclusivo do par derivado x/y para cada pixel em um quádruplo 2x2). Essa instrução [e o valor fino \_ de \_ ](deriv-rty-fine--sm5---asm-.md) derivação são alternativas [para derivar \_ rtx \_ rty e](deriv-rtx-coarse--sm5---asm-.md) [ \_ rty \_ rty.](deriv-rty-coarse--sm5---asm-.md) Essas instruções derivadas finas e finas são uma substituição para o \_ \_ **\_ rtx** de derivação Essas instruções derivadas finas e finas são uma substituição para \_ \_ **\_ rtx** **\_** derivar e derivar rty de modelos de sombreador anteriores.

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

 

 





