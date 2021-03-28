---
title: 'Função SampleBias:: SampleBias (S, float, float, float, uint)'
description: 'Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para. Retorna o status sobre a operação. | Função SampleBias:: SampleBias (S, float, float, float, uint)'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 2f3a994d7b0f0c2d55ae3203db9f3205932c1a25
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172781"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="88fac-106">Função SampleBias:: SampleBias (S, float, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="88fac-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="88fac-107">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="88fac-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="88fac-108">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="88fac-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="88fac-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88fac-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="88fac-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88fac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88fac-111">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="88fac-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88fac-112">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="88fac-112">Type: **SamplerState**</span></span>

<span data-ttu-id="88fac-113">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="88fac-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="88fac-114">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="88fac-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="88fac-115">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="88fac-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88fac-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="88fac-116">Type: **float**</span></span>

<span data-ttu-id="88fac-117">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="88fac-117">The texture coordinates.</span></span> <span data-ttu-id="88fac-118">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="88fac-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="88fac-119">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="88fac-119">Texture-Object Type</span></span>                    | <span data-ttu-id="88fac-120">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="88fac-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="88fac-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="88fac-121">Texture1D</span></span>                              | <span data-ttu-id="88fac-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="88fac-122">float</span></span>          |
| <span data-ttu-id="88fac-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="88fac-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="88fac-124">float2</span><span class="sxs-lookup"><span data-stu-id="88fac-124">float2</span></span>         |
| <span data-ttu-id="88fac-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="88fac-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="88fac-126">float3</span><span class="sxs-lookup"><span data-stu-id="88fac-126">float3</span></span>         |
| <span data-ttu-id="88fac-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="88fac-127">TextureCubeArray</span></span>                       | <span data-ttu-id="88fac-128">float4</span><span class="sxs-lookup"><span data-stu-id="88fac-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="88fac-129">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88fac-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88fac-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="88fac-130">Type: **float**</span></span>

<span data-ttu-id="88fac-131">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="88fac-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="88fac-132">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88fac-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88fac-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="88fac-133">Type: **float**</span></span>

<span data-ttu-id="88fac-134">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="88fac-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="88fac-135">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="88fac-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="88fac-136">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="88fac-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88fac-137">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="88fac-137">Type: **uint**</span></span>

<span data-ttu-id="88fac-138">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="88fac-138">The status of the operation.</span></span> <span data-ttu-id="88fac-139">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="88fac-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="88fac-140">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="88fac-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="88fac-141">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="88fac-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88fac-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88fac-142">Return value</span></span>

<span data-ttu-id="88fac-143">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="88fac-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="88fac-144">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="88fac-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="88fac-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="88fac-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fac-146">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="88fac-146">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="88fac-147">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="88fac-147">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
