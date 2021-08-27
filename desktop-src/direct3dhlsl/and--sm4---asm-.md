---
title: e (sm4 – asm)
description: AND bit a bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b23d473522c2a796201a0edfc3a4b0ec9f047f9e00f359f3879fd80cfc699e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068546"
---
# <a name="and-sm4---asm"></a>e (sm4 – asm)

AND bit a **bit.**



| e dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] valor de 32 bits para **AND** com *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] valor de 32 bits para **AND** com *src0*.<br/>    |



 

## <a name="remarks"></a>Comentários

AND lógico por **componente** de cada par de valores de 32 bits de *src0* e *src1*. Os resultados de 32 bits são colocados *em dest.*

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

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

 

 





