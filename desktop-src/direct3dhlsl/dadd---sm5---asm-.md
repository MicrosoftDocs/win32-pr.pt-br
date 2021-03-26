---
title: Dadd (SM5-ASM)
description: Adição de precisão dupla por componente.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365192"
---
# <a name="dadd-sm5---asm"></a>Dadd (SM5-ASM)

Adição de precisão dupla por componente.



| Dadd \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes a serem adicionados com *src1*.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes a serem adicionados com *src0*<br/>           |



 

## <a name="remarks"></a>Comentários

O swizzles válido para os parâmetros de origem são. xyzw,. xyxy,. zwxy,. zwzw. As máscaras de *destino* válidas são. XY,. zw e. xyzw. Os seguintes mapeamentos são swizzle:

-   *dest* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo entre (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou Subfluxo ocorra.

F significa número real finito.



<table>
<tbody>
<tr class="odd">
<td><dl> <strong>src0</strong><br />
<strong>src1-></strong><br />
</dl></td>
<td><strong>-INF</strong></td>
<td><strong>-F</strong></td>
<td><strong>-0</strong></td>
<td><strong>+0</strong></td>
<td><strong>+ F</strong></td>
<td><strong>+ INF</strong></td>
<td><strong>NaN</strong></td>
</tr>
<tr class="even">
<td><strong>-INF</strong></td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>NaN</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>-F</strong></td>
<td>-inf</td>
<td>-F</td>
<td>src0</td>
<td>src0</td>
<td>+-F ou +-0</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>-0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>-0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>+0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>+ F</strong></td>
<td>-inf</td>
<td>+-F ou +-0</td>
<td>src0</td>
<td>src0</td>
<td>+ F</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+ INF</strong></td>
<td>NaN</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>NaN</strong></td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
</tr>
</tbody>
</table>



 

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

 

 





