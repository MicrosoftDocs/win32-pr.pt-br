---
title: 'Função Texture2DArray:: GatherCmp (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação. | Função Texture2DArray:: GatherCmp (S, float, float, int)'
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
keywords:
- HLSL da função GatherCmp
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbac4c231f7a7070d3ca4549f3d1189b81292b8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968312"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a><span data-ttu-id="906b2-105">Função Texture2DArray:: GatherCmp (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="906b2-105">Texture2DArray::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="906b2-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="906b2-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="906b2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="906b2-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="906b2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="906b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906b2-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="906b2-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906b2-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="906b2-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="906b2-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="906b2-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="906b2-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="906b2-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906b2-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="906b2-113">Type: **float3**</span></span>

<span data-ttu-id="906b2-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="906b2-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="906b2-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="906b2-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906b2-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="906b2-116">Type: **float**</span></span>

<span data-ttu-id="906b2-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="906b2-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="906b2-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="906b2-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906b2-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="906b2-119">Type: **int2**</span></span>

<span data-ttu-id="906b2-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="906b2-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906b2-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="906b2-121">Return value</span></span>

<span data-ttu-id="906b2-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="906b2-122">Type: **float4**</span></span>

<span data-ttu-id="906b2-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="906b2-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="906b2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="906b2-124">Remarks</span></span>

<span data-ttu-id="906b2-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="906b2-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="906b2-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="906b2-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="906b2-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="906b2-127">Vertex</span></span> | <span data-ttu-id="906b2-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="906b2-128">Hull</span></span> | <span data-ttu-id="906b2-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="906b2-129">Domain</span></span> | <span data-ttu-id="906b2-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="906b2-130">Geometry</span></span> | <span data-ttu-id="906b2-131">16x16</span><span class="sxs-lookup"><span data-stu-id="906b2-131">Pixel</span></span> | <span data-ttu-id="906b2-132">Computação</span><span class="sxs-lookup"><span data-stu-id="906b2-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="906b2-133">x</span><span class="sxs-lookup"><span data-stu-id="906b2-133">x</span></span>      | <span data-ttu-id="906b2-134">x</span><span class="sxs-lookup"><span data-stu-id="906b2-134">x</span></span>    | <span data-ttu-id="906b2-135">x</span><span class="sxs-lookup"><span data-stu-id="906b2-135">x</span></span>      | <span data-ttu-id="906b2-136">x</span><span class="sxs-lookup"><span data-stu-id="906b2-136">x</span></span>        | <span data-ttu-id="906b2-137">x</span><span class="sxs-lookup"><span data-stu-id="906b2-137">x</span></span>     | <span data-ttu-id="906b2-138">x</span><span class="sxs-lookup"><span data-stu-id="906b2-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="906b2-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="906b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906b2-140">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="906b2-140">GatherCmp methods</span></span>](texture2darray-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="906b2-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="906b2-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




