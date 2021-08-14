---
title: uaddc (sm5 – asm)
description: Um inteiro sem sinal adiciona com carry.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f649ed68626e5b3351ee1b3c7d5848c8e42f7ec175b4b76c929571056f48e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722184"
---
# <a name="uaddc-sm5---asm"></a>uaddc (sm5 – asm)

Um inteiro sem sinal adiciona com carry.



| uaddc dest0 \[ .mask \] , dest1 \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                               | Descrição                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[em \] Endereço do resultado.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[em \] 1 se carry for produzido. Caso contrário, 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[no \] operand de 32 bits a ser adicionado.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[no \] operand de 32 bits a ser adicionado.<br/>          |



 

## <a name="remarks"></a>Comentários

*dest1* poderá ser NULL se o transporte não for necessário.

Use esta instrução para aritmética de alta precisão.

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

 

 





