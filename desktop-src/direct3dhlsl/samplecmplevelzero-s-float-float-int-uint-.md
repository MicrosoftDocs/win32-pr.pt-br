---
title: 'Função SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, int, uint) para Texture2D'
description: Faz amostras de um Texture2D no nível de mipmap 0 somente e compara o resultado a um valor de comparação e, em seguida, retorna o status sobre a operação. Para Texture2D.
ms.assetid: AEFE424F-2C77-434C-B9C0-8173778CB108
keywords:
- HLSL da função SampleCmpLevelZero
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a28dddeb687093a76f4f8bc60c96777468abc9f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989451"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="e28a7-105">Função SampleCmpLevelZero:: SampleCmpLevelZero (S, float, float, int, uint) para Texture2D</span><span class="sxs-lookup"><span data-stu-id="e28a7-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="e28a7-106">Amostras de um [**Texture2D**](sm5-object-texture2d.md) no nível de mipmap 0 somente e compara o resultado a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="e28a7-106">Samples a [**Texture2D**](sm5-object-texture2d.md) on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="e28a7-107">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="e28a7-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e28a7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e28a7-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e28a7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e28a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e28a7-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e28a7-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28a7-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="e28a7-111">Type: **SamplerState**</span></span>

<span data-ttu-id="e28a7-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e28a7-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e28a7-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="e28a7-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e28a7-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e28a7-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28a7-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e28a7-115">Type: **float**</span></span>

<span data-ttu-id="e28a7-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e28a7-116">The texture coordinates.</span></span> <span data-ttu-id="e28a7-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e28a7-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e28a7-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e28a7-118">Texture-Object Type</span></span>                    | <span data-ttu-id="e28a7-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e28a7-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e28a7-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e28a7-120">Texture1D</span></span>                              | <span data-ttu-id="e28a7-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e28a7-121">float</span></span>          |
| <span data-ttu-id="e28a7-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e28a7-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e28a7-123">float2</span><span class="sxs-lookup"><span data-stu-id="e28a7-123">float2</span></span>         |
| <span data-ttu-id="e28a7-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e28a7-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e28a7-125">float3</span><span class="sxs-lookup"><span data-stu-id="e28a7-125">float3</span></span>         |
| <span data-ttu-id="e28a7-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e28a7-126">TextureCubeArray</span></span>                       | <span data-ttu-id="e28a7-127">float4</span><span class="sxs-lookup"><span data-stu-id="e28a7-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e28a7-128">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e28a7-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28a7-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e28a7-129">Type: **float**</span></span>

<span data-ttu-id="e28a7-130">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="e28a7-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="e28a7-131">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e28a7-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28a7-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="e28a7-132">Type: **int**</span></span>

<span data-ttu-id="e28a7-133">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e28a7-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e28a7-134">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="e28a7-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e28a7-135">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="e28a7-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e28a7-136">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e28a7-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e28a7-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e28a7-137">Texture-Object Type</span></span>           | <span data-ttu-id="e28a7-138">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e28a7-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e28a7-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e28a7-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e28a7-140">INT</span><span class="sxs-lookup"><span data-stu-id="e28a7-140">int</span></span>            |
| <span data-ttu-id="e28a7-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e28a7-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e28a7-142">int2</span><span class="sxs-lookup"><span data-stu-id="e28a7-142">int2</span></span>           |
| <span data-ttu-id="e28a7-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e28a7-143">Texture3D</span></span>                     | <span data-ttu-id="e28a7-144">Int3</span><span class="sxs-lookup"><span data-stu-id="e28a7-144">int3</span></span>           |
| <span data-ttu-id="e28a7-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e28a7-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e28a7-146">sem suporte</span><span class="sxs-lookup"><span data-stu-id="e28a7-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e28a7-147">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e28a7-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e28a7-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e28a7-148">Type: **uint**</span></span>

<span data-ttu-id="e28a7-149">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="e28a7-149">The status of the operation.</span></span> <span data-ttu-id="e28a7-150">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e28a7-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e28a7-151">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e28a7-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e28a7-152">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="e28a7-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e28a7-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e28a7-153">Return value</span></span>

<span data-ttu-id="e28a7-154">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e28a7-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e28a7-155">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e28a7-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e28a7-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="e28a7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28a7-157">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="e28a7-157">SampleCmpLevelZero methods</span></span>](texture2d-samplecmplevelzero.md)
</dt> </dl>

 

 
