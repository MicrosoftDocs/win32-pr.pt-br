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
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="75811-103">SampleLevel (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="75811-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="75811-104">Amostra uma textura usando um deslocamento de nível mipmap.</span><span class="sxs-lookup"><span data-stu-id="75811-104">Samples a texture using a mipmap-level offset.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75811-105">&lt;Tipo &gt; de modelo Object. SampleLevel (o \_ estado de amostra S, local de flutuação, LOD flutuante \[ , deslocamento int \] );</span><span class="sxs-lookup"><span data-stu-id="75811-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span> |



 

<span data-ttu-id="75811-106">Essa função é semelhante à [amostra](dx-graphics-hlsl-to-sample.md) , exceto pelo fato de que ela usa o nível LOD (no último componente do parâmetro Location) para escolher o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="75811-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="75811-107">Por exemplo, uma textura 2D usa os dois primeiros componentes para coordenadas UV e o terceiro componente para o nível mipmap.</span><span class="sxs-lookup"><span data-stu-id="75811-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="75811-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75811-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75811-109">Item</span><span class="sxs-lookup"><span data-stu-id="75811-109">Item</span></span></th>
<th><span data-ttu-id="75811-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="75811-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75811-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="75811-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="75811-112">Qualquer tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="75811-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75811-113"><span id="S"></span><span id="s"></span><em>&</em></span><span class="sxs-lookup"><span data-stu-id="75811-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="75811-114">no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>.</span><span class="sxs-lookup"><span data-stu-id="75811-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="75811-115">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="75811-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75811-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em></span><span class="sxs-lookup"><span data-stu-id="75811-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="75811-117">no As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="75811-117">[in] The texture coordinates.</span></span> <span data-ttu-id="75811-118">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="75811-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75811-119">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="75811-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="75811-120">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="75811-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75811-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="75811-121">Texture1D</span></span></td>
<td><span data-ttu-id="75811-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="75811-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75811-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="75811-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="75811-124">float2</span><span class="sxs-lookup"><span data-stu-id="75811-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75811-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="75811-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="75811-126">float3</span><span class="sxs-lookup"><span data-stu-id="75811-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75811-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75811-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="75811-128">float4</span><span class="sxs-lookup"><span data-stu-id="75811-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="75811-129">Se o objeto de textura for uma matriz, o último componente será o índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="75811-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75811-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span><span class="sxs-lookup"><span data-stu-id="75811-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="75811-131">no Um número que especifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="75811-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="75811-132">Se o valor for = 0, o zero'th (maior mapa) será usado.</span><span class="sxs-lookup"><span data-stu-id="75811-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="75811-133">O valor fracionário (se fornecido) é usado para interpolar entre dois níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="75811-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75811-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></span><span class="sxs-lookup"><span data-stu-id="75811-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="75811-135">no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="75811-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="75811-136">Os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="75811-136">The texture offsets need to be static.</span></span> <span data-ttu-id="75811-137">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="75811-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="75811-138">Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicando deslocamentos de coordenadas de textura</a>.</span><span class="sxs-lookup"><span data-stu-id="75811-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="75811-139">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="75811-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="75811-140">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="75811-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75811-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="75811-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="75811-142">INT</span><span class="sxs-lookup"><span data-stu-id="75811-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75811-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="75811-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="75811-144">int2</span><span class="sxs-lookup"><span data-stu-id="75811-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75811-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="75811-145">Texture3D</span></span></td>
<td><span data-ttu-id="75811-146">Int3</span><span class="sxs-lookup"><span data-stu-id="75811-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75811-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75811-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="75811-148">sem suporte</span><span class="sxs-lookup"><span data-stu-id="75811-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="75811-149">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="75811-149">Return Value</span></span>

<span data-ttu-id="75811-150">O tipo de modelo da textura, que pode ser um vetor de único ou vários componentes.</span><span class="sxs-lookup"><span data-stu-id="75811-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="75811-151">O formato é baseado no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)da textura.</span><span class="sxs-lookup"><span data-stu-id="75811-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="75811-152">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="75811-152">Minimum Shader Model</span></span>

<span data-ttu-id="75811-153">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="75811-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="75811-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75811-154">vs\_4\_0</span></span> | <span data-ttu-id="75811-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="75811-155">vs\_4\_1</span></span>  | <span data-ttu-id="75811-156">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75811-156">ps\_4\_0</span></span> | <span data-ttu-id="75811-157">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="75811-157">ps\_4\_1</span></span>  | <span data-ttu-id="75811-158">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="75811-158">gs\_4\_0</span></span> | <span data-ttu-id="75811-159">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="75811-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="75811-160">x</span><span class="sxs-lookup"><span data-stu-id="75811-160">x</span></span>        | <span data-ttu-id="75811-161">x</span><span class="sxs-lookup"><span data-stu-id="75811-161">x</span></span>         | <span data-ttu-id="75811-162">x</span><span class="sxs-lookup"><span data-stu-id="75811-162">x</span></span>        | <span data-ttu-id="75811-163">x</span><span class="sxs-lookup"><span data-stu-id="75811-163">x</span></span>         | <span data-ttu-id="75811-164">x</span><span class="sxs-lookup"><span data-stu-id="75811-164">x</span></span>        | <span data-ttu-id="75811-165">x</span><span class="sxs-lookup"><span data-stu-id="75811-165">x</span></span>         |



 

1.  <span data-ttu-id="75811-166">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="75811-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="75811-167">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="75811-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="75811-168">Exemplo</span><span class="sxs-lookup"><span data-stu-id="75811-168">Example</span></span>

<span data-ttu-id="75811-169">Este exemplo de código parcial é proveniente do arquivo Instancing. FX no [exemplo Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="75811-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="75811-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75811-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75811-171">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="75811-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

