---
title: BFI (SM5-ASM)
description: Dado um intervalo de bits do LSB de um número, coloque esse número de bits em outro número em qualquer deslocamento.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006902"
---
# <a name="bfi-sm5---asm"></a>BFI (SM5-ASM)

Dado um intervalo de bits do LSB de um número, coloque esse número de bits em outro número em qualquer deslocamento.



| BFI dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle \] , src3 \[ . swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[na largura do campo de \] bits a ser tomada de *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] deslocamento de campo de bits para substituição de partes em *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[no \] número do qual os bits são tirados. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[no \] número com bits a serem substituídos.<br/>              |



 

## <a name="remarks"></a>Comentários

Os LSB 5 bits de *src0* fornecem a largura do campo de bits (0-31) a ser tomada em *src2*.

Os LSB 5 bits de *src1* fornecem o deslocamento de campo de bits (0-31) para iniciar a substituição de bit no número lido de *src3*.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Essa instrução é usada para empacotar inteiros ou sinalizadores.

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

 

 





