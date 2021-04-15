---
title: Imad (sm4-ASM)
description: Número inteiro de multiplicação e adição de inteiros assinados.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988559"
---
# <a name="imad-sm4---asm"></a>Imad (sm4-ASM)

Número inteiro de multiplicação e adição de inteiros assinados.



| Imad dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle \] , \[ - \] src2 \[ . swizzle |
|---------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação.<br/>                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] valor para multiplicar com *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] valor para multiplicar com *src0*.<br/>                    |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[em \] valor para adicionar ao produto de *src0* e *src1*.<br/> |



 

## <a name="remarks"></a>Comentários

Componente [imul](imul--sm4---asm-.md) de operandos de 32 bits *src0* e *src1* (assinados), mantendo os poucos 32 bits (por componente) do resultado, seguido por um [IAdd](iadd--sm4---asm-.md) de *src2*, produzindo o resultado de 32 bits (por componente) correto. Os resultados de 32 bits são colocados no *dest*.

O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação aritmética.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





