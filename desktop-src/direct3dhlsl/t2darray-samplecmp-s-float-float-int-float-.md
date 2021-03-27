---
title: 'SampleCmp:: SampleCmp (S, float, float, int, float) function para Texture2DArray'
description: Saiba como essa função amostra uma textura usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para Texture2DArray.
ms.assetid: 6455BF80-2A22-43BB-80A2-61FBEC66C348
keywords:
- HLSL da função SampleCmp
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0692166766b9f52a1b6b13719c2427438b59835f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664132"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="73ea4-105">SampleCmp:: SampleCmp (S, float, float, int, float) function para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="73ea4-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="73ea4-106">Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="73ea4-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ea4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73ea4-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="73ea4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73ea4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ea4-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="73ea4-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea4-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="73ea4-110">Type: **SamplerState**</span></span>

<span data-ttu-id="73ea4-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="73ea4-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="73ea4-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="73ea4-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="73ea4-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="73ea4-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea4-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="73ea4-114">Type: **float**</span></span>

<span data-ttu-id="73ea4-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="73ea4-115">The texture coordinates.</span></span> <span data-ttu-id="73ea4-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="73ea4-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="73ea4-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="73ea4-117">Texture-Object Type</span></span>                    | <span data-ttu-id="73ea4-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="73ea4-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="73ea4-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73ea4-119">Texture1D</span></span>                              | <span data-ttu-id="73ea4-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="73ea4-120">float</span></span>          |
| <span data-ttu-id="73ea4-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="73ea4-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="73ea4-122">float2</span><span class="sxs-lookup"><span data-stu-id="73ea4-122">float2</span></span>         |
| <span data-ttu-id="73ea4-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="73ea4-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="73ea4-124">float3</span><span class="sxs-lookup"><span data-stu-id="73ea4-124">float3</span></span>         |
| <span data-ttu-id="73ea4-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="73ea4-125">TextureCubeArray</span></span>                       | <span data-ttu-id="73ea4-126">float4</span><span class="sxs-lookup"><span data-stu-id="73ea4-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="73ea4-127">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea4-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea4-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="73ea4-128">Type: **float**</span></span>

<span data-ttu-id="73ea4-129">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="73ea4-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="73ea4-130">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea4-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea4-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="73ea4-131">Type: **int**</span></span>

<span data-ttu-id="73ea4-132">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="73ea4-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="73ea4-133">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="73ea4-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="73ea4-134">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="73ea4-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="73ea4-135">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="73ea4-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="73ea4-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="73ea4-136">Texture-Object Type</span></span>           | <span data-ttu-id="73ea4-137">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="73ea4-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="73ea4-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="73ea4-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="73ea4-139">INT</span><span class="sxs-lookup"><span data-stu-id="73ea4-139">int</span></span>            |
| <span data-ttu-id="73ea4-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="73ea4-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="73ea4-141">int2</span><span class="sxs-lookup"><span data-stu-id="73ea4-141">int2</span></span>           |
| <span data-ttu-id="73ea4-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73ea4-142">Texture3D</span></span>                     | <span data-ttu-id="73ea4-143">Int3</span><span class="sxs-lookup"><span data-stu-id="73ea4-143">int3</span></span>           |
| <span data-ttu-id="73ea4-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="73ea4-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="73ea4-145">sem suporte</span><span class="sxs-lookup"><span data-stu-id="73ea4-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="73ea4-146">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ea4-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ea4-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="73ea4-147">Type: **float**</span></span>

<span data-ttu-id="73ea4-148">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="73ea4-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="73ea4-149">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="73ea4-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ea4-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73ea4-150">Return value</span></span>

<span data-ttu-id="73ea4-151">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="73ea4-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="73ea4-152">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="73ea4-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="73ea4-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="73ea4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ea4-154">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="73ea4-154">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> </dl>

 

 
