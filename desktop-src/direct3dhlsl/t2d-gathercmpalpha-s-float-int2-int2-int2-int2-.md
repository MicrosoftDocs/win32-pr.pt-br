---
title: 'Função Texture2D:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação. | Função Texture2D:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2)'
ms.assetid: C8325626-F281-4D10-9299-0E5DA01BB1BD
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
ms.openlocfilehash: f5095fdb83814ab8c7d52add0fba05cbbf876678
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968475"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2-function"></a><span data-ttu-id="2154f-105">Função Texture2D:: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="2154f-105">Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="2154f-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="2154f-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2154f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2154f-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2154f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2154f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2154f-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2154f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="2154f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2154f-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="2154f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2154f-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2154f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2154f-113">Type: **float**</span></span>

<span data-ttu-id="2154f-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="2154f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2154f-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154f-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2154f-116">Type: **float**</span></span>

<span data-ttu-id="2154f-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="2154f-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="2154f-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154f-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2154f-119">Type: **int2**</span></span>

<span data-ttu-id="2154f-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2154f-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2154f-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154f-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2154f-122">Type: **int2**</span></span>

<span data-ttu-id="2154f-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2154f-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2154f-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154f-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2154f-125">Type: **int2**</span></span>

<span data-ttu-id="2154f-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2154f-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2154f-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2154f-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2154f-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2154f-128">Type: **int2**</span></span>

<span data-ttu-id="2154f-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2154f-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2154f-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2154f-130">Return value</span></span>

<span data-ttu-id="2154f-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2154f-131">Type: **TemplateType**</span></span>

<span data-ttu-id="2154f-132">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="2154f-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2154f-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="2154f-133">Remarks</span></span>

<span data-ttu-id="2154f-134">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="2154f-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2154f-135">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2154f-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2154f-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="2154f-136">Vertex</span></span> | <span data-ttu-id="2154f-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2154f-137">Hull</span></span> | <span data-ttu-id="2154f-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="2154f-138">Domain</span></span> | <span data-ttu-id="2154f-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="2154f-139">Geometry</span></span> | <span data-ttu-id="2154f-140">16x16</span><span class="sxs-lookup"><span data-stu-id="2154f-140">Pixel</span></span> | <span data-ttu-id="2154f-141">Computação</span><span class="sxs-lookup"><span data-stu-id="2154f-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2154f-142">x</span><span class="sxs-lookup"><span data-stu-id="2154f-142">x</span></span>      | <span data-ttu-id="2154f-143">x</span><span class="sxs-lookup"><span data-stu-id="2154f-143">x</span></span>    | <span data-ttu-id="2154f-144">x</span><span class="sxs-lookup"><span data-stu-id="2154f-144">x</span></span>      | <span data-ttu-id="2154f-145">x</span><span class="sxs-lookup"><span data-stu-id="2154f-145">x</span></span>        | <span data-ttu-id="2154f-146">x</span><span class="sxs-lookup"><span data-stu-id="2154f-146">x</span></span>     | <span data-ttu-id="2154f-147">x</span><span class="sxs-lookup"><span data-stu-id="2154f-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2154f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="2154f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2154f-149">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="2154f-149">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 




