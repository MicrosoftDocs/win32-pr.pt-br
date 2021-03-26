---
title: usubb (SM5-ASM)
description: Subtração de inteiro sem sinal com empréstimo.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365191"
---
# <a name="usubb-sm5---asm"></a>usubb (SM5-ASM)

Subtração de inteiro sem sinal com empréstimo.



| usubb dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                               | Descrição                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] contém os resultados de LSAB da instrução.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[no \] componente correspondente de *dest0* que especifica se um empréstimo foi produzido.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[no \] valor do qual subtrair.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[no \] valor a ser subtraído de *src0*.<br/>                                             |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um subtração não assinado por componente de operandos de 32 bits *src1* de *src0*, colocando a parte LSB do resultado de 32 bits em *dest0*.

O componente correspondente no *dest1* será gravado com 1 se um empréstimo for produzido; caso contrário, 0.

*dest1* pode ser nulo se o empréstimo não for necessário.

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

 

 





