---
title: paid (sm5 – asm)
description: Adição de precisão dupla por componente.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e382ea2660b587a843ecca4c3bae93251a5f9434bd2cdca5899beaf25bb2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793524"
---
# <a name="dadd-sm5---asm"></a>paid (sm5 – asm)

Adição de precisão dupla por componente.



| paid \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes a adicionar com *src1*.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os componentes a adicionar com *src0*<br/>           |



 

## <a name="remarks"></a>Comentários

Os swizzles válidos para os parâmetros de origem são .xyzw, .xyxy, .zwxy, .zwzw. As máscaras *de dest* válidas são .xy, .zw e .xyzw. Os seguintes mapeamentos são pós-swizzle:

-   *dest* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src0* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).
-   *src1* é um vec2 duplo em (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números, supondo que nenhum estouro ou estouro ocorra.

F significa número finito real.



<table>
<tbody>
<tr class="odd">
<td><dl> <strong>src0</strong><br />
<strong>src1-></strong><br />
</dl></td>
<td><strong>-inf</strong></td>
<td><strong>-F</strong></td>
<td><strong>-0</strong></td>
<td><strong>+0</strong></td>
<td><strong>+F</strong></td>
<td><strong>+inf</strong></td>
<td><strong>NaN</strong></td>
</tr>
<tr class="even">
<td><strong>-inf</strong></td>
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
<td><strong>+F</strong></td>
<td>-inf</td>
<td>+-F ou +-0</td>
<td>src0</td>
<td>src0</td>
<td>+F</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+inf</strong></td>
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



 

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
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

 

 





