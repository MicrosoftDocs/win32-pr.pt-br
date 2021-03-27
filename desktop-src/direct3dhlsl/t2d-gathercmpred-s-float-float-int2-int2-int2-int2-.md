---
title: 'Função Texture2D:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação. | Função Texture2D:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2)'
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
keywords:
- HLSL da função GatherCmpRed
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f84467c798337ac2cc81283637636900933c9e41
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930361"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a><span data-ttu-id="1d825-105">Função Texture2D:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="1d825-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="1d825-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="1d825-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d825-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d825-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="1d825-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d825-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d825-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1d825-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="1d825-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1d825-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="1d825-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1d825-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1d825-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1d825-113">Type: **float**</span></span>

<span data-ttu-id="1d825-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="1d825-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1d825-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d825-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1d825-116">Type: **float**</span></span>

<span data-ttu-id="1d825-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="1d825-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1d825-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d825-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1d825-119">Type: **int2**</span></span>

<span data-ttu-id="1d825-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1d825-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1d825-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d825-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1d825-122">Type: **int2**</span></span>

<span data-ttu-id="1d825-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1d825-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1d825-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d825-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1d825-125">Type: **int2**</span></span>

<span data-ttu-id="1d825-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1d825-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1d825-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d825-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d825-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1d825-128">Type: **int2**</span></span>

<span data-ttu-id="1d825-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1d825-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d825-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d825-130">Return value</span></span>

<span data-ttu-id="1d825-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1d825-131">Type: **TemplateType**</span></span>

<span data-ttu-id="1d825-132">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="1d825-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d825-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d825-133">Remarks</span></span>

<span data-ttu-id="1d825-134">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="1d825-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1d825-135">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1d825-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1d825-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="1d825-136">Vertex</span></span> | <span data-ttu-id="1d825-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1d825-137">Hull</span></span> | <span data-ttu-id="1d825-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="1d825-138">Domain</span></span> | <span data-ttu-id="1d825-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="1d825-139">Geometry</span></span> | <span data-ttu-id="1d825-140">16x16</span><span class="sxs-lookup"><span data-stu-id="1d825-140">Pixel</span></span> | <span data-ttu-id="1d825-141">Computação</span><span class="sxs-lookup"><span data-stu-id="1d825-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1d825-142">x</span><span class="sxs-lookup"><span data-stu-id="1d825-142">x</span></span>      | <span data-ttu-id="1d825-143">x</span><span class="sxs-lookup"><span data-stu-id="1d825-143">x</span></span>    | <span data-ttu-id="1d825-144">x</span><span class="sxs-lookup"><span data-stu-id="1d825-144">x</span></span>      | <span data-ttu-id="1d825-145">x</span><span class="sxs-lookup"><span data-stu-id="1d825-145">x</span></span>        | <span data-ttu-id="1d825-146">x</span><span class="sxs-lookup"><span data-stu-id="1d825-146">x</span></span>     | <span data-ttu-id="1d825-147">x</span><span class="sxs-lookup"><span data-stu-id="1d825-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1d825-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d825-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d825-149">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="1d825-149">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 




