---
title: DMáx (SM5-ASM)
description: Máximo de precisão dupla por componente.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6846da6fbf3ad5d42be5131322e1214fc49fe2627b824775798e4527de3d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068366"
---
# <a name="dmax-sm5---asm"></a>DMáx (SM5-ASM)

Máximo de precisão dupla por componente.



| DMáx \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> *dest*  =  *src0*  >=  *src1* ? *src0* : *src1*<br/> >= é usado em vez de > de forma que, se min (x, y) = x, Max (x, y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] valor a ser comparado com *src1*.<br/>                                                                                                                                                           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] valor a ser comparado com *src0*.<br/>                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

NaN tem tratamento especial. Se um operando de origem for NaN, o outro operando de origem será retornado. A escolha é feita por componente. Se ambos forem NaN, qualquer representação NaN será retornada.

O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw. As máscaras de *destino* válidas são. XY,. zw e. xyzw. Os seguintes mapeamentos *src* são swizzle:

-   *dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





