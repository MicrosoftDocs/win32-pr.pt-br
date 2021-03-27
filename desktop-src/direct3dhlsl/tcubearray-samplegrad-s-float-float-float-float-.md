---
title: 'Função SampleGrad:: SampleGrad (S, float, float, float, float) para TextureCubeArray'
description: Saiba como essa função amostra uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado. Para TextureCubeArray.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664123"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="75ce6-105">Função SampleGrad:: SampleGrad (S, float, float, float, float) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="75ce6-106">Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="75ce6-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ce6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75ce6-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="75ce6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75ce6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ce6-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="75ce6-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ce6-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="75ce6-110">Type: **SamplerState**</span></span>

<span data-ttu-id="75ce6-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="75ce6-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="75ce6-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="75ce6-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="75ce6-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="75ce6-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ce6-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="75ce6-114">Type: **float**</span></span>

<span data-ttu-id="75ce6-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="75ce6-115">The texture coordinates.</span></span> <span data-ttu-id="75ce6-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="75ce6-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="75ce6-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="75ce6-117">Texture-Object Type</span></span>                    | <span data-ttu-id="75ce6-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ce6-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="75ce6-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="75ce6-119">Texture1D</span></span>                              | <span data-ttu-id="75ce6-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="75ce6-120">float</span></span>          |
| <span data-ttu-id="75ce6-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="75ce6-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="75ce6-122">float2</span><span class="sxs-lookup"><span data-stu-id="75ce6-122">float2</span></span>         |
| <span data-ttu-id="75ce6-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="75ce6-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="75ce6-124">float3</span><span class="sxs-lookup"><span data-stu-id="75ce6-124">float3</span></span>         |
| <span data-ttu-id="75ce6-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-125">TextureCubeArray</span></span>                       | <span data-ttu-id="75ce6-126">float4</span><span class="sxs-lookup"><span data-stu-id="75ce6-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="75ce6-127">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="75ce6-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ce6-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="75ce6-128">Type: **float**</span></span>

<span data-ttu-id="75ce6-129">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="75ce6-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="75ce6-130">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="75ce6-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="75ce6-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="75ce6-131">Texture-Object Type</span></span>                      | <span data-ttu-id="75ce6-132">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ce6-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="75ce6-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="75ce6-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="75ce6-134">float</span></span>          |
| <span data-ttu-id="75ce6-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="75ce6-136">float2</span><span class="sxs-lookup"><span data-stu-id="75ce6-136">float2</span></span>         |
| <span data-ttu-id="75ce6-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="75ce6-138">float3</span><span class="sxs-lookup"><span data-stu-id="75ce6-138">float3</span></span>         |
| <span data-ttu-id="75ce6-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="75ce6-140">sem suporte</span><span class="sxs-lookup"><span data-stu-id="75ce6-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="75ce6-141">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75ce6-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ce6-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="75ce6-142">Type: **float**</span></span>

<span data-ttu-id="75ce6-143">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="75ce6-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="75ce6-144">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="75ce6-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="75ce6-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="75ce6-145">Texture-Object Type</span></span>                      | <span data-ttu-id="75ce6-146">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ce6-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="75ce6-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="75ce6-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="75ce6-148">float</span></span>          |
| <span data-ttu-id="75ce6-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="75ce6-150">float2</span><span class="sxs-lookup"><span data-stu-id="75ce6-150">float2</span></span>         |
| <span data-ttu-id="75ce6-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="75ce6-152">float3</span><span class="sxs-lookup"><span data-stu-id="75ce6-152">float3</span></span>         |
| <span data-ttu-id="75ce6-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="75ce6-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="75ce6-154">sem suporte</span><span class="sxs-lookup"><span data-stu-id="75ce6-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="75ce6-155">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75ce6-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ce6-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="75ce6-156">Type: **float**</span></span>

<span data-ttu-id="75ce6-157">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="75ce6-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="75ce6-158">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="75ce6-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ce6-159">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75ce6-159">Return value</span></span>

<span data-ttu-id="75ce6-160">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="75ce6-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="75ce6-161">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="75ce6-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="75ce6-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="75ce6-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ce6-163">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="75ce6-163">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="75ce6-164">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="75ce6-164">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
