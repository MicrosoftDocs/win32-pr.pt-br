---
title: 'Função Texture2DArray:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação. | Função Texture2DArray:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2)'
ms.assetid: 0D6EC888-AB90-47C8-87D1-7B25E3EEB436
keywords:
- HLSL da função GatherCmpAlpha
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4fd93ed3925d9eaa27b369ffa44b2cc2ffde0f2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968413"
---
# <a name="texture2darraygathercmpalphasfloatfloatint2int2int2int2-function"></a><span data-ttu-id="739e5-105">Função Texture2DArray:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="739e5-105">Texture2DArray::GatherCmpAlpha(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="739e5-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="739e5-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="739e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="739e5-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="739e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="739e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="739e5-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="739e5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="739e5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="739e5-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="739e5-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="739e5-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="739e5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="739e5-113">Type: **float**</span></span>

<span data-ttu-id="739e5-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="739e5-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="739e5-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="739e5-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="739e5-116">Type: **float**</span></span>

<span data-ttu-id="739e5-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="739e5-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="739e5-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="739e5-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="739e5-119">Type: **int2**</span></span>

<span data-ttu-id="739e5-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="739e5-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="739e5-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="739e5-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="739e5-122">Type: **int2**</span></span>

<span data-ttu-id="739e5-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="739e5-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="739e5-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="739e5-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="739e5-125">Type: **int2**</span></span>

<span data-ttu-id="739e5-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="739e5-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="739e5-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="739e5-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="739e5-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="739e5-128">Type: **int2**</span></span>

<span data-ttu-id="739e5-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="739e5-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="739e5-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="739e5-130">Return value</span></span>

<span data-ttu-id="739e5-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="739e5-131">Type: **TemplateType**</span></span>

<span data-ttu-id="739e5-132">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="739e5-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="739e5-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="739e5-133">Remarks</span></span>

<span data-ttu-id="739e5-134">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="739e5-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="739e5-135">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="739e5-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="739e5-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="739e5-136">Vertex</span></span> | <span data-ttu-id="739e5-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="739e5-137">Hull</span></span> | <span data-ttu-id="739e5-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="739e5-138">Domain</span></span> | <span data-ttu-id="739e5-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="739e5-139">Geometry</span></span> | <span data-ttu-id="739e5-140">16x16</span><span class="sxs-lookup"><span data-stu-id="739e5-140">Pixel</span></span> | <span data-ttu-id="739e5-141">Computação</span><span class="sxs-lookup"><span data-stu-id="739e5-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="739e5-142">x</span><span class="sxs-lookup"><span data-stu-id="739e5-142">x</span></span>      | <span data-ttu-id="739e5-143">x</span><span class="sxs-lookup"><span data-stu-id="739e5-143">x</span></span>    | <span data-ttu-id="739e5-144">x</span><span class="sxs-lookup"><span data-stu-id="739e5-144">x</span></span>      | <span data-ttu-id="739e5-145">x</span><span class="sxs-lookup"><span data-stu-id="739e5-145">x</span></span>        | <span data-ttu-id="739e5-146">x</span><span class="sxs-lookup"><span data-stu-id="739e5-146">x</span></span>     | <span data-ttu-id="739e5-147">x</span><span class="sxs-lookup"><span data-stu-id="739e5-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="739e5-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="739e5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="739e5-149">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="739e5-149">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> </dl>

 

 




