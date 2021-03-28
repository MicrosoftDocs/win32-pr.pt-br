---
title: 'Função SampleBias:: SampleBias (S, float, float, float)'
description: 'Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para. | Função SampleBias:: SampleBias (S, float, float, float)'
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: 8d95a1b0341e61853a20d313a04d1cde64dde66d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091911"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="2045c-105">Função SampleBias:: SampleBias (S, float, float, float)</span><span class="sxs-lookup"><span data-stu-id="2045c-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="2045c-106">Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.</span><span class="sxs-lookup"><span data-stu-id="2045c-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2045c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2045c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="2045c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2045c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2045c-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2045c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2045c-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="2045c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2045c-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2045c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2045c-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="2045c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2045c-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2045c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2045c-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2045c-114">Type: **float**</span></span>

<span data-ttu-id="2045c-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="2045c-115">The texture coordinates.</span></span> <span data-ttu-id="2045c-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="2045c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2045c-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2045c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="2045c-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="2045c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2045c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2045c-119">Texture1D</span></span>                              | <span data-ttu-id="2045c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2045c-120">float</span></span>          |
| <span data-ttu-id="2045c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2045c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2045c-122">float2</span><span class="sxs-lookup"><span data-stu-id="2045c-122">float2</span></span>         |
| <span data-ttu-id="2045c-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2045c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2045c-124">float3</span><span class="sxs-lookup"><span data-stu-id="2045c-124">float3</span></span>         |
| <span data-ttu-id="2045c-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2045c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="2045c-126">float4</span><span class="sxs-lookup"><span data-stu-id="2045c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2045c-127">*Tendência* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2045c-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2045c-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2045c-128">Type: **float**</span></span>

<span data-ttu-id="2045c-129">O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2045c-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2045c-130">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2045c-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2045c-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2045c-131">Type: **float**</span></span>

<span data-ttu-id="2045c-132">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="2045c-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2045c-133">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="2045c-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2045c-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2045c-134">Return value</span></span>

<span data-ttu-id="2045c-135">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2045c-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2045c-136">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2045c-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2045c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2045c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2045c-138">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="2045c-138">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="2045c-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="2045c-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
