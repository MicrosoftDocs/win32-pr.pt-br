---
title: Exemplo (objeto de textura DirectX HLSL)
description: Amostra uma textura. | Exemplo (objeto de textura DirectX HLSL)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825743"
---
# <a name="sample-directx-hlsl-texture-object"></a>Exemplo (objeto de textura DirectX HLSL)

Amostra uma textura.

&lt;Tipo &gt; de modelo Object. Sample (amostras de \_ estado S, local de flutuação \[ , deslocamento int \] );

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

<p> </p></td>
</tr>
<tr class="even">
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

## <a name="return-value"></a>Retornar valor

O tipo de modelo da textura, que pode ser um vetor de único ou vários componentes. O formato é baseado no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)da textura.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |

1.  O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.
2.  O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

## <a name="example"></a>Exemplo

Este exemplo de código parcial se baseia no arquivo BasicHLSL11. FX no [exemplo de BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

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

A amostragem de textura usa a posição Texel para pesquisar um valor de Texel. Um deslocamento pode ser aplicado à posição antes da pesquisa. O estado de amostra contém as opções de amostragem e filtragem. Esse método pode ser invocado dentro de um sombreador de pixel, mas não tem suporte em um sombreador de vértice ou em um sombreador de geometria.

Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados diferentes dependendo da implementação do hardware ou das configurações do driver.

### <a name="calculating-texel-positions"></a>Calculando posições texels

As coordenadas de textura são valores de ponto flutuante que referenciam dados de textura, que também são conhecidos como espaço de textura normalizado. Os modos de disposição de endereço são aplicados nesta ordem (coordenadas de textura + deslocamentos + modo de encapsulamento) para modificar as coordenadas de textura fora do \[ intervalo 0... 1 \] .

Para matrizes de textura, um valor adicional no parâmetro Location especifica um índice em uma matriz de textura. Esse índice é tratado como um valor flutuante de escala (em vez do espaço normalizado para coordenadas de textura padrão). A conversão para um índice de inteiro é feita na seguinte ordem (float + Round-to-the mais próximo inteiro + fixe para o intervalo de matriz).

### <a name="applying-texture-coordinate-offsets"></a>Aplicando deslocamentos de coordenadas de textura

O parâmetro offset modifica as coordenadas de textura, no espaço Texel. Embora as coordenadas de textura sejam números de ponto flutuante normalizados, o deslocamento aplica um deslocamento de inteiro. Observe também que os deslocamentos de textura precisam ser estáticos.

O formato de dados retornado é determinado pelo formato de textura. Por exemplo, se o recurso de textura tiver sido definido com o formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, a operação de amostragem converterá texels de amostra de gama 2,0 para 1,0, filtrará e gravará o resultado como um valor de ponto flutuante no intervalo \[ 0.. 1 \] .

## <a name="related-topics"></a>Tópicos relacionados

[Textura-objeto](dx-graphics-hlsl-to-type.md)
