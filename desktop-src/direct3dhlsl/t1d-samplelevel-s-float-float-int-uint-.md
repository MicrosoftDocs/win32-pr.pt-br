---
title: 'Função SampleLevel:: SampleLevel (S, float, float, int, uint) para Texture1D'
description: 'Obtém uma textura no nível de mipmap especificado e retorna o status sobre a operação. Para Texture1D. | Função SampleLevel:: SampleLevel (S, float, float, int, uint)'
ms.assetid: B797C7F9-7436-4DD5-9CAB-EFF81D410174
keywords:
- HLSL da função SampleLevel
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d0c74bd59c8e693b009e9d53a766f339a20a2d6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989456"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="9c278-106">Função SampleLevel:: SampleLevel (S, float, float, int, uint) para Texture1D</span><span class="sxs-lookup"><span data-stu-id="9c278-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="9c278-107">Obtém uma textura no nível de mipmap especificado e retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="9c278-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c278-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c278-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9c278-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c278-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c278-110">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="9c278-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c278-111">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="9c278-111">Type: **SamplerState**</span></span>

<span data-ttu-id="9c278-112">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="9c278-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="9c278-113">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="9c278-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="9c278-114">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9c278-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c278-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9c278-115">Type: **float**</span></span>

<span data-ttu-id="9c278-116">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="9c278-116">The texture coordinates.</span></span> <span data-ttu-id="9c278-117">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="9c278-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="9c278-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9c278-118">Texture-Object Type</span></span>                    | <span data-ttu-id="9c278-119">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c278-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="9c278-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9c278-120">Texture1D</span></span>                              | <span data-ttu-id="9c278-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9c278-121">float</span></span>          |
| <span data-ttu-id="9c278-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="9c278-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="9c278-123">float2</span><span class="sxs-lookup"><span data-stu-id="9c278-123">float2</span></span>         |
| <span data-ttu-id="9c278-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="9c278-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="9c278-125">float3</span><span class="sxs-lookup"><span data-stu-id="9c278-125">float3</span></span>         |
| <span data-ttu-id="9c278-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9c278-126">TextureCubeArray</span></span>                       | <span data-ttu-id="9c278-127">float4</span><span class="sxs-lookup"><span data-stu-id="9c278-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="9c278-128">*LOD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c278-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c278-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9c278-129">Type: **float**</span></span>

<span data-ttu-id="9c278-130">\[em \] um número que especifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="9c278-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="9c278-131">Se o valor for ≤ 0, o nível de mipmap 0 (maior mapa) será usado.</span><span class="sxs-lookup"><span data-stu-id="9c278-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="9c278-132">O valor fracionário (se fornecido) é usado para interpolar entre dois níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="9c278-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="9c278-133">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c278-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c278-134">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="9c278-134">Type: **int**</span></span>

<span data-ttu-id="9c278-135">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="9c278-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="9c278-136">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="9c278-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="9c278-137">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="9c278-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="9c278-138">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9c278-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="9c278-139">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9c278-139">Texture-Object Type</span></span>           | <span data-ttu-id="9c278-140">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c278-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="9c278-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9c278-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="9c278-142">INT</span><span class="sxs-lookup"><span data-stu-id="9c278-142">int</span></span>            |
| <span data-ttu-id="9c278-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9c278-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="9c278-144">int2</span><span class="sxs-lookup"><span data-stu-id="9c278-144">int2</span></span>           |
| <span data-ttu-id="9c278-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9c278-145">Texture3D</span></span>                     | <span data-ttu-id="9c278-146">Int3</span><span class="sxs-lookup"><span data-stu-id="9c278-146">int3</span></span>           |
| <span data-ttu-id="9c278-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9c278-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="9c278-148">sem suporte</span><span class="sxs-lookup"><span data-stu-id="9c278-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="9c278-149">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9c278-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c278-150">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9c278-150">Type: **uint**</span></span>

<span data-ttu-id="9c278-151">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="9c278-151">The status of the operation.</span></span> <span data-ttu-id="9c278-152">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9c278-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9c278-153">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9c278-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9c278-154">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="9c278-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c278-155">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c278-155">Return value</span></span>

<span data-ttu-id="9c278-156">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9c278-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="9c278-157">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="9c278-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="9c278-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c278-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c278-159">Métodos SampleLevel</span><span class="sxs-lookup"><span data-stu-id="9c278-159">SampleLevel methods</span></span>](texture1d-samplelevel.md)
</dt> </dl>

 

 
