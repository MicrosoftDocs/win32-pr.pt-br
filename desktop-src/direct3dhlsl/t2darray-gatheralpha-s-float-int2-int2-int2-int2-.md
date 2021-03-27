---
title: 'Função Texture2DArray:: GatherAlpha (S, float, Int2, Int2, Int2, Int2)'
description: 'Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: GatherAlpha (S, float, Int2, Int2, Int2, Int2)'
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
keywords:
- HLSL da função GatherAlpha
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930324"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="c79a9-105">Função Texture2DArray:: GatherAlpha (S, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="c79a9-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="c79a9-106">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="c79a9-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79a9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c79a9-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="c79a9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c79a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79a9-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c79a9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79a9-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="c79a9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c79a9-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="c79a9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c79a9-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c79a9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79a9-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c79a9-113">Type: **float**</span></span>

<span data-ttu-id="c79a9-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="c79a9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c79a9-115">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c79a9-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79a9-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c79a9-116">Type: **int2**</span></span>

<span data-ttu-id="c79a9-117">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c79a9-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c79a9-118">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c79a9-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79a9-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c79a9-119">Type: **int2**</span></span>

<span data-ttu-id="c79a9-120">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c79a9-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c79a9-121">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c79a9-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79a9-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c79a9-122">Type: **int2**</span></span>

<span data-ttu-id="c79a9-123">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c79a9-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c79a9-124">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c79a9-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79a9-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c79a9-125">Type: **int2**</span></span>

<span data-ttu-id="c79a9-126">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c79a9-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79a9-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c79a9-127">Return value</span></span>

<span data-ttu-id="c79a9-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c79a9-128">Type: **TemplateType**</span></span>

<span data-ttu-id="c79a9-129">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="c79a9-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79a9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c79a9-130">Remarks</span></span>

<span data-ttu-id="c79a9-131">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="c79a9-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c79a9-132">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c79a9-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c79a9-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="c79a9-133">Vertex</span></span> | <span data-ttu-id="c79a9-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c79a9-134">Hull</span></span> | <span data-ttu-id="c79a9-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="c79a9-135">Domain</span></span> | <span data-ttu-id="c79a9-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="c79a9-136">Geometry</span></span> | <span data-ttu-id="c79a9-137">16x16</span><span class="sxs-lookup"><span data-stu-id="c79a9-137">Pixel</span></span> | <span data-ttu-id="c79a9-138">Computação</span><span class="sxs-lookup"><span data-stu-id="c79a9-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c79a9-139">x</span><span class="sxs-lookup"><span data-stu-id="c79a9-139">x</span></span>      | <span data-ttu-id="c79a9-140">x</span><span class="sxs-lookup"><span data-stu-id="c79a9-140">x</span></span>    | <span data-ttu-id="c79a9-141">x</span><span class="sxs-lookup"><span data-stu-id="c79a9-141">x</span></span>      | <span data-ttu-id="c79a9-142">x</span><span class="sxs-lookup"><span data-stu-id="c79a9-142">x</span></span>        | <span data-ttu-id="c79a9-143">x</span><span class="sxs-lookup"><span data-stu-id="c79a9-143">x</span></span>     | <span data-ttu-id="c79a9-144">x</span><span class="sxs-lookup"><span data-stu-id="c79a9-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c79a9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c79a9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79a9-146">Métodos GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="c79a9-146">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




