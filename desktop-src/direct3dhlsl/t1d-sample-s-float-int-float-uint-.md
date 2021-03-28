---
title: 'Função Texture1D:: Sample (S, float, int, float, uint)'
description: 'Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação. | Função Texture1D:: Sample (S, float, int, float, uint)'
ms.assetid: AF987A41-385D-4A77-B3FD-FE5523A6CC5C
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
ms.openlocfilehash: 9fad13781cbf862e386293ff96f8e99b57603c76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989195"
---
# <a name="texture1dsamplesfloatintfloatuint-function"></a><span data-ttu-id="3b0c9-105">Função Texture1D:: Sample (S, float, int, float, uint)</span><span class="sxs-lookup"><span data-stu-id="3b0c9-105">Texture1D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="3b0c9-106">Exemplifica uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0c9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b0c9-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3b0c9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b0c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b0c9-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3b0c9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0c9-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="3b0c9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3b0c9-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3b0c9-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3b0c9-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3b0c9-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3b0c9-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0c9-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3b0c9-114">Type: **float**</span></span>

<span data-ttu-id="3b0c9-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-115">The texture coordinates.</span></span> <span data-ttu-id="3b0c9-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3b0c9-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3b0c9-117">Texture-Object Type</span></span>                    | <span data-ttu-id="3b0c9-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b0c9-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3b0c9-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3b0c9-119">Texture1D</span></span>                              | <span data-ttu-id="3b0c9-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3b0c9-120">float</span></span>          |
| <span data-ttu-id="3b0c9-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3b0c9-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3b0c9-122">float2</span><span class="sxs-lookup"><span data-stu-id="3b0c9-122">float2</span></span>         |
| <span data-ttu-id="3b0c9-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3b0c9-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3b0c9-124">float3</span><span class="sxs-lookup"><span data-stu-id="3b0c9-124">float3</span></span>         |
| <span data-ttu-id="3b0c9-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3b0c9-125">TextureCubeArray</span></span>                       | <span data-ttu-id="3b0c9-126">float4</span><span class="sxs-lookup"><span data-stu-id="3b0c9-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3b0c9-127">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b0c9-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0c9-128">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3b0c9-128">Type: **int**</span></span>

<span data-ttu-id="3b0c9-129">Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3b0c9-130">Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3b0c9-131">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3b0c9-132">Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3b0c9-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3b0c9-133">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3b0c9-133">Texture-Object Type</span></span>           | <span data-ttu-id="3b0c9-134">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b0c9-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3b0c9-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3b0c9-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3b0c9-136">INT</span><span class="sxs-lookup"><span data-stu-id="3b0c9-136">int</span></span>            |
| <span data-ttu-id="3b0c9-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3b0c9-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3b0c9-138">int2</span><span class="sxs-lookup"><span data-stu-id="3b0c9-138">int2</span></span>           |
| <span data-ttu-id="3b0c9-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3b0c9-139">Texture3D</span></span>                     | <span data-ttu-id="3b0c9-140">Int3</span><span class="sxs-lookup"><span data-stu-id="3b0c9-140">int3</span></span>           |
| <span data-ttu-id="3b0c9-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3b0c9-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3b0c9-142">sem suporte</span><span class="sxs-lookup"><span data-stu-id="3b0c9-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3b0c9-143">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b0c9-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0c9-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3b0c9-144">Type: **float**</span></span>

<span data-ttu-id="3b0c9-145">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3b0c9-146">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="3b0c9-147">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3b0c9-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0c9-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3b0c9-148">Type: **uint**</span></span>

<span data-ttu-id="3b0c9-149">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-149">The status of the operation.</span></span> <span data-ttu-id="3b0c9-150">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3b0c9-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3b0c9-151">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3b0c9-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3b0c9-152">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="3b0c9-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b0c9-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b0c9-153">Return value</span></span>

<span data-ttu-id="3b0c9-154">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3b0c9-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3b0c9-155">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3b0c9-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3b0c9-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b0c9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0c9-157">Métodos de exemplo</span><span class="sxs-lookup"><span data-stu-id="3b0c9-157">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
