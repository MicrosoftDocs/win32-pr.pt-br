---
title: 'Função SampleCmp:: SampleCmp (S, float, float, float) para TextureCube'
description: 'Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função SampleCmp:: SampleCmp (S, float, float, float) para TextureCube'
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
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
ms.openlocfilehash: e8a326101df26ab7f4925c9c6cce3673385309fd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104968735"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="2bab5-105">Função SampleCmp:: SampleCmp (S, float, float, float) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="2bab5-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="2bab5-106">Amostras de uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="2bab5-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bab5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bab5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="2bab5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bab5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bab5-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2bab5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bab5-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="2bab5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2bab5-111">Um [estado de amostra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2bab5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2bab5-112">Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="2bab5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2bab5-113">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2bab5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bab5-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2bab5-114">Type: **float**</span></span>

<span data-ttu-id="2bab5-115">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="2bab5-115">The texture coordinates.</span></span> <span data-ttu-id="2bab5-116">O tipo de argumento é dependente do tipo de objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="2bab5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2bab5-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2bab5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="2bab5-118">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bab5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2bab5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2bab5-119">Texture1D</span></span>                              | <span data-ttu-id="2bab5-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2bab5-120">float</span></span>          |
| <span data-ttu-id="2bab5-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2bab5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2bab5-122">float2</span><span class="sxs-lookup"><span data-stu-id="2bab5-122">float2</span></span>         |
| <span data-ttu-id="2bab5-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2bab5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2bab5-124">float3</span><span class="sxs-lookup"><span data-stu-id="2bab5-124">float3</span></span>         |
| <span data-ttu-id="2bab5-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2bab5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="2bab5-126">float4</span><span class="sxs-lookup"><span data-stu-id="2bab5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2bab5-127">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bab5-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bab5-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2bab5-128">Type: **float**</span></span>

<span data-ttu-id="2bab5-129">Um valor de ponto flutuante a ser usado como um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="2bab5-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="2bab5-130">*Fixe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bab5-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bab5-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2bab5-131">Type: **float**</span></span>

<span data-ttu-id="2bab5-132">Um valor opcional para fixe os valores de LOD de exemplo para.</span><span class="sxs-lookup"><span data-stu-id="2bab5-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2bab5-133">Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="2bab5-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bab5-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bab5-134">Return value</span></span>

<span data-ttu-id="2bab5-135">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2bab5-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2bab5-136">O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2bab5-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2bab5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bab5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bab5-138">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="2bab5-138">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="2bab5-139">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="2bab5-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
