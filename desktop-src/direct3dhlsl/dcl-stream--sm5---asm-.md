---
title: dcl_stream (sm5 – asm)
description: Declare um fluxo de saída do sombreador de geometria.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53b8226cc9a4d8d2bd980cd26371f9e7b46a5168ec61ff39e425f73a4d7193c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793037"
---
# <a name="dcl_stream-sm5---asm"></a>fluxo \_ dcl (sm5 – asm)

Declare um fluxo de saída do sombreador de geometria.



| dcl \_ stream m\# |
|-----------------|



 



| Item                                                       | Descrição                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*M\#*<br/> | \[no \] Stream 0..3 (m0.. m3).<br/> |



 

## <a name="remarks"></a>Comentários

Um determinado fluxo só pode ser declarado uma vez.

Se nenhum fluxo for declarado, as declarações de topologia de saída e saída serão assumidas como para o fluxo 0.

O primeiro **fluxo dcl \_ não** pode aparecer após nenhuma **saída dcl \_ ou** **instruções dcl \_ outputTopology.**

Qualquer **instrução dcl \_ output** ou **dcl \_ outputToplogy após** qualquer instrução **dcl \_ stream** m \# define as saídas para o fluxo m \# .

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





