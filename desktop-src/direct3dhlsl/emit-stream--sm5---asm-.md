---
title: emit_stream (sm5 – asm)
description: Emita um vértice para um determinado fluxo.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e90bfb72862abeccc8a9411904a7b42f77c933cc4c87af189d6557596389c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562696"
---
# <a name="emit_stream-sm5---asm"></a>emitir \_ fluxo (sm5 – asm)

Emita um vértice para um determinado fluxo.



| emitir \_ streamIndex |
|--------------------------|



 



| Item                                                                                                               | Descrição                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[em \] O índice de fluxo.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução faz com que todos os registros o declarados para o fluxo determinado sejam lidos do sombreador de geometria para \# gerar um vértice. Aferir a emissão, todos os dados em todos os registros de saída para todos os fluxos se tornam não reinicializados, não apenas o fluxo emitido.

*streamIndex* deve ser um valor \[ imediato 0..3 \] para um fluxo declarado.

À medida **que várias chamadas de \_ fluxo** de emissão são emitidas, os primitivos são gerados.

### <a name="restrictions"></a>Restrições

-   **O fluxo \_ de emissões** pode aparecer várias vezes em um sombreador de geometria, incluindo dentro do controle de fluxo.
-   Se os fluxos não foram declarados, você deve usar [emitir](emit--sm4---asm-.md) em vez **de emitir \_ fluxo**.

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

 

 





