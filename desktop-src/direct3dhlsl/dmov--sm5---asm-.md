---
title: dmov (SM5-ASM)
description: Movimentação por componentes. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930518"
---
# <a name="dmov-sm5---asm"></a>dmov (SM5-ASM)

Movimentação por componentes.



| dmov \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|-------------------------------------------------------------|



 



| Item                                                            | Descrição                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] destino da movimentação. *dest*  =  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes a serem movidos.<br/>            |



 

## <a name="remarks"></a>Comentários

Os modificadores, exceto swizzle, assumem que os dados são de ponto flutuante. A ausência de modificadores move dados sem alterar bits.

O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw. Os seguintes mapeamentos *src* são swizzle:

-   *src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
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

 

 





