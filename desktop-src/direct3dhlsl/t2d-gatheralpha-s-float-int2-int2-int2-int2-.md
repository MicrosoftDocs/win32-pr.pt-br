---
title: 'Função Texture2D:: GatherAlpha (S, float, Int2, Int2, Int2, Int2)'
description: 'Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: GatherAlpha (S, float, Int2, Int2, Int2, Int2)'
ms.assetid: 925A5085-33CB-4DFC-B4E3-1ADA5892C13A
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
ms.openlocfilehash: 4dc2077c8c10d9a7caba1c9d7a3999ffd522b5ab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989230"
---
# <a name="texture2dgatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="2bf52-105">Função Texture2D:: GatherAlpha (S, float, Int2, Int2, Int2, Int2)</span><span class="sxs-lookup"><span data-stu-id="2bf52-105">Texture2D::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="2bf52-106">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="2bf52-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf52-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bf52-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2bf52-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bf52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf52-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2bf52-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf52-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="2bf52-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2bf52-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="2bf52-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2bf52-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2bf52-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf52-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2bf52-113">Type: **float**</span></span>

<span data-ttu-id="2bf52-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="2bf52-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2bf52-115">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bf52-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf52-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2bf52-116">Type: **int2**</span></span>

<span data-ttu-id="2bf52-117">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2bf52-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2bf52-118">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bf52-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf52-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2bf52-119">Type: **int2**</span></span>

<span data-ttu-id="2bf52-120">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2bf52-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2bf52-121">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bf52-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf52-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2bf52-122">Type: **int2**</span></span>

<span data-ttu-id="2bf52-123">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2bf52-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2bf52-124">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bf52-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf52-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2bf52-125">Type: **int2**</span></span>

<span data-ttu-id="2bf52-126">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2bf52-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf52-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bf52-127">Return value</span></span>

<span data-ttu-id="2bf52-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2bf52-128">Type: **TemplateType**</span></span>

<span data-ttu-id="2bf52-129">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="2bf52-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf52-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bf52-130">Remarks</span></span>

<span data-ttu-id="2bf52-131">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="2bf52-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2bf52-132">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2bf52-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2bf52-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="2bf52-133">Vertex</span></span> | <span data-ttu-id="2bf52-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2bf52-134">Hull</span></span> | <span data-ttu-id="2bf52-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="2bf52-135">Domain</span></span> | <span data-ttu-id="2bf52-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="2bf52-136">Geometry</span></span> | <span data-ttu-id="2bf52-137">16x16</span><span class="sxs-lookup"><span data-stu-id="2bf52-137">Pixel</span></span> | <span data-ttu-id="2bf52-138">Computação</span><span class="sxs-lookup"><span data-stu-id="2bf52-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2bf52-139">x</span><span class="sxs-lookup"><span data-stu-id="2bf52-139">x</span></span>      | <span data-ttu-id="2bf52-140">x</span><span class="sxs-lookup"><span data-stu-id="2bf52-140">x</span></span>    | <span data-ttu-id="2bf52-141">x</span><span class="sxs-lookup"><span data-stu-id="2bf52-141">x</span></span>      | <span data-ttu-id="2bf52-142">x</span><span class="sxs-lookup"><span data-stu-id="2bf52-142">x</span></span>        | <span data-ttu-id="2bf52-143">x</span><span class="sxs-lookup"><span data-stu-id="2bf52-143">x</span></span>     | <span data-ttu-id="2bf52-144">x</span><span class="sxs-lookup"><span data-stu-id="2bf52-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2bf52-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bf52-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf52-146">Métodos GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="2bf52-146">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> </dl>

 

 




