---
title: f32tof16 (SM5-ASM)
description: Float16 de componente para conversão de float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7f2a5810024800c812780a8138948ec873f20d1dfe95d554718a6d63b38cb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907740"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Float16 de componente para conversão de float32.



| f32tof16 dest \[ . Mask \] , \[ - \] src \[ . swizzle\] |
|----------------------------------------------|



 



| Item                                                            | Descrição                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado de float16.<br/> |
| <span id="src"></span><span id="SRC"></span>*orig*<br/>    | \[no \] valor float32 a ser convertido.<br/>  |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma conversão por componente de um valor de float32 em um resultado de valor float16 colocado em LSB 16 bits.

Essa instrução segue as regras do D3D para conversão de ponto flutuante.

Use esta instrução para compactação de dados orientada por sombreador.

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

 

 





