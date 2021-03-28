---
title: 'SampleGrad:: SampleGrad (S, float, float, float, int, float) function para Texture2DArray'
description: Saiba como essa função amostra uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para Texture2DArray.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
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
ms.openlocfilehash: 032d2b228800ffca654704c85a72d5ada76e65ef
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968744"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="ad9f9-105">SampleGrad:: SampleGrad (S, float, float, float, int, float) function para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="ad9f9-106">Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9f9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad9f9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ad9f9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad9f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9f9-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ad9f9-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ad9f9-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ad9f9-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ad9f9-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-114">Type: **float**</span></span>

<span data-ttu-id="ad9f9-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-115">The texture coordinates.</span></span> <span data-ttu-id="ad9f9-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ad9f9-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ad9f9-117">Texture-Object Type</span></span>                    | <span data-ttu-id="ad9f9-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad9f9-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ad9f9-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ad9f9-119">Texture1D</span></span>                              | <span data-ttu-id="ad9f9-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ad9f9-120">float</span></span>          |
| <span data-ttu-id="ad9f9-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ad9f9-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ad9f9-122">float2</span><span class="sxs-lookup"><span data-stu-id="ad9f9-122">float2</span></span>         |
| <span data-ttu-id="ad9f9-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ad9f9-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ad9f9-124">float3</span><span class="sxs-lookup"><span data-stu-id="ad9f9-124">float3</span></span>         |
| <span data-ttu-id="ad9f9-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-125">TextureCubeArray</span></span>                       | <span data-ttu-id="ad9f9-126">float4</span><span class="sxs-lookup"><span data-stu-id="ad9f9-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ad9f9-127">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-128">Type: **float**</span></span>

<span data-ttu-id="ad9f9-129">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="ad9f9-130">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ad9f9-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ad9f9-131">Texture-Object Type</span></span>                      | <span data-ttu-id="ad9f9-132">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad9f9-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="ad9f9-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="ad9f9-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ad9f9-134">float</span></span>          |
| <span data-ttu-id="ad9f9-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="ad9f9-136">float2</span><span class="sxs-lookup"><span data-stu-id="ad9f9-136">float2</span></span>         |
| <span data-ttu-id="ad9f9-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ad9f9-138">float3</span><span class="sxs-lookup"><span data-stu-id="ad9f9-138">float3</span></span>         |
| <span data-ttu-id="ad9f9-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="ad9f9-140">sem suporte</span><span class="sxs-lookup"><span data-stu-id="ad9f9-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ad9f9-141">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-142">Type: **float**</span></span>

<span data-ttu-id="ad9f9-143">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="ad9f9-144">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ad9f9-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ad9f9-145">Texture-Object Type</span></span>                      | <span data-ttu-id="ad9f9-146">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad9f9-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="ad9f9-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="ad9f9-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ad9f9-148">float</span></span>          |
| <span data-ttu-id="ad9f9-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="ad9f9-150">float2</span><span class="sxs-lookup"><span data-stu-id="ad9f9-150">float2</span></span>         |
| <span data-ttu-id="ad9f9-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ad9f9-152">float3</span><span class="sxs-lookup"><span data-stu-id="ad9f9-152">float3</span></span>         |
| <span data-ttu-id="ad9f9-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="ad9f9-154">sem suporte</span><span class="sxs-lookup"><span data-stu-id="ad9f9-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ad9f9-155">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-156">Type: **int**</span></span>

<span data-ttu-id="ad9f9-157">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ad9f9-158">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ad9f9-159">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ad9f9-160">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ad9f9-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ad9f9-161">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ad9f9-161">Texture-Object Type</span></span>           | <span data-ttu-id="ad9f9-162">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad9f9-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ad9f9-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ad9f9-164">INT</span><span class="sxs-lookup"><span data-stu-id="ad9f9-164">int</span></span>            |
| <span data-ttu-id="ad9f9-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ad9f9-166">int2</span><span class="sxs-lookup"><span data-stu-id="ad9f9-166">int2</span></span>           |
| <span data-ttu-id="ad9f9-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ad9f9-167">Texture3D</span></span>                     | <span data-ttu-id="ad9f9-168">Int3</span><span class="sxs-lookup"><span data-stu-id="ad9f9-168">int3</span></span>           |
| <span data-ttu-id="ad9f9-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ad9f9-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ad9f9-170">sem suporte</span><span class="sxs-lookup"><span data-stu-id="ad9f9-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ad9f9-171">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9f9-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9f9-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-172">Type: **float**</span></span>

<span data-ttu-id="ad9f9-173">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ad9f9-174">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="ad9f9-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9f9-175">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad9f9-175">Return value</span></span>

<span data-ttu-id="ad9f9-176">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ad9f9-177">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ad9f9-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ad9f9-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad9f9-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9f9-179">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="ad9f9-179">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="ad9f9-180">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="ad9f9-180">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
