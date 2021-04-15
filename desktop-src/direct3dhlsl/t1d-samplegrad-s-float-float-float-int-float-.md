---
title: 'SampleGrad:: SampleGrad (S, float, float, float, int, float) function para Texture1D'
description: A função amostra uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
keywords:
- HLSL da função SampleGrad
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968740"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="74b63-104">SampleGrad:: SampleGrad (S, float, float, float, int, float) function para Texture1D</span><span class="sxs-lookup"><span data-stu-id="74b63-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="74b63-105">Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="74b63-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b63-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74b63-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="74b63-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74b63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b63-108">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="74b63-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b63-109">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="74b63-109">Type: **SamplerState**</span></span>

<span data-ttu-id="74b63-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="74b63-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="74b63-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="74b63-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="74b63-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="74b63-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b63-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="74b63-113">Type: **float**</span></span>

<span data-ttu-id="74b63-114">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="74b63-114">The texture coordinates.</span></span> <span data-ttu-id="74b63-115">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="74b63-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="74b63-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="74b63-116">Texture-Object Type</span></span>                    | <span data-ttu-id="74b63-117">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="74b63-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="74b63-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="74b63-118">Texture1D</span></span>                              | <span data-ttu-id="74b63-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="74b63-119">float</span></span>          |
| <span data-ttu-id="74b63-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="74b63-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="74b63-121">float2</span><span class="sxs-lookup"><span data-stu-id="74b63-121">float2</span></span>         |
| <span data-ttu-id="74b63-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="74b63-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="74b63-123">float3</span><span class="sxs-lookup"><span data-stu-id="74b63-123">float3</span></span>         |
| <span data-ttu-id="74b63-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="74b63-124">TextureCubeArray</span></span>                       | <span data-ttu-id="74b63-125">float4</span><span class="sxs-lookup"><span data-stu-id="74b63-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="74b63-126">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="74b63-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b63-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="74b63-127">Type: **float**</span></span>

<span data-ttu-id="74b63-128">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="74b63-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="74b63-129">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="74b63-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="74b63-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="74b63-130">Texture-Object Type</span></span>                      | <span data-ttu-id="74b63-131">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="74b63-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="74b63-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="74b63-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="74b63-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="74b63-133">float</span></span>          |
| <span data-ttu-id="74b63-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="74b63-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="74b63-135">float2</span><span class="sxs-lookup"><span data-stu-id="74b63-135">float2</span></span>         |
| <span data-ttu-id="74b63-136">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="74b63-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="74b63-137">float3</span><span class="sxs-lookup"><span data-stu-id="74b63-137">float3</span></span>         |
| <span data-ttu-id="74b63-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="74b63-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="74b63-139">sem suporte</span><span class="sxs-lookup"><span data-stu-id="74b63-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="74b63-140">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74b63-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b63-141">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="74b63-141">Type: **float**</span></span>

<span data-ttu-id="74b63-142">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="74b63-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="74b63-143">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="74b63-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="74b63-144">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="74b63-144">Texture-Object Type</span></span>                      | <span data-ttu-id="74b63-145">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="74b63-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="74b63-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="74b63-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="74b63-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="74b63-147">float</span></span>          |
| <span data-ttu-id="74b63-148">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="74b63-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="74b63-149">float2</span><span class="sxs-lookup"><span data-stu-id="74b63-149">float2</span></span>         |
| <span data-ttu-id="74b63-150">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="74b63-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="74b63-151">float3</span><span class="sxs-lookup"><span data-stu-id="74b63-151">float3</span></span>         |
| <span data-ttu-id="74b63-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="74b63-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="74b63-153">sem suporte</span><span class="sxs-lookup"><span data-stu-id="74b63-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="74b63-154">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74b63-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b63-155">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="74b63-155">Type: **int**</span></span>

<span data-ttu-id="74b63-156">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="74b63-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="74b63-157">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="74b63-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="74b63-158">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="74b63-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="74b63-159">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="74b63-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="74b63-160">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="74b63-160">Texture-Object Type</span></span>           | <span data-ttu-id="74b63-161">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="74b63-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="74b63-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="74b63-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="74b63-163">INT</span><span class="sxs-lookup"><span data-stu-id="74b63-163">int</span></span>            |
| <span data-ttu-id="74b63-164">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="74b63-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="74b63-165">int2</span><span class="sxs-lookup"><span data-stu-id="74b63-165">int2</span></span>           |
| <span data-ttu-id="74b63-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="74b63-166">Texture3D</span></span>                     | <span data-ttu-id="74b63-167">Int3</span><span class="sxs-lookup"><span data-stu-id="74b63-167">int3</span></span>           |
| <span data-ttu-id="74b63-168">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="74b63-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="74b63-169">sem suporte</span><span class="sxs-lookup"><span data-stu-id="74b63-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="74b63-170">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74b63-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b63-171">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="74b63-171">Type: **float**</span></span>

<span data-ttu-id="74b63-172">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="74b63-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="74b63-173">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="74b63-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b63-174">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74b63-174">Return value</span></span>

<span data-ttu-id="74b63-175">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="74b63-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="74b63-176">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="74b63-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="74b63-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="74b63-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b63-178">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="74b63-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
