---
title: 'Função SampleBias:: SampleBias (S, float, float, int, float)'
description: 'Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para. | Função SampleBias:: SampleBias (S, float, float, int, float)'
ms.assetid: C252F1D1-51F9-48E3-BD74-3B050E0E16E0
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
ms.openlocfilehash: 16cc939de3bffe32dd26380b05eb65afac05114d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968309"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="26503-105">Função SampleBias:: SampleBias (S, float, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="26503-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="26503-106">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="26503-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="26503-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26503-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="26503-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26503-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26503-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="26503-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26503-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="26503-110">Type: **SamplerState**</span></span>

<span data-ttu-id="26503-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="26503-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="26503-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="26503-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="26503-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="26503-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26503-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="26503-114">Type: **float**</span></span>

<span data-ttu-id="26503-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="26503-115">The texture coordinates.</span></span> <span data-ttu-id="26503-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="26503-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="26503-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="26503-117">Texture-Object Type</span></span>                    | <span data-ttu-id="26503-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="26503-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="26503-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="26503-119">Texture1D</span></span>                              | <span data-ttu-id="26503-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="26503-120">float</span></span>          |
| <span data-ttu-id="26503-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="26503-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="26503-122">float2</span><span class="sxs-lookup"><span data-stu-id="26503-122">float2</span></span>         |
| <span data-ttu-id="26503-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="26503-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="26503-124">float3</span><span class="sxs-lookup"><span data-stu-id="26503-124">float3</span></span>         |
| <span data-ttu-id="26503-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="26503-125">TextureCubeArray</span></span>                       | <span data-ttu-id="26503-126">float4</span><span class="sxs-lookup"><span data-stu-id="26503-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="26503-127">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26503-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26503-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="26503-128">Type: **float**</span></span>

<span data-ttu-id="26503-129">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="26503-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="26503-130">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26503-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26503-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="26503-131">Type: **int**</span></span>

<span data-ttu-id="26503-132">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="26503-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="26503-133">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="26503-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="26503-134">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="26503-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="26503-135">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="26503-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="26503-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="26503-136">Texture-Object Type</span></span>           | <span data-ttu-id="26503-137">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="26503-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="26503-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="26503-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="26503-139">INT</span><span class="sxs-lookup"><span data-stu-id="26503-139">int</span></span>            |
| <span data-ttu-id="26503-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="26503-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="26503-141">int2</span><span class="sxs-lookup"><span data-stu-id="26503-141">int2</span></span>           |
| <span data-ttu-id="26503-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="26503-142">Texture3D</span></span>                     | <span data-ttu-id="26503-143">Int3</span><span class="sxs-lookup"><span data-stu-id="26503-143">int3</span></span>           |
| <span data-ttu-id="26503-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="26503-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="26503-145">sem suporte</span><span class="sxs-lookup"><span data-stu-id="26503-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="26503-146">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26503-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26503-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="26503-147">Type: **float**</span></span>

<span data-ttu-id="26503-148">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="26503-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="26503-149">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="26503-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26503-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26503-150">Return value</span></span>

<span data-ttu-id="26503-151">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="26503-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="26503-152">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="26503-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="26503-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="26503-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26503-154">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="26503-154">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="26503-155">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="26503-155">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
