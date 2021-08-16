---
title: dtof (SM5-ASM)
description: Conversão por componente de dados de ponto flutuante de precisão dupla para dados de ponto flutuante de precisão simples.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d16ddf79b1a201bf78e0b45d1206169576bee4193b8c8158469055131768efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792323"
---
# <a name="dtof-sm5---asm"></a>dtof (SM5-ASM)

Conversão por componente de dados de ponto flutuante de precisão dupla para dados de ponto flutuante de precisão simples.



| dtof dest \[ . Mask \] , \[ - \] src \[ . swizzle \] , |
|-------------------------------------------|



 



| Item                                                            | Descrição                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos dados convertidos.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] dados a serem convertidos.<br/>          |



 

## <a name="remarks"></a>Comentários

Cada componente da origem é convertido da representação de precisão dupla para a representação de precisão única usando o arredondamento de arredondamento mais próximo.

O swizzles válido para o parâmetro de origem é. xyzw,. xyxy,. zwxy,. zwzw.

As máscaras de *destino* válidas são um ou dois componentes. Isto é:. x,. y,. z,. w,. XY,. XZ,. XW,. yz,. YW,. zw o resultado da primeira conversão vai para o primeiro componente na máscara e o resultado do segundo componente vai para o segundo componente na máscara, se presente.

os componentes de *destino* são float32.

*src* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB) post swizzle.

Para o float32<->conversões duplas, as implementações podem honrar as innormas float32 ou pode liberá-las.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





