---
title: ubfe (SM5-ASM)
description: Dado um intervalo de bits em um número, mude esses bits para o LSB e defina os bits restantes como 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823446"
---
# <a name="ubfe-sm5---asm"></a>ubfe (SM5-ASM)

Dado um intervalo de bits em um número, mude esses bits para o LSB e defina os bits restantes como 0.



| ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contém os resultados da instrução.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] LSB de 5 bits fornecem a largura do campo de bits (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] LSB 5 bits de *src1* fornecem o deslocamento de campo de bits (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[no \] número a ser deslocado.<br/>                                         |



 

## <a name="remarks"></a>Comentários

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

Use esta instrução para desempacotar os números inteiros ou sinalizadores não assinados.

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

 

 





