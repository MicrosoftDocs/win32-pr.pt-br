---
title: 'Função Texture2DArray:: GatherRed (S, float, Int2, Int2, Int2, Int2)'
description: 'Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: GatherRed (S, float, Int2, Int2, Int2, Int2)'
ms.assetid: EB367373-D798-4CBA-AEB6-8BF89371D765
keywords:
- HLSL da função GatherRed
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a080580c3735018c9e6459acd6b742ce45e933d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930286"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2-function"></a><span data-ttu-id="efc5d-105">Função Texture2DArray:: GatherRed (S, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="efc5d-105">Texture2DArray::GatherRed(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="efc5d-106">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="efc5d-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc5d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efc5d-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="efc5d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efc5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc5d-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="efc5d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc5d-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="efc5d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="efc5d-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="efc5d-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="efc5d-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="efc5d-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc5d-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="efc5d-113">Type: **float**</span></span>

<span data-ttu-id="efc5d-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="efc5d-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="efc5d-115">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efc5d-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc5d-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="efc5d-116">Type: **int2**</span></span>

<span data-ttu-id="efc5d-117">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="efc5d-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="efc5d-118">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efc5d-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc5d-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="efc5d-119">Type: **int2**</span></span>

<span data-ttu-id="efc5d-120">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="efc5d-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="efc5d-121">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efc5d-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc5d-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="efc5d-122">Type: **int2**</span></span>

<span data-ttu-id="efc5d-123">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="efc5d-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="efc5d-124">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efc5d-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc5d-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="efc5d-125">Type: **int2**</span></span>

<span data-ttu-id="efc5d-126">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="efc5d-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc5d-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efc5d-127">Return value</span></span>

<span data-ttu-id="efc5d-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="efc5d-128">Type: **TemplateType**</span></span>

<span data-ttu-id="efc5d-129">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="efc5d-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="efc5d-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="efc5d-130">Remarks</span></span>

<span data-ttu-id="efc5d-131">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="efc5d-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="efc5d-132">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="efc5d-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="efc5d-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="efc5d-133">Vertex</span></span> | <span data-ttu-id="efc5d-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="efc5d-134">Hull</span></span> | <span data-ttu-id="efc5d-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="efc5d-135">Domain</span></span> | <span data-ttu-id="efc5d-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="efc5d-136">Geometry</span></span> | <span data-ttu-id="efc5d-137">16x16</span><span class="sxs-lookup"><span data-stu-id="efc5d-137">Pixel</span></span> | <span data-ttu-id="efc5d-138">Computação</span><span class="sxs-lookup"><span data-stu-id="efc5d-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="efc5d-139">x</span><span class="sxs-lookup"><span data-stu-id="efc5d-139">x</span></span>      | <span data-ttu-id="efc5d-140">x</span><span class="sxs-lookup"><span data-stu-id="efc5d-140">x</span></span>    | <span data-ttu-id="efc5d-141">x</span><span class="sxs-lookup"><span data-stu-id="efc5d-141">x</span></span>      | <span data-ttu-id="efc5d-142">x</span><span class="sxs-lookup"><span data-stu-id="efc5d-142">x</span></span>        | <span data-ttu-id="efc5d-143">x</span><span class="sxs-lookup"><span data-stu-id="efc5d-143">x</span></span>     | <span data-ttu-id="efc5d-144">x</span><span class="sxs-lookup"><span data-stu-id="efc5d-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="efc5d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="efc5d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc5d-146">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="efc5d-146">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 




