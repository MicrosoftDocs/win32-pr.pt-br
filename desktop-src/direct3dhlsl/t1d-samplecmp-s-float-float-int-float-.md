---
title: 'SampleCmp:: SampleCmp (S, float, float, int, float) function para Texture1D'
description: 'Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | SampleCmp:: SampleCmp (S, float, float, int, float) function para Texture1D'
ms.assetid: 91AD0B59-D3F0-4A0D-8825-17282815D64B
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
ms.openlocfilehash: 811636e7e7002afedf026d4e3955f08f647c2c5d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989442"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="3bbb3-105">SampleCmp:: SampleCmp (S, float, float, int, float) function para Texture1D</span><span class="sxs-lookup"><span data-stu-id="3bbb3-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="3bbb3-106">Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbb3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bbb3-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="3bbb3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bbb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbb3-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3bbb3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbb3-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="3bbb3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3bbb3-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3bbb3-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3bbb3-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3bbb3-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3bbb3-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbb3-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3bbb3-114">Type: **float**</span></span>

<span data-ttu-id="3bbb3-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-115">The texture coordinates.</span></span> <span data-ttu-id="3bbb3-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3bbb3-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3bbb3-117">Texture-Object Type</span></span>                    | <span data-ttu-id="3bbb3-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bbb3-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3bbb3-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3bbb3-119">Texture1D</span></span>                              | <span data-ttu-id="3bbb3-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3bbb3-120">float</span></span>          |
| <span data-ttu-id="3bbb3-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3bbb3-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3bbb3-122">float2</span><span class="sxs-lookup"><span data-stu-id="3bbb3-122">float2</span></span>         |
| <span data-ttu-id="3bbb3-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3bbb3-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3bbb3-124">float3</span><span class="sxs-lookup"><span data-stu-id="3bbb3-124">float3</span></span>         |
| <span data-ttu-id="3bbb3-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3bbb3-125">TextureCubeArray</span></span>                       | <span data-ttu-id="3bbb3-126">float4</span><span class="sxs-lookup"><span data-stu-id="3bbb3-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3bbb3-127">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bbb3-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbb3-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3bbb3-128">Type: **float**</span></span>

<span data-ttu-id="3bbb3-129">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="3bbb3-130">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bbb3-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbb3-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3bbb3-131">Type: **int**</span></span>

<span data-ttu-id="3bbb3-132">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3bbb3-133">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3bbb3-134">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3bbb3-135">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3bbb3-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3bbb3-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3bbb3-136">Texture-Object Type</span></span>           | <span data-ttu-id="3bbb3-137">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bbb3-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3bbb3-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3bbb3-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3bbb3-139">INT</span><span class="sxs-lookup"><span data-stu-id="3bbb3-139">int</span></span>            |
| <span data-ttu-id="3bbb3-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3bbb3-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3bbb3-141">int2</span><span class="sxs-lookup"><span data-stu-id="3bbb3-141">int2</span></span>           |
| <span data-ttu-id="3bbb3-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3bbb3-142">Texture3D</span></span>                     | <span data-ttu-id="3bbb3-143">Int3</span><span class="sxs-lookup"><span data-stu-id="3bbb3-143">int3</span></span>           |
| <span data-ttu-id="3bbb3-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3bbb3-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3bbb3-145">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3bbb3-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3bbb3-146">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bbb3-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbb3-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3bbb3-147">Type: **float**</span></span>

<span data-ttu-id="3bbb3-148">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3bbb3-149">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="3bbb3-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbb3-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bbb3-150">Return value</span></span>

<span data-ttu-id="3bbb3-151">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3bbb3-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3bbb3-152">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3bbb3-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3bbb3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bbb3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbb3-154">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="3bbb3-154">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
