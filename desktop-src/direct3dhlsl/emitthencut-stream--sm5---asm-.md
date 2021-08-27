---
title: emitThenCut_stream (sm5 – asm)
description: Equivalente a um comando de eit seguido por um comando cut. | emitThenCut_stream (sm5 – asm)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d2be28ae1d63617b8ba775f8f8839c270668aeeded8a4944ef9ae7554d598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067956"
---
# <a name="emitthencut_stream-sm5---asm"></a>fluxo emitThenCut \_ (sm5 - asm)

Equivalente a um [comando de eit](emit--sm4---asm-.md) seguido por um [comando cut.](cut--sm4---asm-.md)



| emitThenCut \_ streamIndex |
|---------------------------------|



 



| Item                                                                                                               | Descrição                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[em \] O índice de fluxo.<br/> |



 

## <a name="remarks"></a>Comentários

Essa operação é útil ao sair com conhecimento do último vértice em uma topologia.

Se os fluxos não foram declarados, você deve usar [emitThenCut em](emitthencut--sm4---asm-.md) vez **de emitThenCut \_ stream**.

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

 

 





