---
title: IBFE (SM5-ASM)
description: Dado um intervalo de bits em um número, mude esses bits para o LSB e assine a extensão do MSB do intervalo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b04bfcaea154a8a63e9b118da12a8994398357b7c6a022a4589353c6c06eb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949616"
---
# <a name="ibfe-sm5---asm"></a>IBFE (SM5-ASM)

Dado um intervalo de bits em um número, mude esses bits para o LSB e assine a extensão do MSB do intervalo.



| IBFE dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[na \] largura do campo de bits.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] deslocamento de campo de bits.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[no \] valor a ser deslocado.<br/>                          |



 

## <a name="remarks"></a>Comentários

Os LSB 5 bits de src0 fornecem a largura do campo de bits (0-31).

Os LSB 5 bits de src1 fornecem o deslocamento de campo de bits (0-31).

O exemplo a seguir mostra como usar essa instrução.

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

Use esta instrução para desempacotar os inteiros ou sinalizadores assinados.

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

 

 





