---
title: f16tof32 (SM5-ASM)
description: Float16 de componente para conversão de float32. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc4456737d5ddaaed351ae2a1cc76418c33af9c498e725099e1912d8fabe7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562647"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (SM5-ASM)

Float16 de componente para conversão de float32.



| f16tof32 dest \[ . Mask \] , \[ - \] src \[ . swizzle\] |
|----------------------------------------------|



 



| Item                                                            | Descrição                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado de float32.<br/> |
| <span id="src"></span><span id="SRC"></span>*orig*<br/>    | \[no \] valor float16 a ser convertido.<br/>      |



 

## <a name="remarks"></a>Comentários

Esta operação executa uma conversão por componente de um valor de float16 de LSB bits para um resultado de float32.

Esta operação segue as regras do D3D para conversão de ponto flutuante.

Use esta instrução para descompactação de dados orientada por sombreador.

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

 

 





