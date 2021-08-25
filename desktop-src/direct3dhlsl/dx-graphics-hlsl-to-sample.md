---
title: Exemplo (objeto de textura DirectX HLSL)
description: Amostras de uma textura. | Exemplo (objeto de textura HLSL do DirectX)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0970b1128c8eed1983bc3741e9ff631fd9f59b70dbc75598d3631c3577580884
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950226"
---
# <a name="sample-directx-hlsl-texture-object"></a>Exemplo (objeto de textura DirectX HLSL)

Amostras de uma textura.

&lt;Template Type &gt; Object.Sample( sampler \_ state S, float Location \[ , int Offset \] );

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
<td>Qualquer <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (exceto Texture2DMS e Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Um <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>. Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Localização</em><br/></td>
<td>[in] As coordenadas de textura. O tipo de argumento depende do tipo de objeto de textura. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object tipo</th>
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

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Deslocamento</em></p></td>
<td><p>[in] Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Os deslocamentos de textura precisam ser estáticos. O tipo de argumento depende do tipo de objeto de textura. Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Aplicando deslocamentos de coordenadas de textura.</a></p>

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
<td>INT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
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

## <a name="return-value"></a>Valor retornado

O tipo de modelo da textura, que pode ser um vetor de um ou vários componentes. O formato é baseado no formato [**DXGI \_ da textura.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |

1.  TextureCubeArray está disponível no Modelo de Sombreador 4.1 ou superior.
2.  O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.

## <a name="example"></a>Exemplo

Este exemplo de código parcial baseia-se no arquivo BasicHLSL11.fx no [exemplo BasicHLSL11 .](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a>Comentários

A amostragem de textura usa a posição de texel para procurar um valor de texel. Um deslocamento pode ser aplicado à posição antes da pesquisa. O estado de amostra contém as opções de amostragem e filtragem. Esse método pode ser invocado em um sombreador de pixel, mas não tem suporte em um sombreador de vértice ou em um sombreador de geometria.

Use um deslocamento somente em um miplevel inteiro; caso contrário, você poderá obter resultados diferentes dependendo da implementação de hardware ou das configurações de driver.

### <a name="calculating-texel-positions"></a>Calculando posições de texel

As coordenadas de textura são valores de ponto flutuante que fazem referência a dados de textura, que também é conhecido como espaço de textura normalizado. Os modos de empacotamento de endereço são aplicados nessa ordem (coordenadas de textura + deslocamentos + modo de wrap) para modificar as coordenadas de textura fora do intervalo \[ 0...1. \]

Para matrizes de textura, um valor adicional no parâmetro location especifica um índice em uma matriz de textura. Esse índice é tratado como um valor float dimensionado (em vez do espaço normalizado para coordenadas de textura padrão). A conversão em um índice inteiro é feita na seguinte ordem (float + round-to-nearest-even integer + fixe para o intervalo de matriz).

### <a name="applying-texture-coordinate-offsets"></a>Aplicando deslocamentos de coordenadas de textura

O parâmetro offset modifica as coordenadas de textura, no espaço texel. Embora as coordenadas de textura sejam números de ponto flutuante normalizados, o deslocamento aplica um deslocamento inteiro. Observe também que os deslocamentos de textura precisam ser estáticos.

O formato de dados retornado é determinado pelo formato de textura. Por exemplo, se o recurso de textura foi definido com o formato DXGI \_ \_ FORMAT A8B8G8R8R8 UNORM SRGB, a operação de amostragem converte os texels amostrados de \_ gama \_ 2.0 para 1,0, filtra e grava o resultado como um valor de ponto flutuante no intervalo \[ de 0,1 \] .

## <a name="related-topics"></a>Tópicos relacionados

[Objeto de textura](dx-graphics-hlsl-to-type.md)
