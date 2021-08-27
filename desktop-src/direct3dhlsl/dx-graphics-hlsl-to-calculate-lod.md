---
title: CalculateLevelOfDetail (objeto de textura directX HLSL)
description: Calcula o nível de detalhes.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44d71469cf5fd3246a0bb038cf369227cb3a3017
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625822"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a>CalculateLevelOfDetail (objeto de textura directX HLSL)

Calcula o nível de detalhes.

ret Object.CalculateLevelOfDetail( sampler \_ state S, float x );



 

## <a name="parameters"></a>Parâmetros



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em><br/></td>
<td>Qualquer <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (exceto Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Um <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">estado sampler</a>. Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="x"></span><span id="X"></span><em>X</em><br/></td>
<td>[in] O valor ou valores de interpolação linear, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive. O número de componentes depende do tipo de objeto de textura. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
<th>Tipo de parâmetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float1</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valor Retornado

Retorna o LOD calculado, um único valor de ponto flutuante.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | x         |          |           |



 

1.  TextureCubeArray está disponível no Modelo de Sombreador 4.1 ou superior.
2.  O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto de textura](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

