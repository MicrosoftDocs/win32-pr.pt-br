---
title: 'Função SampleBias:: SampleBias (S, float, float, float) para TextureCube'
description: 'A função SampleBias:: SampleBias (S, float, float, float) para TextureCube amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187687"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="cd0b3-104">Função SampleBias:: SampleBias (S, float, float, float) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="cd0b3-104">SampleBias::SampleBias(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="cd0b3-105">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0b3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd0b3-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="cd0b3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd0b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd0b3-108">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="cd0b3-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0b3-109">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="cd0b3-109">Type: **SamplerState**</span></span>

<span data-ttu-id="cd0b3-110">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="cd0b3-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="cd0b3-111">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="cd0b3-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cd0b3-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0b3-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cd0b3-113">Type: **float**</span></span>

<span data-ttu-id="cd0b3-114">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-114">The texture coordinates.</span></span> <span data-ttu-id="cd0b3-115">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="cd0b3-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="cd0b3-116">Texture-Object Type</span></span>                    | <span data-ttu-id="cd0b3-117">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd0b3-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="cd0b3-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="cd0b3-118">Texture1D</span></span>                              | <span data-ttu-id="cd0b3-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cd0b3-119">float</span></span>          |
| <span data-ttu-id="cd0b3-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="cd0b3-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="cd0b3-121">float2</span><span class="sxs-lookup"><span data-stu-id="cd0b3-121">float2</span></span>         |
| <span data-ttu-id="cd0b3-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="cd0b3-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="cd0b3-123">float3</span><span class="sxs-lookup"><span data-stu-id="cd0b3-123">float3</span></span>         |
| <span data-ttu-id="cd0b3-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="cd0b3-124">TextureCubeArray</span></span>                       | <span data-ttu-id="cd0b3-125">float4</span><span class="sxs-lookup"><span data-stu-id="cd0b3-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="cd0b3-126">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd0b3-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0b3-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cd0b3-127">Type: **float**</span></span>

<span data-ttu-id="cd0b3-128">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="cd0b3-129">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cd0b3-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0b3-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cd0b3-130">Type: **float**</span></span>

<span data-ttu-id="cd0b3-131">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="cd0b3-132">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="cd0b3-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd0b3-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd0b3-133">Return value</span></span>

<span data-ttu-id="cd0b3-134">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="cd0b3-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="cd0b3-135">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="cd0b3-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="cd0b3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd0b3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0b3-137">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="cd0b3-137">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="cd0b3-138">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="cd0b3-138">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
