---
title: SampleLevel (objeto de textura HLSL do DirectX)
description: Amostra uma textura usando um deslocamento no nível de mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826680"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="35b88-103">SampleLevel (objeto de textura HLSL do DirectX)</span><span class="sxs-lookup"><span data-stu-id="35b88-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="35b88-104">Amostra uma textura usando um deslocamento no nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="35b88-104">Samples a texture using a mipmap-level offset.</span></span>

<span data-ttu-id="35b88-105">&lt;Template Type &gt; Object.SampleLevel( sampler \_ state S, float Location, float LOD \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="35b88-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span>



 

<span data-ttu-id="35b88-106">Essa função é semelhante a [Sample,](dx-graphics-hlsl-to-sample.md) exceto que ela usa o nível LOD (no último componente do parâmetro location) para escolher o nível mipmap.</span><span class="sxs-lookup"><span data-stu-id="35b88-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="35b88-107">Por exemplo, uma textura 2D usa os dois primeiros componentes para coordenadas uv e o terceiro componente para o nível mipmap.</span><span class="sxs-lookup"><span data-stu-id="35b88-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="35b88-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35b88-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35b88-109">Item</span><span class="sxs-lookup"><span data-stu-id="35b88-109">Item</span></span></th>
<th><span data-ttu-id="35b88-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b88-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35b88-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="35b88-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="35b88-112">Qualquer <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (exceto Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="35b88-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b88-113"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="35b88-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="35b88-114">[in] Um <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>.</span><span class="sxs-lookup"><span data-stu-id="35b88-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="35b88-115">Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="35b88-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b88-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Localização</em></span><span class="sxs-lookup"><span data-stu-id="35b88-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="35b88-117">[in] As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="35b88-117">[in] The texture coordinates.</span></span> <span data-ttu-id="35b88-118">O tipo de argumento depende do tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="35b88-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="35b88-119">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="35b88-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="35b88-120">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="35b88-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35b88-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="35b88-121">Texture1D</span></span></td>
<td><span data-ttu-id="35b88-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="35b88-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b88-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="35b88-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="35b88-124">float2</span><span class="sxs-lookup"><span data-stu-id="35b88-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b88-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="35b88-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="35b88-126">float3</span><span class="sxs-lookup"><span data-stu-id="35b88-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b88-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="35b88-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="35b88-128">float4</span><span class="sxs-lookup"><span data-stu-id="35b88-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="35b88-129">Se o objeto de textura for uma matriz, o último componente será o índice da matriz.</span><span class="sxs-lookup"><span data-stu-id="35b88-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35b88-130"><span id="LOD"></span><span id="lod"></span><em>Lod</em></span><span class="sxs-lookup"><span data-stu-id="35b88-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="35b88-131">[in] Um número que especifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="35b88-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="35b88-132">Se o valor for = 0, o zero (maior mapa) será usado.</span><span class="sxs-lookup"><span data-stu-id="35b88-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="35b88-133">O valor fracionado (se fornecido) é usado para interpolar entre dois níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="35b88-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35b88-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Deslocamento</em></span><span class="sxs-lookup"><span data-stu-id="35b88-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="35b88-135">[in] Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="35b88-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="35b88-136">Os deslocamentos de textura precisam ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="35b88-136">The texture offsets need to be static.</span></span> <span data-ttu-id="35b88-137">O tipo de argumento depende do tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="35b88-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="35b88-138">Para obter mais informações, consulte <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Aplicando deslocamentos de coordenadas de textura.</a></span><span class="sxs-lookup"><span data-stu-id="35b88-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="35b88-139">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="35b88-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="35b88-140">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="35b88-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35b88-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="35b88-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="35b88-142">INT</span><span class="sxs-lookup"><span data-stu-id="35b88-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b88-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="35b88-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="35b88-144">int2</span><span class="sxs-lookup"><span data-stu-id="35b88-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b88-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="35b88-145">Texture3D</span></span></td>
<td><span data-ttu-id="35b88-146">int3</span><span class="sxs-lookup"><span data-stu-id="35b88-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b88-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="35b88-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="35b88-148">sem suporte</span><span class="sxs-lookup"><span data-stu-id="35b88-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="35b88-149">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="35b88-149">Return Value</span></span>

<span data-ttu-id="35b88-150">O tipo de modelo da textura, que pode ser um vetor de um ou vários componentes.</span><span class="sxs-lookup"><span data-stu-id="35b88-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="35b88-151">O formato é baseado no formato [**DXGI \_ da textura.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="35b88-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="35b88-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="35b88-152">Minimum Shader Model</span></span>

<span data-ttu-id="35b88-153">Essa função tem suporte nos modelos de sombreador a seguir.</span><span class="sxs-lookup"><span data-stu-id="35b88-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="35b88-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35b88-154">vs\_4\_0</span></span> | <span data-ttu-id="35b88-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="35b88-155">vs\_4\_1</span></span>  | <span data-ttu-id="35b88-156">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35b88-156">ps\_4\_0</span></span> | <span data-ttu-id="35b88-157">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="35b88-157">ps\_4\_1</span></span>  | <span data-ttu-id="35b88-158">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35b88-158">gs\_4\_0</span></span> | <span data-ttu-id="35b88-159">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="35b88-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="35b88-160">x</span><span class="sxs-lookup"><span data-stu-id="35b88-160">x</span></span>        | <span data-ttu-id="35b88-161">x</span><span class="sxs-lookup"><span data-stu-id="35b88-161">x</span></span>         | <span data-ttu-id="35b88-162">x</span><span class="sxs-lookup"><span data-stu-id="35b88-162">x</span></span>        | <span data-ttu-id="35b88-163">x</span><span class="sxs-lookup"><span data-stu-id="35b88-163">x</span></span>         | <span data-ttu-id="35b88-164">x</span><span class="sxs-lookup"><span data-stu-id="35b88-164">x</span></span>        | <span data-ttu-id="35b88-165">x</span><span class="sxs-lookup"><span data-stu-id="35b88-165">x</span></span>         |



 

1.  <span data-ttu-id="35b88-166">TextureCubeArray está disponível no Modelo de Sombreador 4.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="35b88-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="35b88-167">O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="35b88-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="35b88-168">Exemplo</span><span class="sxs-lookup"><span data-stu-id="35b88-168">Example</span></span>

<span data-ttu-id="35b88-169">Este exemplo de código parcial é do arquivo Instancing.fx no [Exemplo instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="35b88-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="35b88-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35b88-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b88-171">Objeto de textura</span><span class="sxs-lookup"><span data-stu-id="35b88-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

