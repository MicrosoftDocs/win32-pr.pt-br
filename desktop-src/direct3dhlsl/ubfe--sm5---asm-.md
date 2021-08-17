---
title: ubfe (sm5 – asm)
description: Dado um intervalo de bits em um número, deslocar esses bits para o LSB e definir os bits restantes como 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3149173bf495957bb38800234e4d853d0e32797254eecfdb3e5b77faf4498ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722157"
---
# <a name="ubfe-sm5---asm"></a>ubfe (sm5 – asm)

Dado um intervalo de bits em um número, deslocar esses bits para o LSB e definir os bits restantes como 0.



| ubfe dest \[ .mask \] , src0 \[ .swizzle, \] src1 \[ .swizzle, \] src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] Contém os resultados da instrução.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os 5 bits LSB fornecem a largura do campo de bits (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] LSB, 5 bits *de src1* fornecem o deslocamento do campo de bits (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[em \] O número a ser deslocado.<br/>                                         |



 

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

Use esta instrução para desempacotar inteiros ou sinalizadores sem sinal.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





