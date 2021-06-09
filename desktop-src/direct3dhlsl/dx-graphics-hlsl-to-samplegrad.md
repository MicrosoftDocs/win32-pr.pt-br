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
ms.openlocfilehash: 959304d36da2b95bdf6289fba1b8c75d6ecfa314
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825733"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="3046c-104">SampleGrad (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3046c-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="3046c-105">Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.</span><span class="sxs-lookup"><span data-stu-id="3046c-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>

<span data-ttu-id="3046c-106">&lt;Tipo &gt; de modelo Object. SampleGrad (amostras de \_ estado S, local float, float campo DDX, float ddy \[ , int offset \] );</span><span class="sxs-lookup"><span data-stu-id="3046c-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="3046c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3046c-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3046c-108">Item</span><span class="sxs-lookup"><span data-stu-id="3046c-108">Item</span></span></th>
<th><span data-ttu-id="3046c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3046c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3046c-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="3046c-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="3046c-111">Qualquer tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="3046c-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-112"><span id="S"></span><span id="s"></span><em>&</em></span><span class="sxs-lookup"><span data-stu-id="3046c-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="3046c-113">no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>.</span><span class="sxs-lookup"><span data-stu-id="3046c-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="3046c-114">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="3046c-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em></span><span class="sxs-lookup"><span data-stu-id="3046c-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="3046c-116">no As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3046c-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="3046c-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3046c-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3046c-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3046c-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3046c-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3046c-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3046c-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3046c-120">Texture1D</span></span></td>
<td><span data-ttu-id="3046c-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3046c-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3046c-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="3046c-123">float2</span><span class="sxs-lookup"><span data-stu-id="3046c-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3046c-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="3046c-125">float3</span><span class="sxs-lookup"><span data-stu-id="3046c-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3046c-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3046c-127">float4</span><span class="sxs-lookup"><span data-stu-id="3046c-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3046c-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3046c-129">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3046c-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3046c-130"><span id="DDX"></span><span id="ddx"></span><em>CAMPO DDX</em></span><span class="sxs-lookup"><span data-stu-id="3046c-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="3046c-131">no A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="3046c-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="3046c-132">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3046c-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3046c-133">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3046c-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3046c-134">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3046c-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3046c-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3046c-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="3046c-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3046c-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3046c-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="3046c-138">float2</span><span class="sxs-lookup"><span data-stu-id="3046c-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3046c-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3046c-140">float3</span><span class="sxs-lookup"><span data-stu-id="3046c-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3046c-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3046c-142">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3046c-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3046c-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="3046c-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="3046c-144">no A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="3046c-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="3046c-145">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3046c-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3046c-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3046c-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3046c-147">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3046c-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3046c-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3046c-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="3046c-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3046c-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3046c-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="3046c-151">float2</span><span class="sxs-lookup"><span data-stu-id="3046c-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3046c-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3046c-153">float3</span><span class="sxs-lookup"><span data-stu-id="3046c-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3046c-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3046c-155">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3046c-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3046c-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></span><span class="sxs-lookup"><span data-stu-id="3046c-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="3046c-157">no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="3046c-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="3046c-158">O deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="3046c-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="3046c-159">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="3046c-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3046c-160">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3046c-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3046c-161">Para obter mais informações, consulte<a href="dx-graphics-hlsl-to-sample.md">aplicando deslocamentos de inteiro</a>.</span><span class="sxs-lookup"><span data-stu-id="3046c-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3046c-162">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3046c-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="3046c-163">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3046c-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3046c-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3046c-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="3046c-165">INT</span><span class="sxs-lookup"><span data-stu-id="3046c-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3046c-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="3046c-167">int2</span><span class="sxs-lookup"><span data-stu-id="3046c-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3046c-168">Texture3D</span></span></td>
<td><span data-ttu-id="3046c-169">Int3</span><span class="sxs-lookup"><span data-stu-id="3046c-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3046c-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3046c-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="3046c-171">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3046c-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3046c-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3046c-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="3046c-173">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3046c-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="3046c-174">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3046c-174">Return Value</span></span>

<span data-ttu-id="3046c-175">O tipo de modelo da textura, que pode ser um vetor de único ou vários componentes.</span><span class="sxs-lookup"><span data-stu-id="3046c-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="3046c-176">O formato é baseado no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)da textura.</span><span class="sxs-lookup"><span data-stu-id="3046c-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3046c-177">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3046c-177">Minimum Shader Model</span></span>

<span data-ttu-id="3046c-178">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3046c-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3046c-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3046c-179">vs\_4\_0</span></span> | <span data-ttu-id="3046c-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3046c-180">vs\_4\_1</span></span>  | <span data-ttu-id="3046c-181">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3046c-181">ps\_4\_0</span></span> | <span data-ttu-id="3046c-182">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3046c-182">ps\_4\_1</span></span>  | <span data-ttu-id="3046c-183">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3046c-183">gs\_4\_0</span></span> | <span data-ttu-id="3046c-184">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3046c-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="3046c-185">x</span><span class="sxs-lookup"><span data-stu-id="3046c-185">x</span></span>        | <span data-ttu-id="3046c-186">x</span><span class="sxs-lookup"><span data-stu-id="3046c-186">x</span></span>         | <span data-ttu-id="3046c-187">x</span><span class="sxs-lookup"><span data-stu-id="3046c-187">x</span></span>        | <span data-ttu-id="3046c-188">x</span><span class="sxs-lookup"><span data-stu-id="3046c-188">x</span></span>         | <span data-ttu-id="3046c-189">x</span><span class="sxs-lookup"><span data-stu-id="3046c-189">x</span></span>        | <span data-ttu-id="3046c-190">x</span><span class="sxs-lookup"><span data-stu-id="3046c-190">x</span></span>         |



 

1.  <span data-ttu-id="3046c-191">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3046c-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="3046c-192">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3046c-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="3046c-193">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3046c-193">Example</span></span>

<span data-ttu-id="3046c-194">Este exemplo de código parcial é do arquivo MotionBlur. FX no [exemplo de MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="3046c-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3046c-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3046c-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3046c-196">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="3046c-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

