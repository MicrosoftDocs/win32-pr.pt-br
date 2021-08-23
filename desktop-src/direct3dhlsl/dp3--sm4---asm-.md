---
title: dp3 (sm4 – asm)
description: Vetor tridimensional dot-product de componentes rgb, POS-swizzle.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7e74d0e1cb623377c63de6717e546b5c0ba74c2609ace8d0f01de252f28f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625536"
---
# <a name="dp3-sm4---asm"></a>dp3 (sm4 – asm)

Vetor tridimensional dot-product de componentes rgb, POS-swizzle.



| dp3 \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle, \] |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O resultado da operação.<br/> *dest*  =  *src0.r* \* *src1.r*  +  *src0.g* \* *src1.g*  +  *src0.b* \* *src1.b*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes na propriedade.<br/>                                                                                   |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os componentes na propriedade.<br/>                                                                                   |



 

## <a name="remarks"></a>Comentários

Resultado escalar replicado para componentes na máscara de gravação.

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

 

 





