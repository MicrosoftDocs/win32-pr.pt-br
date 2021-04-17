---
title: 'Função de função SampleBias:: SampleBias (S, float, float, int, float) para Texture1D'
description: 'A função SampleBias:: SampleBias (S, float, float, int, float) amostras de uma textura depois de aplicar o valor de tendência ao nível de mipmap.'
ms.assetid: 88BC4E99-B33D-4DAA-9A77-849B2F5FE6A7
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
ms.openlocfilehash: 1f7c6979d9781964d6bdd89914602c1946ce481c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187895"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="4abec-104">SampleBias:: SampleBias (S, float, float, int, float) function para Texture1D</span><span class="sxs-lookup"><span data-stu-id="4abec-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="4abec-105">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="4abec-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="4abec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4abec-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="4abec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4abec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abec-108">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="4abec-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abec-109">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="4abec-109">Type: **SamplerState**</span></span>

<span data-ttu-id="4abec-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4abec-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4abec-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="4abec-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4abec-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4abec-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abec-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4abec-113">Type: **float**</span></span>

<span data-ttu-id="4abec-114">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="4abec-114">The texture coordinates.</span></span> <span data-ttu-id="4abec-115">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="4abec-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4abec-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4abec-116">Texture-Object Type</span></span>                    | <span data-ttu-id="4abec-117">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4abec-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4abec-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4abec-118">Texture1D</span></span>                              | <span data-ttu-id="4abec-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4abec-119">float</span></span>          |
| <span data-ttu-id="4abec-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4abec-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4abec-121">float2</span><span class="sxs-lookup"><span data-stu-id="4abec-121">float2</span></span>         |
| <span data-ttu-id="4abec-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4abec-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4abec-123">float3</span><span class="sxs-lookup"><span data-stu-id="4abec-123">float3</span></span>         |
| <span data-ttu-id="4abec-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4abec-124">TextureCubeArray</span></span>                       | <span data-ttu-id="4abec-125">float4</span><span class="sxs-lookup"><span data-stu-id="4abec-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4abec-126">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4abec-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abec-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4abec-127">Type: **float**</span></span>

<span data-ttu-id="4abec-128">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="4abec-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4abec-129">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4abec-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abec-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4abec-130">Type: **int**</span></span>

<span data-ttu-id="4abec-131">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="4abec-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4abec-132">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="4abec-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4abec-133">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="4abec-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4abec-134">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4abec-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4abec-135">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4abec-135">Texture-Object Type</span></span>           | <span data-ttu-id="4abec-136">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4abec-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4abec-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4abec-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4abec-138">INT</span><span class="sxs-lookup"><span data-stu-id="4abec-138">int</span></span>            |
| <span data-ttu-id="4abec-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4abec-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4abec-140">int2</span><span class="sxs-lookup"><span data-stu-id="4abec-140">int2</span></span>           |
| <span data-ttu-id="4abec-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4abec-141">Texture3D</span></span>                     | <span data-ttu-id="4abec-142">Int3</span><span class="sxs-lookup"><span data-stu-id="4abec-142">int3</span></span>           |
| <span data-ttu-id="4abec-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4abec-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4abec-144">sem suporte</span><span class="sxs-lookup"><span data-stu-id="4abec-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4abec-145">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4abec-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abec-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4abec-146">Type: **float**</span></span>

<span data-ttu-id="4abec-147">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="4abec-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4abec-148">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="4abec-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abec-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4abec-149">Return value</span></span>

<span data-ttu-id="4abec-150">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4abec-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4abec-151">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4abec-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4abec-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="4abec-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abec-153">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="4abec-153">SampleBias methods</span></span>](texture1d-samplebias.md)
</dt> </dl>

 

 
