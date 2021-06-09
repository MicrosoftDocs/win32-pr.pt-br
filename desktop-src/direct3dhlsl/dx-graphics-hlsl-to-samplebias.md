---
title: SampleBias (objeto de textura DirectX HLSL)
description: Amostra uma textura, depois de aplicar a tendência de entrada ao nível de mipmap.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01087ab36bdbe90ff73643899229c7ec6ccfbdbe
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826791"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="69834-103">SampleBias (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69834-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="69834-104">Amostra uma textura, depois de aplicar a tendência de entrada ao nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="69834-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>

<span data-ttu-id="69834-105">&lt;Tipo de modelo &gt; Object. SampleBias (amostras de \_ estado S, local de flutuação, inclinação flutuante \[ , deslocamento int \] );</span><span class="sxs-lookup"><span data-stu-id="69834-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="69834-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69834-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69834-107">Item</span><span class="sxs-lookup"><span data-stu-id="69834-107">Item</span></span></th>
<th><span data-ttu-id="69834-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="69834-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="69834-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="69834-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="69834-110">Qualquer tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="69834-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69834-111"><span id="S"></span><span id="s"></span><em>&</em></span><span class="sxs-lookup"><span data-stu-id="69834-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="69834-112">no Um <a href="dx-graphics-hlsl-sampler.md">estado de amostra</a>.</span><span class="sxs-lookup"><span data-stu-id="69834-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="69834-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="69834-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69834-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Local</em></span><span class="sxs-lookup"><span data-stu-id="69834-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="69834-115">no As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="69834-115">[in] The texture coordinates.</span></span> <span data-ttu-id="69834-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="69834-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="69834-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="69834-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="69834-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="69834-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="69834-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="69834-119">Texture1D</span></span></td>
<td><span data-ttu-id="69834-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="69834-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69834-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="69834-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="69834-122">float2</span><span class="sxs-lookup"><span data-stu-id="69834-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69834-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="69834-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="69834-124">float3</span><span class="sxs-lookup"><span data-stu-id="69834-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69834-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="69834-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="69834-126">float4</span><span class="sxs-lookup"><span data-stu-id="69834-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69834-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span><span class="sxs-lookup"><span data-stu-id="69834-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="69834-128">no O valor de tendência, que é um número de ponto flutuante entre-16,0 e 15,99, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="69834-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69834-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Desvio</em></span><span class="sxs-lookup"><span data-stu-id="69834-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="69834-130">no Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="69834-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="69834-131">Os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="69834-131">The texture offsets need to be static.</span></span> <span data-ttu-id="69834-132">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="69834-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="69834-133">Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicando deslocamentos de coordenadas de textura</a>.</span><span class="sxs-lookup"><span data-stu-id="69834-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="69834-134">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="69834-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="69834-135">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="69834-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="69834-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="69834-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="69834-137">INT</span><span class="sxs-lookup"><span data-stu-id="69834-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69834-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="69834-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="69834-139">int2</span><span class="sxs-lookup"><span data-stu-id="69834-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69834-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="69834-140">Texture3D</span></span></td>
<td><span data-ttu-id="69834-141">Int3</span><span class="sxs-lookup"><span data-stu-id="69834-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69834-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="69834-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="69834-143">sem suporte</span><span class="sxs-lookup"><span data-stu-id="69834-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="69834-144">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="69834-144">Return Value</span></span>

<span data-ttu-id="69834-145">O tipo de modelo da textura, que pode ser um vetor de único ou vários componentes.</span><span class="sxs-lookup"><span data-stu-id="69834-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="69834-146">O formato é baseado no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)da textura.</span><span class="sxs-lookup"><span data-stu-id="69834-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="69834-147">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="69834-147">Minimum Shader Model</span></span>

<span data-ttu-id="69834-148">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="69834-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69834-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69834-149">vs\_4\_0</span></span> | <span data-ttu-id="69834-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="69834-150">vs\_4\_1</span></span>  | <span data-ttu-id="69834-151">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69834-151">ps\_4\_0</span></span> | <span data-ttu-id="69834-152">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="69834-152">ps\_4\_1</span></span>  | <span data-ttu-id="69834-153">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="69834-153">gs\_4\_0</span></span> | <span data-ttu-id="69834-154">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="69834-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="69834-155">x</span><span class="sxs-lookup"><span data-stu-id="69834-155">x</span></span>        | <span data-ttu-id="69834-156">x</span><span class="sxs-lookup"><span data-stu-id="69834-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="69834-157">O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="69834-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="69834-158">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="69834-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69834-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69834-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69834-160">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="69834-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

