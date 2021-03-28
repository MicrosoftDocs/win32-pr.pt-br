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
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989137"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="898f3-104">Exemplo (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="898f3-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="898f3-105">Amostra uma textura.</span><span class="sxs-lookup"><span data-stu-id="898f3-105">Samples a texture.</span></span>

|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="898f3-106">&lt;Tipo &gt; de modelo Object. Sample (amostras de \_ estado S, local de flutuação \[ , deslocamento int \] );</span><span class="sxs-lookup"><span data-stu-id="898f3-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span> |

## <a name="parameters"></a><span data-ttu-id="898f3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="898f3-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="898f3-108">Item</span><span class="sxs-lookup"><span data-stu-id="898f3-108">Item</span></span></th>
<th><span data-ttu-id="898f3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="898f3-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="898f3-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="898f3-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="898f3-111">Qualquer tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="898f3-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="898f3-112"><span id="S"></span><span id="s"></span><em>&</em></span><span class="sxs-lookup"><span data-stu-id="898f3-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="898f3-113">no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>.</span><span class="sxs-lookup"><span data-stu-id="898f3-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="898f3-114">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="898f3-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="898f3-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em></span><span class="sxs-lookup"><span data-stu-id="898f3-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="898f3-116">no As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="898f3-116">[in] The texture coordinates.</span></span> <span data-ttu-id="898f3-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="898f3-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="898f3-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="898f3-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="898f3-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="898f3-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="898f3-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="898f3-120">Texture1D</span></span></td>
<td><span data-ttu-id="898f3-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="898f3-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="898f3-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="898f3-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="898f3-123">float2</span><span class="sxs-lookup"><span data-stu-id="898f3-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="898f3-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="898f3-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="898f3-125">float3</span><span class="sxs-lookup"><span data-stu-id="898f3-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="898f3-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="898f3-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="898f3-127">float4</span><span class="sxs-lookup"><span data-stu-id="898f3-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898f3-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></span><span class="sxs-lookup"><span data-stu-id="898f3-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="898f3-129">no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="898f3-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="898f3-130">Os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="898f3-130">The texture offsets need to be static.</span></span> <span data-ttu-id="898f3-131">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="898f3-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="898f3-132">Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicando deslocamentos de coordenadas de textura</a>.</span><span class="sxs-lookup"><span data-stu-id="898f3-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="898f3-133">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="898f3-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="898f3-134">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="898f3-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="898f3-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="898f3-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="898f3-136">INT</span><span class="sxs-lookup"><span data-stu-id="898f3-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="898f3-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="898f3-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="898f3-138">int2</span><span class="sxs-lookup"><span data-stu-id="898f3-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="898f3-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="898f3-139">Texture3D</span></span></td>
<td><span data-ttu-id="898f3-140">Int3</span><span class="sxs-lookup"><span data-stu-id="898f3-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="898f3-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="898f3-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="898f3-142">sem suporte</span><span class="sxs-lookup"><span data-stu-id="898f3-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="898f3-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="898f3-143">Return value</span></span>

<span data-ttu-id="898f3-144">O tipo de modelo da textura, que pode ser um vetor de único ou vários componentes.</span><span class="sxs-lookup"><span data-stu-id="898f3-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="898f3-145">O formato é baseado no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)da textura.</span><span class="sxs-lookup"><span data-stu-id="898f3-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="898f3-146">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="898f3-146">Minimum Shader Model</span></span>

<span data-ttu-id="898f3-147">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="898f3-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="898f3-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="898f3-148">vs\_4\_0</span></span> | <span data-ttu-id="898f3-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="898f3-149">vs\_4\_1</span></span>  | <span data-ttu-id="898f3-150">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="898f3-150">ps\_4\_0</span></span> | <span data-ttu-id="898f3-151">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="898f3-151">ps\_4\_1</span></span>  | <span data-ttu-id="898f3-152">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="898f3-152">gs\_4\_0</span></span> | <span data-ttu-id="898f3-153">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="898f3-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="898f3-154">x</span><span class="sxs-lookup"><span data-stu-id="898f3-154">x</span></span>        | <span data-ttu-id="898f3-155">x</span><span class="sxs-lookup"><span data-stu-id="898f3-155">x</span></span>         |          |           |

1.  <span data-ttu-id="898f3-156">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="898f3-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="898f3-157">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="898f3-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="898f3-158">Exemplo</span><span class="sxs-lookup"><span data-stu-id="898f3-158">Example</span></span>

<span data-ttu-id="898f3-159">Este exemplo de código parcial se baseia no arquivo BasicHLSL11. FX no [exemplo de BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span><span class="sxs-lookup"><span data-stu-id="898f3-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

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

## <a name="remarks"></a><span data-ttu-id="898f3-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="898f3-160">Remarks</span></span>

<span data-ttu-id="898f3-161">A amostragem de textura usa a posição Texel para pesquisar um valor de Texel.</span><span class="sxs-lookup"><span data-stu-id="898f3-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="898f3-162">Um deslocamento pode ser aplicado à posição antes da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="898f3-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="898f3-163">O estado de amostra contém as opções de amostragem e filtragem.</span><span class="sxs-lookup"><span data-stu-id="898f3-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="898f3-164">Esse método pode ser invocado dentro de um sombreador de pixel, mas não tem suporte em um sombreador de vértice ou em um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="898f3-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="898f3-165">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados diferentes dependendo da implementação do hardware ou das configurações do driver.</span><span class="sxs-lookup"><span data-stu-id="898f3-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="898f3-166">Calculando posições texels</span><span class="sxs-lookup"><span data-stu-id="898f3-166">Calculating texel positions</span></span>

<span data-ttu-id="898f3-167">As coordenadas de textura são valores de ponto flutuante que referenciam dados de textura, que também são conhecidos como espaço de textura normalizado.</span><span class="sxs-lookup"><span data-stu-id="898f3-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="898f3-168">Os modos de disposição de endereço são aplicados nesta ordem (coordenadas de textura + deslocamentos + modo de encapsulamento) para modificar as coordenadas de textura fora do \[ intervalo 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="898f3-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="898f3-169">Para matrizes de textura, um valor adicional no parâmetro Location especifica um índice em uma matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="898f3-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="898f3-170">Esse índice é tratado como um valor flutuante de escala (em vez do espaço normalizado para coordenadas de textura padrão).</span><span class="sxs-lookup"><span data-stu-id="898f3-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="898f3-171">A conversão para um índice de inteiro é feita na seguinte ordem (float + Round-to-the mais próximo inteiro + fixe para o intervalo de matriz).</span><span class="sxs-lookup"><span data-stu-id="898f3-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="898f3-172">Aplicando deslocamentos de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="898f3-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="898f3-173">O parâmetro offset modifica as coordenadas de textura, no espaço Texel.</span><span class="sxs-lookup"><span data-stu-id="898f3-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="898f3-174">Embora as coordenadas de textura sejam números de ponto flutuante normalizados, o deslocamento aplica um deslocamento de inteiro.</span><span class="sxs-lookup"><span data-stu-id="898f3-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="898f3-175">Observe também que os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="898f3-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="898f3-176">O formato de dados retornado é determinado pelo formato de textura.</span><span class="sxs-lookup"><span data-stu-id="898f3-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="898f3-177">Por exemplo, se o recurso de textura tiver sido definido com o formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, a operação de amostragem converterá texels de amostra de gama 2,0 para 1,0, filtrará e gravará o resultado como um valor de ponto flutuante no intervalo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="898f3-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="898f3-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="898f3-178">Related topics</span></span>

[<span data-ttu-id="898f3-179">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="898f3-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
