---
title: 'Função SampleCmp:: SampleCmp (S, float, float, int, float, uint) para Texture1D'
description: A função amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para Texture1D.
ms.assetid: D2320225-4BC6-4229-A624-6D0F105DD788
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
ms.openlocfilehash: 690ede3cac45d05a3000fe60654255daef5202f7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968741"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="91b1a-105">Função SampleCmp:: SampleCmp (S, float, float, int, float, uint) para Texture1D</span><span class="sxs-lookup"><span data-stu-id="91b1a-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="91b1a-106">Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="91b1a-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="91b1a-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="91b1a-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b1a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91b1a-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="91b1a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91b1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b1a-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="91b1a-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b1a-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="91b1a-111">Type: **SamplerState**</span></span>

<span data-ttu-id="91b1a-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="91b1a-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="91b1a-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="91b1a-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="91b1a-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="91b1a-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b1a-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="91b1a-115">Type: **float**</span></span>

<span data-ttu-id="91b1a-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="91b1a-116">The texture coordinates.</span></span> <span data-ttu-id="91b1a-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="91b1a-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="91b1a-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="91b1a-118">Texture-Object Type</span></span>                    | <span data-ttu-id="91b1a-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="91b1a-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="91b1a-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="91b1a-120">Texture1D</span></span>                              | <span data-ttu-id="91b1a-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="91b1a-121">float</span></span>          |
| <span data-ttu-id="91b1a-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="91b1a-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="91b1a-123">float2</span><span class="sxs-lookup"><span data-stu-id="91b1a-123">float2</span></span>         |
| <span data-ttu-id="91b1a-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="91b1a-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="91b1a-125">float3</span><span class="sxs-lookup"><span data-stu-id="91b1a-125">float3</span></span>         |
| <span data-ttu-id="91b1a-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="91b1a-126">TextureCubeArray</span></span>                       | <span data-ttu-id="91b1a-127">float4</span><span class="sxs-lookup"><span data-stu-id="91b1a-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="91b1a-128">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91b1a-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b1a-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="91b1a-129">Type: **float**</span></span>

<span data-ttu-id="91b1a-130">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="91b1a-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="91b1a-131">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91b1a-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b1a-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="91b1a-132">Type: **int**</span></span>

<span data-ttu-id="91b1a-133">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="91b1a-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="91b1a-134">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="91b1a-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="91b1a-135">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="91b1a-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="91b1a-136">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="91b1a-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="91b1a-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="91b1a-137">Texture-Object Type</span></span>           | <span data-ttu-id="91b1a-138">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="91b1a-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="91b1a-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="91b1a-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="91b1a-140">INT</span><span class="sxs-lookup"><span data-stu-id="91b1a-140">int</span></span>            |
| <span data-ttu-id="91b1a-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="91b1a-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="91b1a-142">int2</span><span class="sxs-lookup"><span data-stu-id="91b1a-142">int2</span></span>           |
| <span data-ttu-id="91b1a-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="91b1a-143">Texture3D</span></span>                     | <span data-ttu-id="91b1a-144">Int3</span><span class="sxs-lookup"><span data-stu-id="91b1a-144">int3</span></span>           |
| <span data-ttu-id="91b1a-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="91b1a-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="91b1a-146">sem suporte</span><span class="sxs-lookup"><span data-stu-id="91b1a-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="91b1a-147">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91b1a-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91b1a-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="91b1a-148">Type: **float**</span></span>

<span data-ttu-id="91b1a-149">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="91b1a-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="91b1a-150">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="91b1a-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="91b1a-151">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="91b1a-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91b1a-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="91b1a-152">Type: **uint**</span></span>

<span data-ttu-id="91b1a-153">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="91b1a-153">The status of the operation.</span></span> <span data-ttu-id="91b1a-154">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="91b1a-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="91b1a-155">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="91b1a-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="91b1a-156">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="91b1a-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b1a-157">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91b1a-157">Return value</span></span>

<span data-ttu-id="91b1a-158">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="91b1a-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="91b1a-159">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="91b1a-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="91b1a-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="91b1a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b1a-161">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="91b1a-161">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
