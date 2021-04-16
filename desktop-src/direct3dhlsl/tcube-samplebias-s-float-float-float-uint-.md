---
title: 'Função SampleBias:: SampleBias (S, float, float, float, uint) para TextureCube'
description: 'A função SampleBias:: SampleBias (S, float, float, float, uint) para o TextureCube amostras de uma textura depois de aplicar o valor de tendência ao nível de mipmap.'
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
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187683"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="c3e2e-104">Função SampleBias:: SampleBias (S, float, float, float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="c3e2e-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="c3e2e-105">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c3e2e-106">Retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e2e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3e2e-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c3e2e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3e2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3e2e-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c3e2e-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e2e-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c3e2e-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c3e2e-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c3e2e-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c3e2e-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c3e2e-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e2e-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-114">Type: **float**</span></span>

<span data-ttu-id="c3e2e-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-115">The texture coordinates.</span></span> <span data-ttu-id="c3e2e-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c3e2e-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c3e2e-117">Texture-Object Type</span></span>                    | <span data-ttu-id="c3e2e-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3e2e-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c3e2e-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c3e2e-119">Texture1D</span></span>                              | <span data-ttu-id="c3e2e-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c3e2e-120">float</span></span>          |
| <span data-ttu-id="c3e2e-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c3e2e-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c3e2e-122">float2</span><span class="sxs-lookup"><span data-stu-id="c3e2e-122">float2</span></span>         |
| <span data-ttu-id="c3e2e-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c3e2e-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c3e2e-124">float3</span><span class="sxs-lookup"><span data-stu-id="c3e2e-124">float3</span></span>         |
| <span data-ttu-id="c3e2e-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c3e2e-125">TextureCubeArray</span></span>                       | <span data-ttu-id="c3e2e-126">float4</span><span class="sxs-lookup"><span data-stu-id="c3e2e-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c3e2e-127">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3e2e-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e2e-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-128">Type: **float**</span></span>

<span data-ttu-id="c3e2e-129">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c3e2e-130">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3e2e-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e2e-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-131">Type: **float**</span></span>

<span data-ttu-id="c3e2e-132">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c3e2e-133">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c3e2e-134">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c3e2e-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3e2e-135">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-135">Type: **uint**</span></span>

<span data-ttu-id="c3e2e-136">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-136">The status of the operation.</span></span> <span data-ttu-id="c3e2e-137">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c3e2e-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c3e2e-138">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c3e2e-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c3e2e-139">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c3e2e-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3e2e-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3e2e-140">Return value</span></span>

<span data-ttu-id="c3e2e-141">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c3e2e-142">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c3e2e-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c3e2e-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3e2e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e2e-144">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="c3e2e-144">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="c3e2e-145">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="c3e2e-145">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
