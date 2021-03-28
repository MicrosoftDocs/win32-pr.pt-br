---
title: 'Função SampleLevel:: SampleLevel (S, float, float, int, uint) para Texture2D'
description: Amostra um Texture2D no nível de mipmap especificado e retorna o status sobre a operação.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
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
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989448"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="aa9c9-104">Função SampleLevel:: SampleLevel (S, float, float, int, uint) para Texture2D</span><span class="sxs-lookup"><span data-stu-id="aa9c9-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="aa9c9-105">Amostra um [**Texture2D**](sm5-object-texture2d.md) no nível de mipmap especificado e retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9c9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa9c9-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="aa9c9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa9c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9c9-108">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="aa9c9-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c9-109">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="aa9c9-109">Type: **SamplerState**</span></span>

<span data-ttu-id="aa9c9-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c9-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="aa9c9-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="aa9c9-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="aa9c9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c9-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="aa9c9-113">Type: **float**</span></span>

<span data-ttu-id="aa9c9-114">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-114">The texture coordinates.</span></span> <span data-ttu-id="aa9c9-115">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="aa9c9-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="aa9c9-116">Texture-Object Type</span></span>                    | <span data-ttu-id="aa9c9-117">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa9c9-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="aa9c9-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="aa9c9-118">Texture1D</span></span>                              | <span data-ttu-id="aa9c9-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="aa9c9-119">float</span></span>          |
| <span data-ttu-id="aa9c9-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="aa9c9-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="aa9c9-121">float2</span><span class="sxs-lookup"><span data-stu-id="aa9c9-121">float2</span></span>         |
| <span data-ttu-id="aa9c9-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="aa9c9-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="aa9c9-123">float3</span><span class="sxs-lookup"><span data-stu-id="aa9c9-123">float3</span></span>         |
| <span data-ttu-id="aa9c9-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="aa9c9-124">TextureCubeArray</span></span>                       | <span data-ttu-id="aa9c9-125">float4</span><span class="sxs-lookup"><span data-stu-id="aa9c9-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="aa9c9-126">*LOD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9c9-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c9-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="aa9c9-127">Type: **float**</span></span>

<span data-ttu-id="aa9c9-128">\[em \] um número que especifica o nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="aa9c9-129">Se o valor for ≤ 0, o nível de mipmap 0 (maior mapa) será usado.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="aa9c9-130">O valor fracionário (se fornecido) é usado para interpolar entre dois níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="aa9c9-131">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9c9-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c9-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="aa9c9-132">Type: **int**</span></span>

<span data-ttu-id="aa9c9-133">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="aa9c9-134">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="aa9c9-135">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="aa9c9-136">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c9-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="aa9c9-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="aa9c9-137">Texture-Object Type</span></span>           | <span data-ttu-id="aa9c9-138">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa9c9-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="aa9c9-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="aa9c9-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="aa9c9-140">INT</span><span class="sxs-lookup"><span data-stu-id="aa9c9-140">int</span></span>            |
| <span data-ttu-id="aa9c9-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="aa9c9-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="aa9c9-142">int2</span><span class="sxs-lookup"><span data-stu-id="aa9c9-142">int2</span></span>           |
| <span data-ttu-id="aa9c9-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="aa9c9-143">Texture3D</span></span>                     | <span data-ttu-id="aa9c9-144">Int3</span><span class="sxs-lookup"><span data-stu-id="aa9c9-144">int3</span></span>           |
| <span data-ttu-id="aa9c9-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="aa9c9-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="aa9c9-146">sem suporte</span><span class="sxs-lookup"><span data-stu-id="aa9c9-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="aa9c9-147">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="aa9c9-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c9-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aa9c9-148">Type: **uint**</span></span>

<span data-ttu-id="aa9c9-149">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-149">The status of the operation.</span></span> <span data-ttu-id="aa9c9-150">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c9-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="aa9c9-151">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="aa9c9-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="aa9c9-152">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="aa9c9-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9c9-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa9c9-153">Return value</span></span>

<span data-ttu-id="aa9c9-154">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="aa9c9-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="aa9c9-155">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="aa9c9-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa9c9-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa9c9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9c9-157">Métodos SampleLevel</span><span class="sxs-lookup"><span data-stu-id="aa9c9-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
