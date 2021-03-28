---
title: 'Função Texture1D:: Sample (S, float, int, float)'
description: 'Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função Texture1D:: Sample (S, float, int, float)'
ms.assetid: D2E2E143-8240-43AA-AD70-BD793B3CFD19
keywords:
- Exemplo de função HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f119955a66f7aec336ce52d730d54a5f11756527
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012034"
---
# <a name="texture1dsamplesfloatintfloat-function"></a><span data-ttu-id="df6b5-105">Função Texture1D:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="df6b5-105">Texture1D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="df6b5-106">Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="df6b5-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6b5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df6b5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="df6b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df6b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6b5-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="df6b5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6b5-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="df6b5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="df6b5-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="df6b5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="df6b5-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="df6b5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="df6b5-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="df6b5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6b5-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="df6b5-114">Type: **float**</span></span>

<span data-ttu-id="df6b5-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="df6b5-115">The texture coordinates.</span></span> <span data-ttu-id="df6b5-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="df6b5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="df6b5-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="df6b5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="df6b5-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="df6b5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="df6b5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="df6b5-119">Texture1D</span></span>                              | <span data-ttu-id="df6b5-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="df6b5-120">float</span></span>          |
| <span data-ttu-id="df6b5-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="df6b5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="df6b5-122">float2</span><span class="sxs-lookup"><span data-stu-id="df6b5-122">float2</span></span>         |
| <span data-ttu-id="df6b5-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="df6b5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="df6b5-124">float3</span><span class="sxs-lookup"><span data-stu-id="df6b5-124">float3</span></span>         |
| <span data-ttu-id="df6b5-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="df6b5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="df6b5-126">float4</span><span class="sxs-lookup"><span data-stu-id="df6b5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="df6b5-127">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6b5-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6b5-128">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="df6b5-128">Type: **int**</span></span>

<span data-ttu-id="df6b5-129">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="df6b5-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="df6b5-130">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="df6b5-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="df6b5-131">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="df6b5-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="df6b5-132">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="df6b5-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="df6b5-133">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="df6b5-133">Texture-Object Type</span></span>           | <span data-ttu-id="df6b5-134">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="df6b5-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="df6b5-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="df6b5-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="df6b5-136">INT</span><span class="sxs-lookup"><span data-stu-id="df6b5-136">int</span></span>            |
| <span data-ttu-id="df6b5-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="df6b5-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="df6b5-138">int2</span><span class="sxs-lookup"><span data-stu-id="df6b5-138">int2</span></span>           |
| <span data-ttu-id="df6b5-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="df6b5-139">Texture3D</span></span>                     | <span data-ttu-id="df6b5-140">Int3</span><span class="sxs-lookup"><span data-stu-id="df6b5-140">int3</span></span>           |
| <span data-ttu-id="df6b5-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="df6b5-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="df6b5-142">sem suporte</span><span class="sxs-lookup"><span data-stu-id="df6b5-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="df6b5-143">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df6b5-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6b5-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="df6b5-144">Type: **float**</span></span>

<span data-ttu-id="df6b5-145">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="df6b5-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="df6b5-146">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="df6b5-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6b5-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df6b5-147">Return value</span></span>

<span data-ttu-id="df6b5-148">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="df6b5-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="df6b5-149">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="df6b5-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="df6b5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="df6b5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6b5-151">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="df6b5-151">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
