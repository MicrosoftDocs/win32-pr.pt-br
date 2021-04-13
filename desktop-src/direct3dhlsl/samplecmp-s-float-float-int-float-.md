---
title: 'Função SampleCmp:: SampleCmp (S, float, float, int, float)) para Texture2D'
description: Essa função amostra um Texture2D usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) de amostra para.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968749"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="0a8ed-104">SampleCmp:: SampleCmp (S, float, float, int, float) function para Texture2D</span><span class="sxs-lookup"><span data-stu-id="0a8ed-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="0a8ed-105">Amostras de um [**Texture2D**](sm5-object-texture2d.md), usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) de amostra para.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a8ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a8ed-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="0a8ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a8ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a8ed-108">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0a8ed-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a8ed-109">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="0a8ed-109">Type: **SamplerState**</span></span>

<span data-ttu-id="0a8ed-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="0a8ed-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="0a8ed-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="0a8ed-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0a8ed-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a8ed-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0a8ed-113">Type: **float**</span></span>

<span data-ttu-id="0a8ed-114">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-114">The texture coordinates.</span></span> <span data-ttu-id="0a8ed-115">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0a8ed-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0a8ed-116">Texture-Object Type</span></span>                    | <span data-ttu-id="0a8ed-117">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a8ed-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="0a8ed-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0a8ed-118">Texture1D</span></span>                              | <span data-ttu-id="0a8ed-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0a8ed-119">float</span></span>          |
| <span data-ttu-id="0a8ed-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="0a8ed-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="0a8ed-121">float2</span><span class="sxs-lookup"><span data-stu-id="0a8ed-121">float2</span></span>         |
| <span data-ttu-id="0a8ed-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0a8ed-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="0a8ed-123">float3</span><span class="sxs-lookup"><span data-stu-id="0a8ed-123">float3</span></span>         |
| <span data-ttu-id="0a8ed-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0a8ed-124">TextureCubeArray</span></span>                       | <span data-ttu-id="0a8ed-125">float4</span><span class="sxs-lookup"><span data-stu-id="0a8ed-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="0a8ed-126">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a8ed-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a8ed-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0a8ed-127">Type: **float**</span></span>

<span data-ttu-id="0a8ed-128">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="0a8ed-129">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a8ed-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a8ed-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0a8ed-130">Type: **int**</span></span>

<span data-ttu-id="0a8ed-131">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="0a8ed-132">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="0a8ed-133">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="0a8ed-134">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="0a8ed-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="0a8ed-135">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0a8ed-135">Texture-Object Type</span></span>           | <span data-ttu-id="0a8ed-136">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a8ed-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="0a8ed-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0a8ed-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="0a8ed-138">INT</span><span class="sxs-lookup"><span data-stu-id="0a8ed-138">int</span></span>            |
| <span data-ttu-id="0a8ed-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0a8ed-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="0a8ed-140">int2</span><span class="sxs-lookup"><span data-stu-id="0a8ed-140">int2</span></span>           |
| <span data-ttu-id="0a8ed-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0a8ed-141">Texture3D</span></span>                     | <span data-ttu-id="0a8ed-142">Int3</span><span class="sxs-lookup"><span data-stu-id="0a8ed-142">int3</span></span>           |
| <span data-ttu-id="0a8ed-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0a8ed-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0a8ed-144">sem suporte</span><span class="sxs-lookup"><span data-stu-id="0a8ed-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0a8ed-145">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a8ed-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a8ed-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="0a8ed-146">Type: **float**</span></span>

<span data-ttu-id="0a8ed-147">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="0a8ed-148">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a8ed-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a8ed-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a8ed-149">Return value</span></span>

<span data-ttu-id="0a8ed-150">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="0a8ed-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="0a8ed-151">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="0a8ed-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="0a8ed-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a8ed-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8ed-153">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="0a8ed-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
