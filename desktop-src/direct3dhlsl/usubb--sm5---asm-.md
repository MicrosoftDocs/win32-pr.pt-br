---
title: usubb (sm5 – asm)
description: Subtração de inteiro sem sinal com empréstimo.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c2f70f39729f5245f7044945e9d3b233ec4f0893be27c5143f5c55989693b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721820"
---
# <a name="usubb-sm5---asm"></a>usubb (sm5 – asm)

Subtração de inteiro sem sinal com empréstimo.



| usubb dest0 \[ .mask \] , dest1 \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                               | Descrição                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[em \] Contém os resultados do LSAB da instrução.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[em \] O componente correspondente de *dest0* que especifica se um empréstimo foi produzido.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[em \] O valor do qual subtrair.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[em \] O valor a ser subtraído de *src0*.<br/>                                             |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma subtração sem assinatura de componente de 32 bits *src1* de *src0*, colocando a parte LSB do resultado de 32 bits em *dest0*.

O componente correspondente em *dest1* será escrito com 1 se um empréstimo for produzido; caso contrário, 0.

*dest1* poderá ser NULL se o empréstimo não for necessário.

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

 

 





