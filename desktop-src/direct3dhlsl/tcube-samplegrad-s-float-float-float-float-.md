---
title: 'Função SampleGrad:: SampleGrad (S, float, float, float, float) para TextureCube'
description: Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506550"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="e4f53-105">Função SampleGrad:: SampleGrad (S, float, float, float, float) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="e4f53-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="e4f53-106">Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="e4f53-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f53-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4f53-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="e4f53-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4f53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f53-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e4f53-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f53-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="e4f53-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e4f53-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e4f53-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e4f53-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="e4f53-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e4f53-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e4f53-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f53-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e4f53-114">Type: **float**</span></span>

<span data-ttu-id="e4f53-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e4f53-115">The texture coordinates.</span></span> <span data-ttu-id="e4f53-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e4f53-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e4f53-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e4f53-117">Texture-Object Type</span></span>                    | <span data-ttu-id="e4f53-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4f53-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e4f53-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e4f53-119">Texture1D</span></span>                              | <span data-ttu-id="e4f53-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e4f53-120">float</span></span>          |
| <span data-ttu-id="e4f53-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e4f53-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e4f53-122">float2</span><span class="sxs-lookup"><span data-stu-id="e4f53-122">float2</span></span>         |
| <span data-ttu-id="e4f53-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e4f53-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e4f53-124">float3</span><span class="sxs-lookup"><span data-stu-id="e4f53-124">float3</span></span>         |
| <span data-ttu-id="e4f53-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-125">TextureCubeArray</span></span>                       | <span data-ttu-id="e4f53-126">float4</span><span class="sxs-lookup"><span data-stu-id="e4f53-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e4f53-127">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e4f53-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f53-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e4f53-128">Type: **float**</span></span>

<span data-ttu-id="e4f53-129">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="e4f53-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="e4f53-130">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e4f53-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e4f53-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e4f53-131">Texture-Object Type</span></span>                      | <span data-ttu-id="e4f53-132">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4f53-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e4f53-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e4f53-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e4f53-134">float</span></span>          |
| <span data-ttu-id="e4f53-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e4f53-136">float2</span><span class="sxs-lookup"><span data-stu-id="e4f53-136">float2</span></span>         |
| <span data-ttu-id="e4f53-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e4f53-138">float3</span><span class="sxs-lookup"><span data-stu-id="e4f53-138">float3</span></span>         |
| <span data-ttu-id="e4f53-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e4f53-140">sem suporte</span><span class="sxs-lookup"><span data-stu-id="e4f53-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e4f53-141">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4f53-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f53-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e4f53-142">Type: **float**</span></span>

<span data-ttu-id="e4f53-143">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="e4f53-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="e4f53-144">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e4f53-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e4f53-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e4f53-145">Texture-Object Type</span></span>                      | <span data-ttu-id="e4f53-146">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4f53-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e4f53-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e4f53-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e4f53-148">float</span></span>          |
| <span data-ttu-id="e4f53-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e4f53-150">float2</span><span class="sxs-lookup"><span data-stu-id="e4f53-150">float2</span></span>         |
| <span data-ttu-id="e4f53-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e4f53-152">float3</span><span class="sxs-lookup"><span data-stu-id="e4f53-152">float3</span></span>         |
| <span data-ttu-id="e4f53-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e4f53-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e4f53-154">sem suporte</span><span class="sxs-lookup"><span data-stu-id="e4f53-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e4f53-155">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4f53-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f53-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e4f53-156">Type: **float**</span></span>

<span data-ttu-id="e4f53-157">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="e4f53-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e4f53-158">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="e4f53-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f53-159">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4f53-159">Return value</span></span>

<span data-ttu-id="e4f53-160">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e4f53-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e4f53-161">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e4f53-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e4f53-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4f53-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f53-163">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="e4f53-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="e4f53-164">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="e4f53-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
