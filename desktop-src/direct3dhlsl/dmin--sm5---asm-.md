---
title: dmin (sm5 – asm)
description: Mínimo de precisão dupla por componente.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20977a24113db111e85bc644ed68eccaa7e75db91c18bf71d80ac89f5ee19547
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855116"
---
# <a name="dmin-sm5---asm"></a>dmin (sm5 – asm)

Mínimo de precisão dupla por componente.



| dmin \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados da operação.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> < é usado em vez de <= para que se min(x,y) = x, max(x,y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes a comparar com *src1*.<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os componentes a comparar com *src0*.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

O NaN tem tratamento especial. Se um operand de origem for NaN, o outro operand de origem será retornado. A escolha é feita por componente. Se ambos são NaN, qualquer representação NaN é retornada.

Os swizzles válidos para os parâmetros de origem são .xyzw, .xyxy, .zwxy, .zwzw. As máscaras *de dest* válidas são .xy, .zw e .xyzw. Os seguintes *mapeamentos de src* são pós-swizzle:

-   *dest* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





