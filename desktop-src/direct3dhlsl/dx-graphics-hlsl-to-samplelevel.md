---
title: SampleLevel (objeto de textura DirectX HLSL)
description: Amostra uma textura usando um deslocamento de nível mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73cf7bc0c13987099540cecd49519de35b4b7de1
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "104085018"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (objeto de textura DirectX HLSL)

Amostra uma textura usando um deslocamento de nível mipmap.



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| &lt;Tipo &gt; de modelo Object. SampleLevel (o \_ estado de amostra S, local de flutuação, LOD flutuante \[ , deslocamento int \] ); |



 

Essa função é semelhante à [amostra](dx-graphics-hlsl-to-sample.md) , exceto pelo fato de que ela usa o nível LOD (no último componente do parâmetro Location) para escolher o nível de mipmap. Por exemplo, uma textura 2D usa os dois primeiros componentes para coordenadas UV e o terceiro componente para o nível mipmap.

## <a name="parameters"></a>Parâmetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Qualquer tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (exceto Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>&</em><br/></td>
<td>no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>. Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em><br/></td>
<td>no As coordenadas de textura. O tipo de argumento é dependente do tipo de objeto Texture. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
<th>Tipo de parâmetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D</td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Se o objeto de textura for uma matriz, o último componente será o índice de matriz.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>LOD</em></p></td>
<td><p>no Um número que especifica o nível de mipmap. Se o valor for = 0, o zero'th (maior mapa) será usado. O valor fracionário (se fornecido) é usado para interpolar entre dois níveis de mipmap.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></p></td>
<td><p>no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Os deslocamentos de textura precisam ser estáticos. O tipo de argumento é dependente do tipo de objeto Texture. Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicando deslocamentos de coordenadas de textura</a>.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
<th>Tipo de parâmetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>INT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>Int3</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>sem suporte</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valor Retornado

O tipo de modelo da textura, que pode ser um vetor de único ou vários componentes. O formato é baseado no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)da textura.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.
2.  O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

## <a name="example"></a>Exemplo

Este exemplo de código parcial é proveniente do arquivo Instancing. FX no [exemplo Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

