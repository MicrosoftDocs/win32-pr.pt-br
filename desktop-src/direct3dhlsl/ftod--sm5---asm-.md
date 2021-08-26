---
title: ftod (SM5-ASM)
description: Conversão por componente de dados de ponto flutuante de precisão simples para dados de ponto flutuante de precisão dupla.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31396aa0f2b82dc4ea366bbdde704d55fa850d0d0a9f2f1f3de539a763facb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982426"
---
# <a name="ftod-sm5---asm"></a>ftod (SM5-ASM)

Conversão por componente de dados de ponto flutuante de precisão simples para dados de ponto flutuante de precisão dupla.



| ftod dest \[ . Mask \] , \[ - \] src \[ . swizzle \] , |
|-------------------------------------------|



 



| Item                                                            | Descrição                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos dados convertidos.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] dados a serem convertidos.<br/>          |



 

## <a name="remarks"></a>Comentários

Cada componente da origem é convertido da representação de precisão única para a representação de precisão dupla.

As máscaras de *destino* válidas são. XY,. zw e. xyzw. . o XY recebe o resultado da primeira conversão e. zw recebe o resultado da segunda conversão.

*dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

*src* é um vec2 flutuante entre x e y (ZW ignorado) (post swizzle).

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

 

 





