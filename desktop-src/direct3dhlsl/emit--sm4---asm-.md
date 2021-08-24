---
title: emitir (sm4 – asm)
description: Emita um vértice.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce90ed4ea87c74c09c6f45d590e8bc7a70bbb8178988b059c2b3a79726aabcb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673076"
---
# <a name="emit-sm4---asm"></a>emitir (sm4 – asm)

Emita um vértice.



| Emitir |
|------|



 

## <a name="remarks"></a>Comentários

**emitir faz** com que todos os registros o declarados sejam lidos do Sombreador de Geometria \# para gerar um vértice.

À medida **que várias chamadas de** emissão são emitidas, os primitivos são gerados.

**Emit** pode aparecer qualquer número de vezes em um Sombreador de Geometria, incluindo dentro do controle de fluxo.

Se os fluxos foram declarados, você deve usar [o fluxo de \_ emissões](emit-stream--sm5---asm-.md).

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               | x               |              |



 

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




