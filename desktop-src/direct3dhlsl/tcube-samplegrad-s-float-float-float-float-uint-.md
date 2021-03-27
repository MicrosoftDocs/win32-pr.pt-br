---
title: 'Função SampleGrad:: SampleGrad (S, float, float, float, float, uint) para TextureCube'
description: Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para TextureCube.
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
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
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506541"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="8d9ea-105">Função SampleGrad:: SampleGrad (S, float, float, float, float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="8d9ea-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="8d9ea-106">Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="8d9ea-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d9ea-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8d9ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d9ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9ea-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="8d9ea-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ea-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-111">Type: **SamplerState**</span></span>

<span data-ttu-id="8d9ea-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="8d9ea-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="8d9ea-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="8d9ea-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8d9ea-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ea-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-115">Type: **float**</span></span>

<span data-ttu-id="8d9ea-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-116">The texture coordinates.</span></span> <span data-ttu-id="8d9ea-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8d9ea-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8d9ea-118">Texture-Object Type</span></span>                    | <span data-ttu-id="8d9ea-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d9ea-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="8d9ea-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8d9ea-120">Texture1D</span></span>                              | <span data-ttu-id="8d9ea-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8d9ea-121">float</span></span>          |
| <span data-ttu-id="8d9ea-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="8d9ea-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="8d9ea-123">float2</span><span class="sxs-lookup"><span data-stu-id="8d9ea-123">float2</span></span>         |
| <span data-ttu-id="8d9ea-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="8d9ea-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="8d9ea-125">float3</span><span class="sxs-lookup"><span data-stu-id="8d9ea-125">float3</span></span>         |
| <span data-ttu-id="8d9ea-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-126">TextureCubeArray</span></span>                       | <span data-ttu-id="8d9ea-127">float4</span><span class="sxs-lookup"><span data-stu-id="8d9ea-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="8d9ea-128">*Campo DDX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="8d9ea-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ea-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-129">Type: **float**</span></span>

<span data-ttu-id="8d9ea-130">A taxa de alteração da geometria da superfície na direção x.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="8d9ea-131">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8d9ea-132">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8d9ea-132">Texture-Object Type</span></span>                      | <span data-ttu-id="8d9ea-133">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d9ea-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="8d9ea-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="8d9ea-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8d9ea-135">float</span></span>          |
| <span data-ttu-id="8d9ea-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="8d9ea-137">float2</span><span class="sxs-lookup"><span data-stu-id="8d9ea-137">float2</span></span>         |
| <span data-ttu-id="8d9ea-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8d9ea-139">float3</span><span class="sxs-lookup"><span data-stu-id="8d9ea-139">float3</span></span>         |
| <span data-ttu-id="8d9ea-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="8d9ea-141">sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d9ea-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8d9ea-142">*Ddy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d9ea-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ea-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-143">Type: **float**</span></span>

<span data-ttu-id="8d9ea-144">A taxa de alteração da geometria da superfície na direção y.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="8d9ea-145">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8d9ea-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8d9ea-146">Texture-Object Type</span></span>                      | <span data-ttu-id="8d9ea-147">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d9ea-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="8d9ea-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="8d9ea-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8d9ea-149">float</span></span>          |
| <span data-ttu-id="8d9ea-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="8d9ea-151">float2</span><span class="sxs-lookup"><span data-stu-id="8d9ea-151">float2</span></span>         |
| <span data-ttu-id="8d9ea-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8d9ea-153">float3</span><span class="sxs-lookup"><span data-stu-id="8d9ea-153">float3</span></span>         |
| <span data-ttu-id="8d9ea-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8d9ea-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="8d9ea-155">sem suporte</span><span class="sxs-lookup"><span data-stu-id="8d9ea-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8d9ea-156">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d9ea-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ea-157">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-157">Type: **float**</span></span>

<span data-ttu-id="8d9ea-158">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="8d9ea-159">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="8d9ea-160">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8d9ea-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ea-161">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-161">Type: **uint**</span></span>

<span data-ttu-id="8d9ea-162">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-162">The status of the operation.</span></span> <span data-ttu-id="8d9ea-163">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8d9ea-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8d9ea-164">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8d9ea-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8d9ea-165">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="8d9ea-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9ea-166">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d9ea-166">Return value</span></span>

<span data-ttu-id="8d9ea-167">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="8d9ea-168">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="8d9ea-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="8d9ea-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d9ea-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9ea-170">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="8d9ea-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="8d9ea-171">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="8d9ea-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
