---
title: bfrev (SM5-ASM)
description: Inverta um número de 32 bits.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988593"
---
# <a name="bfrev-sm5---asm"></a>bfrev (SM5-ASM)

Inverta um número de 32 bits.



| bfrev dest \[ . Mask \] , src0 \[ . swizzle\] |
|---------------------------------------|



 



| Item                                                            | Descrição                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço para *src0* com bits invertidos.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] número de 32 bits para reverter.<br/>              |



 

## <a name="remarks"></a>Comentários

Por exemplo, dado 0x12345678, o resultado seria 0x1e6a2c48.

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

 

 





