---
title: 'Função SampleBias:: SampleBias (S, float, float, int, float, uint) para Texture1DArray'
description: 'Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para. | Função SampleBias:: SampleBias (S, float, float, int, float, uint) para Texture1DArray'
ms.assetid: 6136674B-38F4-4081-82D6-0731604EB1A3
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
ms.openlocfilehash: 4050503525345803a105d7717e96f6aa7b5c43cd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506547"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="7b2e8-105">Função SampleBias:: SampleBias (S, float, float, int, float, uint) para Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="7b2e8-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="7b2e8-106">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="7b2e8-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2e8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b2e8-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7b2e8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b2e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b2e8-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="7b2e8-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e8-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-111">Type: **SamplerState**</span></span>

<span data-ttu-id="7b2e8-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="7b2e8-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="7b2e8-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="7b2e8-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7b2e8-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e8-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-115">Type: **float**</span></span>

<span data-ttu-id="7b2e8-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-116">The texture coordinates.</span></span> <span data-ttu-id="7b2e8-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="7b2e8-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7b2e8-118">Texture-Object Type</span></span>                    | <span data-ttu-id="7b2e8-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b2e8-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="7b2e8-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7b2e8-120">Texture1D</span></span>                              | <span data-ttu-id="7b2e8-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="7b2e8-121">float</span></span>          |
| <span data-ttu-id="7b2e8-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="7b2e8-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="7b2e8-123">float2</span><span class="sxs-lookup"><span data-stu-id="7b2e8-123">float2</span></span>         |
| <span data-ttu-id="7b2e8-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="7b2e8-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="7b2e8-125">float3</span><span class="sxs-lookup"><span data-stu-id="7b2e8-125">float3</span></span>         |
| <span data-ttu-id="7b2e8-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7b2e8-126">TextureCubeArray</span></span>                       | <span data-ttu-id="7b2e8-127">float4</span><span class="sxs-lookup"><span data-stu-id="7b2e8-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="7b2e8-128">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2e8-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e8-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-129">Type: **float**</span></span>

<span data-ttu-id="7b2e8-130">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7b2e8-131">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2e8-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e8-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-132">Type: **int**</span></span>

<span data-ttu-id="7b2e8-133">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="7b2e8-134">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="7b2e8-135">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="7b2e8-136">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="7b2e8-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="7b2e8-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7b2e8-137">Texture-Object Type</span></span>           | <span data-ttu-id="7b2e8-138">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b2e8-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="7b2e8-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="7b2e8-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="7b2e8-140">INT</span><span class="sxs-lookup"><span data-stu-id="7b2e8-140">int</span></span>            |
| <span data-ttu-id="7b2e8-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7b2e8-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="7b2e8-142">int2</span><span class="sxs-lookup"><span data-stu-id="7b2e8-142">int2</span></span>           |
| <span data-ttu-id="7b2e8-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7b2e8-143">Texture3D</span></span>                     | <span data-ttu-id="7b2e8-144">Int3</span><span class="sxs-lookup"><span data-stu-id="7b2e8-144">int3</span></span>           |
| <span data-ttu-id="7b2e8-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7b2e8-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="7b2e8-146">sem suporte</span><span class="sxs-lookup"><span data-stu-id="7b2e8-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="7b2e8-147">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b2e8-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e8-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-148">Type: **float**</span></span>

<span data-ttu-id="7b2e8-149">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="7b2e8-150">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="7b2e8-151">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7b2e8-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e8-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-152">Type: **uint**</span></span>

<span data-ttu-id="7b2e8-153">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-153">The status of the operation.</span></span> <span data-ttu-id="7b2e8-154">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7b2e8-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7b2e8-155">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7b2e8-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7b2e8-156">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="7b2e8-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b2e8-157">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b2e8-157">Return value</span></span>

<span data-ttu-id="7b2e8-158">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="7b2e8-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="7b2e8-159">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="7b2e8-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="7b2e8-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b2e8-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2e8-161">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="7b2e8-161">SampleBias methods</span></span>](texture1darray-samplebias.md)
</dt> </dl>

 

 
