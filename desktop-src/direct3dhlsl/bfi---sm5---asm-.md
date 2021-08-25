---
title: bfi (sm5 – asm)
description: Dado um intervalo de bits do LSB de um número, coloque esse número de bits em outro número em qualquer deslocamento.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1452b1f15525753738ee6f74a1bd43473f43033346c9b493cd72222eaab22cb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068526"
---
# <a name="bfi-sm5---asm"></a>bfi (sm5 – asm)

Dado um intervalo de bits do LSB de um número, coloque esse número de bits em outro número em qualquer deslocamento.



| bfi dest \[ .mask \] , src0 \[ \] .swizzle , src1 \[ .swizzle, \] src2 \[ .swizzle \] , src3 \[ .swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] A largura do campo de bits a ser de *src2*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] deslocamento do campo de bits para substituir bits em *src3.*<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[em \] O número de onde os bits são retirados. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[em \] O número com bits a serem substituídos.<br/>              |



 

## <a name="remarks"></a>Comentários

Os 5 bits LSB de *src0* fornecem a largura do campo de bits (0-31) a ser assumida de *src2.*

Os 5 bits LSB de *src1* fornecem o deslocamento do campo de bits (0-31) para começar a substituir os bits no número lido de *src3.*

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Essa instrução é usada para empacotar inteiros ou sinalizadores.

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

 

 





