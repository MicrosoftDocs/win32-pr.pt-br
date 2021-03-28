---
title: 'Função SampleCmp:: SampleCmp (S, float, float, int, float, uint) para Texture2DArray'
description: Essa função amostra uma textura usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para Texture2DArray.
ms.assetid: 847A6B79-3A66-4209-AB01-7C1FDA8A433A
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
ms.openlocfilehash: cc8957ca2f6c1eb3e4a665b5d6df134c854ccc3c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104173223"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="9a9fd-105">Função SampleCmp:: SampleCmp (S, float, float, int, float, uint) para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9a9fd-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="9a9fd-106">Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="9a9fd-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9fd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a9fd-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9a9fd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a9fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9fd-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="9a9fd-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9fd-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-111">Type: **SamplerState**</span></span>

<span data-ttu-id="9a9fd-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="9a9fd-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="9a9fd-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="9a9fd-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9a9fd-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9fd-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-115">Type: **float**</span></span>

<span data-ttu-id="9a9fd-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-116">The texture coordinates.</span></span> <span data-ttu-id="9a9fd-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="9a9fd-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9a9fd-118">Texture-Object Type</span></span>                    | <span data-ttu-id="9a9fd-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a9fd-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="9a9fd-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9a9fd-120">Texture1D</span></span>                              | <span data-ttu-id="9a9fd-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9a9fd-121">float</span></span>          |
| <span data-ttu-id="9a9fd-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="9a9fd-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="9a9fd-123">float2</span><span class="sxs-lookup"><span data-stu-id="9a9fd-123">float2</span></span>         |
| <span data-ttu-id="9a9fd-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="9a9fd-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="9a9fd-125">float3</span><span class="sxs-lookup"><span data-stu-id="9a9fd-125">float3</span></span>         |
| <span data-ttu-id="9a9fd-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9a9fd-126">TextureCubeArray</span></span>                       | <span data-ttu-id="9a9fd-127">float4</span><span class="sxs-lookup"><span data-stu-id="9a9fd-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="9a9fd-128">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a9fd-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9fd-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-129">Type: **float**</span></span>

<span data-ttu-id="9a9fd-130">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="9a9fd-131">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a9fd-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9fd-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-132">Type: **int**</span></span>

<span data-ttu-id="9a9fd-133">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="9a9fd-134">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="9a9fd-135">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="9a9fd-136">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9a9fd-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="9a9fd-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9a9fd-137">Texture-Object Type</span></span>           | <span data-ttu-id="9a9fd-138">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a9fd-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="9a9fd-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9a9fd-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="9a9fd-140">INT</span><span class="sxs-lookup"><span data-stu-id="9a9fd-140">int</span></span>            |
| <span data-ttu-id="9a9fd-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9a9fd-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="9a9fd-142">int2</span><span class="sxs-lookup"><span data-stu-id="9a9fd-142">int2</span></span>           |
| <span data-ttu-id="9a9fd-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9a9fd-143">Texture3D</span></span>                     | <span data-ttu-id="9a9fd-144">Int3</span><span class="sxs-lookup"><span data-stu-id="9a9fd-144">int3</span></span>           |
| <span data-ttu-id="9a9fd-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9a9fd-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="9a9fd-146">sem suporte</span><span class="sxs-lookup"><span data-stu-id="9a9fd-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="9a9fd-147">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a9fd-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9fd-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-148">Type: **float**</span></span>

<span data-ttu-id="9a9fd-149">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="9a9fd-150">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="9a9fd-151">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9a9fd-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9fd-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-152">Type: **uint**</span></span>

<span data-ttu-id="9a9fd-153">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-153">The status of the operation.</span></span> <span data-ttu-id="9a9fd-154">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9a9fd-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9a9fd-155">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9a9fd-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9a9fd-156">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="9a9fd-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9fd-157">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a9fd-157">Return value</span></span>

<span data-ttu-id="9a9fd-158">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="9a9fd-159">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="9a9fd-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a9fd-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a9fd-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9fd-161">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="9a9fd-161">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="9a9fd-162">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="9a9fd-162">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
