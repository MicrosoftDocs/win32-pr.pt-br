---
title: 'Função SampleBias:: SampleBias (S, float, float, int, float, uint) para Texture1D'
description: Essa função amostra uma textura depois de aplicar o valor de tendência ao nível de mipmap e tem um valor opcional para fixe os valores de LOD (nível de detalhe) de exemplo para.
ms.assetid: 47657CD8-57F5-4770-BD2F-491A5C57577A
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
ms.openlocfilehash: eb9443512c350ed701d7752bd529834e24d227c7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298888"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="981e5-104">Função SampleBias:: SampleBias (S, float, float, int, float, uint) para Texture1D</span><span class="sxs-lookup"><span data-stu-id="981e5-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="981e5-105">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="981e5-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="981e5-106">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="981e5-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="981e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="981e5-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="981e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="981e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="981e5-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="981e5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="981e5-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="981e5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="981e5-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="981e5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="981e5-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="981e5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="981e5-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="981e5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="981e5-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="981e5-114">Type: **float**</span></span>

<span data-ttu-id="981e5-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="981e5-115">The texture coordinates.</span></span> <span data-ttu-id="981e5-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="981e5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="981e5-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="981e5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="981e5-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="981e5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="981e5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="981e5-119">Texture1D</span></span>                              | <span data-ttu-id="981e5-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="981e5-120">float</span></span>          |
| <span data-ttu-id="981e5-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="981e5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="981e5-122">float2</span><span class="sxs-lookup"><span data-stu-id="981e5-122">float2</span></span>         |
| <span data-ttu-id="981e5-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="981e5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="981e5-124">float3</span><span class="sxs-lookup"><span data-stu-id="981e5-124">float3</span></span>         |
| <span data-ttu-id="981e5-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="981e5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="981e5-126">float4</span><span class="sxs-lookup"><span data-stu-id="981e5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="981e5-127">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="981e5-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="981e5-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="981e5-128">Type: **float**</span></span>

<span data-ttu-id="981e5-129">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="981e5-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="981e5-130">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="981e5-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="981e5-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="981e5-131">Type: **int**</span></span>

<span data-ttu-id="981e5-132">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="981e5-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="981e5-133">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="981e5-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="981e5-134">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="981e5-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="981e5-135">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="981e5-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="981e5-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="981e5-136">Texture-Object Type</span></span>           | <span data-ttu-id="981e5-137">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="981e5-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="981e5-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="981e5-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="981e5-139">INT</span><span class="sxs-lookup"><span data-stu-id="981e5-139">int</span></span>            |
| <span data-ttu-id="981e5-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="981e5-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="981e5-141">int2</span><span class="sxs-lookup"><span data-stu-id="981e5-141">int2</span></span>           |
| <span data-ttu-id="981e5-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="981e5-142">Texture3D</span></span>                     | <span data-ttu-id="981e5-143">Int3</span><span class="sxs-lookup"><span data-stu-id="981e5-143">int3</span></span>           |
| <span data-ttu-id="981e5-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="981e5-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="981e5-145">sem suporte</span><span class="sxs-lookup"><span data-stu-id="981e5-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="981e5-146">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="981e5-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="981e5-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="981e5-147">Type: **float**</span></span>

<span data-ttu-id="981e5-148">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="981e5-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="981e5-149">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="981e5-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="981e5-150">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="981e5-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="981e5-151">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="981e5-151">Type: **uint**</span></span>

<span data-ttu-id="981e5-152">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="981e5-152">The status of the operation.</span></span> <span data-ttu-id="981e5-153">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="981e5-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="981e5-154">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="981e5-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="981e5-155">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="981e5-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="981e5-156">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="981e5-156">Return value</span></span>

<span data-ttu-id="981e5-157">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="981e5-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="981e5-158">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="981e5-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="981e5-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="981e5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981e5-160">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="981e5-160">SampleBias methods</span></span>](texture1d-samplebias.md)
</dt> </dl>

 

 
