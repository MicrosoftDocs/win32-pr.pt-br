---
title: emit_stream (SM5-ASM)
description: Emitir um vértice para um determinado fluxo.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365218"
---
# <a name="emit_stream-sm5---asm"></a>fluxo de emissão \_ (SM5-ASM)

Emitir um vértice para um determinado fluxo.



| emitir \_ fluxo streamIndex |
|--------------------------|



 



| Item                                                                                                               | Descrição                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[no \] índice de fluxo.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução faz com que todos os registros de o declarados do \# fluxo de dados sejam lidos do sombreador de geometria para gerar um vértice. Após a emissão, todos os dados em todos os registros de saída de todos os fluxos se tornam não inicializados, não apenas o fluxo emitido para.

*streamIndex* deve ser um valor imediato \[ 0.. 3 \] para um fluxo declarado.

Como várias chamadas de **\_ fluxo de emissão** são emitidas, os primitivos são gerados.

### <a name="restrictions"></a>Restrições

-   **o \_ fluxo de emissão** pode aparecer qualquer número de vezes em um sombreador de geometria, incluindo dentro do controle de fluxo.
-   Se os fluxos não tiverem sido declarados, você deverá usar [Emit](emit--sm4---asm-.md) em vez de **\_ Stream de emissão**.

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

 

 





