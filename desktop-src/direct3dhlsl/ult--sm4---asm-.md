---
title: ultados (sm4-ASM)
description: Comparação de inteiros não assinados de vetor sem sinal de componente.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988571"
---
# <a name="ult-sm4---asm"></a>ultados (sm4-ASM)

Comparação de inteiros não assinados de vetor sem sinal de componente.



| ultados dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|-------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] valor a ser comparado com *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] valor a ser comparado com *src1*.<br/>             |



 

## <a name="remarks"></a>Comentários

Executa a comparação de inteiros sem sinal (*src0*  <  *src1*) para cada componente e grava o resultado em *dest*.

Se a comparação for verdadeira, essa instrução retornará 0xFFFFFFFF para esse componente. Caso contrário, ele retornará 0x0000000.

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

 

 





