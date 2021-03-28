---
title: 'Função Texture2D:: GatherRed (S, float, Int2, Int2, Int2, Int2)'
description: 'Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: GatherRed (S, float, Int2, Int2, Int2, Int2)'
ms.assetid: 85C321CB-B77C-430B-921D-D56E5597B24A
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
ms.openlocfilehash: b17e192388b6fc439d31cfe35eca99168da1c3f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172605"
---
# <a name="texture2dgatherredsfloatint2int2int2int2-function"></a><span data-ttu-id="df0cc-105">Função Texture2D:: GatherRed (S, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="df0cc-105">Texture2D::GatherRed(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="df0cc-106">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="df0cc-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df0cc-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="df0cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df0cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0cc-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="df0cc-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0cc-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="df0cc-110">Type: **SamplerState**</span></span>

<span data-ttu-id="df0cc-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="df0cc-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="df0cc-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="df0cc-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0cc-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="df0cc-113">Type: **float**</span></span>

<span data-ttu-id="df0cc-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="df0cc-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="df0cc-115">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df0cc-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0cc-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="df0cc-116">Type: **int2**</span></span>

<span data-ttu-id="df0cc-117">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="df0cc-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="df0cc-118">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df0cc-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0cc-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="df0cc-119">Type: **int2**</span></span>

<span data-ttu-id="df0cc-120">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="df0cc-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="df0cc-121">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df0cc-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0cc-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="df0cc-122">Type: **int2**</span></span>

<span data-ttu-id="df0cc-123">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="df0cc-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="df0cc-124">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df0cc-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0cc-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="df0cc-125">Type: **int2**</span></span>

<span data-ttu-id="df0cc-126">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="df0cc-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0cc-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df0cc-127">Return value</span></span>

<span data-ttu-id="df0cc-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="df0cc-128">Type: **TemplateType**</span></span>

<span data-ttu-id="df0cc-129">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="df0cc-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="df0cc-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="df0cc-130">Remarks</span></span>

<span data-ttu-id="df0cc-131">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="df0cc-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="df0cc-132">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="df0cc-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="df0cc-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="df0cc-133">Vertex</span></span> | <span data-ttu-id="df0cc-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="df0cc-134">Hull</span></span> | <span data-ttu-id="df0cc-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="df0cc-135">Domain</span></span> | <span data-ttu-id="df0cc-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="df0cc-136">Geometry</span></span> | <span data-ttu-id="df0cc-137">16x16</span><span class="sxs-lookup"><span data-stu-id="df0cc-137">Pixel</span></span> | <span data-ttu-id="df0cc-138">Computação</span><span class="sxs-lookup"><span data-stu-id="df0cc-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="df0cc-139">x</span><span class="sxs-lookup"><span data-stu-id="df0cc-139">x</span></span>      | <span data-ttu-id="df0cc-140">x</span><span class="sxs-lookup"><span data-stu-id="df0cc-140">x</span></span>    | <span data-ttu-id="df0cc-141">x</span><span class="sxs-lookup"><span data-stu-id="df0cc-141">x</span></span>      | <span data-ttu-id="df0cc-142">x</span><span class="sxs-lookup"><span data-stu-id="df0cc-142">x</span></span>        | <span data-ttu-id="df0cc-143">x</span><span class="sxs-lookup"><span data-stu-id="df0cc-143">x</span></span>     | <span data-ttu-id="df0cc-144">x</span><span class="sxs-lookup"><span data-stu-id="df0cc-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="df0cc-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="df0cc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0cc-146">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="df0cc-146">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> </dl>

 

 




