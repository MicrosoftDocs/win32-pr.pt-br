---
title: dmul (SM5-ASM)
description: Multiplicação de precisão dupla por componente.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988576"
---
# <a name="dmul-sm5---asm"></a>dmul (SM5-ASM)

Multiplicação de precisão dupla por componente.



| dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> *dest*  =  *src0* \* *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para multiplicar com *src1*.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes para multiplicar com *src0*.<br/>                                          |



 

## <a name="remarks"></a>Comentários

O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw. As máscaras de *destino* válidas são. XY,. zw e. xyzw. Os seguintes mapeamentos *src* são swizzle:

-   *dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.

F significa número real finito.



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **src0 src1->** | **-INF** | **-F** | **-1,0** | **-0** | **+0** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
| **-INF**           | +inf     | +inf   | +inf     | NaN    | NaN    | -inf     | -inf   | -inf     | NaN     |
| **-F**             | +inf     | + F     | -src0    | +0     | -0     | src0     | -F     | -inf     | NaN     |
| **-1,0 f**          | +inf     | -src1  | + 1,0     | +0     | -0     | -1,0     | -src1  | -inf     | NaN     |
| **-0**             | NaN      | +0     | +0       | +0     | -0     | -0       | -0     | NaN      | NaN     |
| **+0**             | NaN      | -0     | -0       | -0     | +0     | +0       | +0     | NaN      | NaN     |
| **+ 1,0**           | -inf     | src1   | -1,0     | -0     | +0     | +1       | src1   | +inf     | NaN     |
| **+ F**             | -inf     | -F     | -src0    | -0     | +0     | src0     | + F     | +inf     | NaN     |
| **+ INF**           | -inf     | -inf   | -inf     | NaN    | NaN    | +inf     | +inf   | +inf     | NaN     |
| **NaN**            | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





