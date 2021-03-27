---
title: countbits (SM5-ASM)
description: Conta o número de bits definidos em um número.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823448"
---
# <a name="countbits-sm5---asm"></a>countbits (SM5-ASM)

Conta o número de bits definidos em um número.



| countbits dest \[ . Mask \] , src0 \[ . swizzle\] |
|-------------------------------------------|



 



| Item                                                            | Descrição                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] número de entrada 32-bit.<br/>    |



 

## <a name="remarks"></a>Comentários

Essa instrução pode ser usada para calcular a porcentagem de cobertura de entrada do sombreador.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
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

 

 





