---
title: dcl_input_control_point_count (SM5-ASM)
description: Declare a contagem de pontos de controle de entrada do sombreador envoltória na seção declaração do sombreador envoltória.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365295"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>\_ \_ \_ \_ contagem de pontos de controle de entrada de DCL (SM5-ASM)

Declare a contagem de pontos de controle de entrada do sombreador envoltória na seção declaração do sombreador envoltória.



| contagem de pontos de controle de entrada de DCL \_ \_ \_ \_ {1.. 32} |
|-------------------------------------------|



 



| Item                                                   | Descrição                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*P*<br/> | \[na \] contagem de pontos de controle de entrada.<br/> |



 

## <a name="remarks"></a>Comentários

Pelo menos 1 ponto de controle de entrada é necessário; Ele poderá ficar vazio se não for necessário.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





