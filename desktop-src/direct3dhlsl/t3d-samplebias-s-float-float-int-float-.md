---
title: 'SampleBias:: SampleBias (S, float, float, int, float) function para Texture3D'
description: 'A função SampleBias:: SampleBias (S, float, float, int, float) para o Texture3D amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.'
keywords:
- HLSL da função SampleBias
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7ef038a3faa4cb0a208e9a9d05de230d2b87231
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187919"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="fd951-104">SampleBias:: SampleBias (S, float, float, int, float) function para Texture3D</span><span class="sxs-lookup"><span data-stu-id="fd951-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="fd951-105">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="fd951-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd951-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd951-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="fd951-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd951-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd951-108">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fd951-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd951-109">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="fd951-109">Type: **SamplerState**</span></span>

<span data-ttu-id="fd951-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="fd951-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fd951-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="fd951-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fd951-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="fd951-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd951-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fd951-113">Type: **float**</span></span>

<span data-ttu-id="fd951-114">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fd951-114">The texture coordinates.</span></span> <span data-ttu-id="fd951-115">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="fd951-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fd951-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fd951-116">Texture-Object Type</span></span>                    | <span data-ttu-id="fd951-117">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd951-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fd951-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fd951-118">Texture1D</span></span>                              | <span data-ttu-id="fd951-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fd951-119">float</span></span>          |
| <span data-ttu-id="fd951-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="fd951-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fd951-121">float2</span><span class="sxs-lookup"><span data-stu-id="fd951-121">float2</span></span>         |
| <span data-ttu-id="fd951-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fd951-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fd951-123">float3</span><span class="sxs-lookup"><span data-stu-id="fd951-123">float3</span></span>         |
| <span data-ttu-id="fd951-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fd951-124">TextureCubeArray</span></span>                       | <span data-ttu-id="fd951-125">float4</span><span class="sxs-lookup"><span data-stu-id="fd951-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fd951-126">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd951-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd951-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fd951-127">Type: **float**</span></span>

<span data-ttu-id="fd951-128">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="fd951-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fd951-129">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd951-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd951-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fd951-130">Type: **int**</span></span>

<span data-ttu-id="fd951-131">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="fd951-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="fd951-132">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="fd951-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="fd951-133">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="fd951-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="fd951-134">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fd951-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="fd951-135">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="fd951-135">Texture-Object Type</span></span>           | <span data-ttu-id="fd951-136">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd951-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="fd951-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fd951-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="fd951-138">INT</span><span class="sxs-lookup"><span data-stu-id="fd951-138">int</span></span>            |
| <span data-ttu-id="fd951-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fd951-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="fd951-140">int2</span><span class="sxs-lookup"><span data-stu-id="fd951-140">int2</span></span>           |
| <span data-ttu-id="fd951-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fd951-141">Texture3D</span></span>                     | <span data-ttu-id="fd951-142">Int3</span><span class="sxs-lookup"><span data-stu-id="fd951-142">int3</span></span>           |
| <span data-ttu-id="fd951-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fd951-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fd951-144">sem suporte</span><span class="sxs-lookup"><span data-stu-id="fd951-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fd951-145">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd951-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd951-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fd951-146">Type: **float**</span></span>

<span data-ttu-id="fd951-147">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="fd951-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fd951-148">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="fd951-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd951-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd951-149">Return value</span></span>

<span data-ttu-id="fd951-150">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fd951-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fd951-151">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="fd951-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fd951-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd951-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd951-153">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="fd951-153">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="fd951-154">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="fd951-154">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
