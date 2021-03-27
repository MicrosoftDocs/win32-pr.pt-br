---
title: Umad (sm4-ASM)
description: Número de multiplicação e adição de inteiro não assinado.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638866"
---
# <a name="umad-sm4---asm"></a>Umad (sm4-ASM)

Número de multiplicação e adição de inteiro não assinado.



| Umad dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle \] , src2 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/>           |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] valor para multiplicar com *src1*.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] valor para multiplicar com *src1*.<br/>                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[no \] valor a ser adicionado ao produto de *src0* e *src1*.<br/> |



 

## <a name="remarks"></a>Comentários

Componente [umul](umul--sm4---asm-.md) de operandos de 32 bits *src0* e *src1* não assinados, mantendo os poucos 32 bits, por componente, do resultado. Em seguida, essa instrução executa um [IAdd](iadd--sm4---asm-.md) de *src2*, produzindo o resultado de baixa de 32 bits (por componente) correto. Os resultados de 32 bits são colocados no *dest*.

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

 

 





