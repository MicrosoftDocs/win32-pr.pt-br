---
title: 'SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) function para Texture2D'
description: Amostras de um Texture2D, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe de exemplo de valores LOD (nível de detalhe) de amostra.
ms.assetid: 896497E1-A795-4674-AB41-2440A7D0CC76
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
ms.openlocfilehash: 9f1909c792863a3b480b6bdec553db58f7ff8492
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989449"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="e99e2-104">SampleGrad:: SampleGrad (S, float, float, float, int, float, uint) function para Texture2D</span><span class="sxs-lookup"><span data-stu-id="e99e2-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="e99e2-105">Amostras de um [**Texture2D**](sm5-object-texture2d.md), usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe de exemplo de valores LOD (nível de detalhe) de amostra.</span><span class="sxs-lookup"><span data-stu-id="e99e2-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e99e2-106">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="e99e2-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e99e2-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e99e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e99e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99e2-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="e99e2-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e99e2-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e99e2-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e99e2-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="e99e2-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e99e2-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99e2-114">Type: **float**</span></span>

<span data-ttu-id="e99e2-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e99e2-115">The texture coordinates.</span></span> <span data-ttu-id="e99e2-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e99e2-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e99e2-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e99e2-117">Texture-Object Type</span></span>                    | <span data-ttu-id="e99e2-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e99e2-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e99e2-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e99e2-119">Texture1D</span></span>                              | <span data-ttu-id="e99e2-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e99e2-120">float</span></span>          |
| <span data-ttu-id="e99e2-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e99e2-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e99e2-122">float2</span><span class="sxs-lookup"><span data-stu-id="e99e2-122">float2</span></span>         |
| <span data-ttu-id="e99e2-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e99e2-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e99e2-124">float3</span><span class="sxs-lookup"><span data-stu-id="e99e2-124">float3</span></span>         |
| <span data-ttu-id="e99e2-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-125">TextureCubeArray</span></span>                       | <span data-ttu-id="e99e2-126">float4</span><span class="sxs-lookup"><span data-stu-id="e99e2-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e99e2-127">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99e2-128">Type: **float**</span></span>

<span data-ttu-id="e99e2-129">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="e99e2-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="e99e2-130">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e99e2-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e99e2-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e99e2-131">Texture-Object Type</span></span>                      | <span data-ttu-id="e99e2-132">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e99e2-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e99e2-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e99e2-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e99e2-134">float</span></span>          |
| <span data-ttu-id="e99e2-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e99e2-136">float2</span><span class="sxs-lookup"><span data-stu-id="e99e2-136">float2</span></span>         |
| <span data-ttu-id="e99e2-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e99e2-138">float3</span><span class="sxs-lookup"><span data-stu-id="e99e2-138">float3</span></span>         |
| <span data-ttu-id="e99e2-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e99e2-140">sem suporte</span><span class="sxs-lookup"><span data-stu-id="e99e2-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e99e2-141">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99e2-142">Type: **float**</span></span>

<span data-ttu-id="e99e2-143">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="e99e2-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="e99e2-144">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e99e2-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e99e2-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e99e2-145">Texture-Object Type</span></span>                      | <span data-ttu-id="e99e2-146">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e99e2-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e99e2-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e99e2-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e99e2-148">float</span></span>          |
| <span data-ttu-id="e99e2-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e99e2-150">float2</span><span class="sxs-lookup"><span data-stu-id="e99e2-150">float2</span></span>         |
| <span data-ttu-id="e99e2-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e99e2-152">float3</span><span class="sxs-lookup"><span data-stu-id="e99e2-152">float3</span></span>         |
| <span data-ttu-id="e99e2-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e99e2-154">sem suporte</span><span class="sxs-lookup"><span data-stu-id="e99e2-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e99e2-155">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="e99e2-156">Type: **int**</span></span>

<span data-ttu-id="e99e2-157">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e99e2-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e99e2-158">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="e99e2-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e99e2-159">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e99e2-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e99e2-160">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e99e2-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e99e2-161">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e99e2-161">Texture-Object Type</span></span>           | <span data-ttu-id="e99e2-162">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e99e2-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e99e2-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e99e2-164">INT</span><span class="sxs-lookup"><span data-stu-id="e99e2-164">int</span></span>            |
| <span data-ttu-id="e99e2-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e99e2-166">int2</span><span class="sxs-lookup"><span data-stu-id="e99e2-166">int2</span></span>           |
| <span data-ttu-id="e99e2-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e99e2-167">Texture3D</span></span>                     | <span data-ttu-id="e99e2-168">Int3</span><span class="sxs-lookup"><span data-stu-id="e99e2-168">int3</span></span>           |
| <span data-ttu-id="e99e2-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e99e2-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e99e2-170">sem suporte</span><span class="sxs-lookup"><span data-stu-id="e99e2-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e99e2-171">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e99e2-172">Type: **float**</span></span>

<span data-ttu-id="e99e2-173">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="e99e2-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e99e2-174">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="e99e2-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e99e2-175">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-176">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e99e2-176">Type: **uint**</span></span>

<span data-ttu-id="e99e2-177">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="e99e2-177">The status of the operation.</span></span> <span data-ttu-id="e99e2-178">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e99e2-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e99e2-179">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e99e2-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e99e2-180">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="e99e2-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99e2-181">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e99e2-181">Return value</span></span>

<span data-ttu-id="e99e2-182">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e99e2-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e99e2-183">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e99e2-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e99e2-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="e99e2-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99e2-185">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="e99e2-185">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
