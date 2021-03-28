---
title: dcl_stream (SM5-ASM)
description: Declare um fluxo de saída do sombreador de geometria.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365286"
---
# <a name="dcl_stream-sm5---asm"></a>\_fluxo de DCL (SM5-ASM)

Declare um fluxo de saída do sombreador de geometria.



| fluxo de DCL \_ m\# |
|-----------------|



 



| Item                                                       | Descrição                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*d\#*<br/> | \[no \] fluxo 0.. 3 (M0.. m3).<br/> |



 

## <a name="remarks"></a>Comentários

Um determinado fluxo só pode ser declarado uma vez.

Se nenhum fluxo for declarado, as declarações de topologia de saída e saída serão consideradas para o fluxo 0.

O primeiro **\_ fluxo DCL** não pode aparecer após nenhuma instrução de **\_ saída DCL** ou **\_ outputTopology DCL** .

Todas as instruções de **\_ saída DCL** ou **DCL \_ outputToplogy** após qualquer instrução de **\_ fluxo** m de DCL \# definem as saídas para o fluxo m \# .

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

 

 





