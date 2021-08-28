---
title: SampleGrad (objeto de textura DirectX HLSL)
description: Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado. | SampleGrad (objeto de textura DirectX HLSL)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e315cfc32b10274eee47258360e85543f15311a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624092"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a>SampleGrad (objeto de textura DirectX HLSL)

Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.

&lt;Tipo &gt; de modelo Object. SampleGrad (amostras de \_ estado S, local float, float campo DDX, float ddy \[ , int offset \] );



 

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
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>sem suporte</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="DDX"></span><span id="ddx"></span><em>CAMPO DDX</em></p></td>
<td><p>no A taxa de alteração da geometria da superfície na direção x. O tipo de argumento é dependente do tipo de objeto Texture.</p>

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
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>sem suporte</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span id="DDY"></span><span id="ddy"></span><em>DDY</em></p></td>
<td><p>no A taxa de alteração da geometria da superfície na direção y. O tipo de argumento é dependente do tipo de objeto Texture.</p>

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
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>sem suporte</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></p></td>
<td><p>no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura. O deslocamento é aplicado ao local antes da amostragem. Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware. O tipo de argumento é dependente do tipo de objeto Texture. Para obter mais informações, consulte<a href="dx-graphics-hlsl-to-sample.md">aplicando deslocamentos de inteiro</a>.</p>

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
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
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

Este exemplo de código parcial é do arquivo MotionBlur. FX no [exemplo de MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

