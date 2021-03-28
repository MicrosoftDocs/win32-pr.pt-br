---
title: uaddc (SM5-ASM)
description: Adição de inteiro sem sinal com transporte.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498942"
---
# <a name="uaddc-sm5---asm"></a>uaddc (SM5-ASM)

Adição de inteiro sem sinal com transporte.



| uaddc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                               | Descrição                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[em \] endereço do resultado.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[em \] 1, se a execução for produzida. Caso contrário, 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[no \] operando de 32 bits a ser adicionado.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[no \] operando de 32 bits a ser adicionado.<br/>          |



 

## <a name="remarks"></a>Comentários

*dest1* pode ser nulo se o transporte não for necessário.

Use esta instrução para aritmética de alta precisão.

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

 

 





