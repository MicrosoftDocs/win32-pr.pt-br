---
title: 'SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) function para Texture2DArray'
description: Saiba como essa função amostra uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado. Para Texture2DArray.
ms.assetid: 71CC8747-8684-4ABD-8B7A-E02889048261
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
ms.openlocfilehash: 3d6c46deb14c3a2c3554052ecc3e6625b13b2848
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989445"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="45a41-105">SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) function para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="45a41-106">Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="45a41-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="45a41-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="45a41-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a41-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45a41-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="45a41-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45a41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45a41-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="45a41-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="45a41-111">Type: **SamplerState**</span></span>

<span data-ttu-id="45a41-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="45a41-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="45a41-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="45a41-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="45a41-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="45a41-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="45a41-115">Type: **float**</span></span>

<span data-ttu-id="45a41-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="45a41-116">The texture coordinates.</span></span> <span data-ttu-id="45a41-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="45a41-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="45a41-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="45a41-118">Texture-Object Type</span></span>                    | <span data-ttu-id="45a41-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="45a41-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="45a41-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="45a41-120">Texture1D</span></span>                              | <span data-ttu-id="45a41-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45a41-121">float</span></span>          |
| <span data-ttu-id="45a41-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="45a41-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="45a41-123">float2</span><span class="sxs-lookup"><span data-stu-id="45a41-123">float2</span></span>         |
| <span data-ttu-id="45a41-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="45a41-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="45a41-125">float3</span><span class="sxs-lookup"><span data-stu-id="45a41-125">float3</span></span>         |
| <span data-ttu-id="45a41-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="45a41-126">TextureCubeArray</span></span>                       | <span data-ttu-id="45a41-127">float4</span><span class="sxs-lookup"><span data-stu-id="45a41-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="45a41-128">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="45a41-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="45a41-129">Type: **float**</span></span>

<span data-ttu-id="45a41-130">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="45a41-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="45a41-131">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="45a41-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="45a41-132">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="45a41-132">Texture-Object Type</span></span>                      | <span data-ttu-id="45a41-133">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="45a41-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="45a41-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="45a41-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45a41-135">float</span></span>          |
| <span data-ttu-id="45a41-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="45a41-137">float2</span><span class="sxs-lookup"><span data-stu-id="45a41-137">float2</span></span>         |
| <span data-ttu-id="45a41-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="45a41-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="45a41-139">float3</span><span class="sxs-lookup"><span data-stu-id="45a41-139">float3</span></span>         |
| <span data-ttu-id="45a41-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="45a41-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="45a41-141">sem suporte</span><span class="sxs-lookup"><span data-stu-id="45a41-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="45a41-142">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45a41-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="45a41-143">Type: **float**</span></span>

<span data-ttu-id="45a41-144">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="45a41-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="45a41-145">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="45a41-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="45a41-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="45a41-146">Texture-Object Type</span></span>                      | <span data-ttu-id="45a41-147">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="45a41-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="45a41-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="45a41-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="45a41-149">float</span></span>          |
| <span data-ttu-id="45a41-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="45a41-151">float2</span><span class="sxs-lookup"><span data-stu-id="45a41-151">float2</span></span>         |
| <span data-ttu-id="45a41-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="45a41-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="45a41-153">float3</span><span class="sxs-lookup"><span data-stu-id="45a41-153">float3</span></span>         |
| <span data-ttu-id="45a41-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="45a41-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="45a41-155">sem suporte</span><span class="sxs-lookup"><span data-stu-id="45a41-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="45a41-156">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45a41-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="45a41-157">Type: **int**</span></span>

<span data-ttu-id="45a41-158">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="45a41-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="45a41-159">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="45a41-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="45a41-160">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="45a41-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="45a41-161">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="45a41-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="45a41-162">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="45a41-162">Texture-Object Type</span></span>           | <span data-ttu-id="45a41-163">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="45a41-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="45a41-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="45a41-165">INT</span><span class="sxs-lookup"><span data-stu-id="45a41-165">int</span></span>            |
| <span data-ttu-id="45a41-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="45a41-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="45a41-167">int2</span><span class="sxs-lookup"><span data-stu-id="45a41-167">int2</span></span>           |
| <span data-ttu-id="45a41-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="45a41-168">Texture3D</span></span>                     | <span data-ttu-id="45a41-169">Int3</span><span class="sxs-lookup"><span data-stu-id="45a41-169">int3</span></span>           |
| <span data-ttu-id="45a41-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="45a41-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="45a41-171">sem suporte</span><span class="sxs-lookup"><span data-stu-id="45a41-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="45a41-172">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45a41-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-173">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="45a41-173">Type: **float**</span></span>

<span data-ttu-id="45a41-174">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="45a41-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="45a41-175">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="45a41-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="45a41-176">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="45a41-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45a41-177">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="45a41-177">Type: **uint**</span></span>

<span data-ttu-id="45a41-178">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="45a41-178">The status of the operation.</span></span> <span data-ttu-id="45a41-179">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="45a41-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="45a41-180">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="45a41-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="45a41-181">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="45a41-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45a41-182">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45a41-182">Return value</span></span>

<span data-ttu-id="45a41-183">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="45a41-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="45a41-184">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="45a41-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="45a41-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="45a41-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a41-186">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="45a41-186">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="45a41-187">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="45a41-187">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
