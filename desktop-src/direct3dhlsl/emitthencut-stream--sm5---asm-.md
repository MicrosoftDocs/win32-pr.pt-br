---
title: emitThenCut_stream (SM5-ASM)
description: Equivalente a um comando Emit seguido por um comando Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968315"
---
# <a name="emitthencut_stream-sm5---asm"></a>fluxo de emitThenCut \_ (SM5-ASM)

Equivalente a um comando [Emit](emit--sm4---asm-.md) seguido por um comando [Cut](cut--sm4---asm-.md) .



| emitThenCut \_ Stream streamIndex |
|---------------------------------|



 



| Item                                                                                                               | Descrição                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[no \] índice de fluxo.<br/> |



 

## <a name="remarks"></a>Comentários

Essa operação é útil ao produzir a saída do último vértice em uma topologia.

Se os fluxos não tiverem sido declarados, você deverá usar [emitThenCut](emitthencut--sm4---asm-.md) em vez de **emitThenCut \_ Stream**.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





