---
title: 'Função Texture2D:: GatherCmp (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação. | Função Texture2D:: GatherCmp (S, float, float, int)'
ms.assetid: 1084bcb3-2834-400a-98ff-4e3182f63f20
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
ms.openlocfilehash: d6005d8a95d3ec5ed5cddd9c4fbe6a42f36b7f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968359"
---
# <a name="texture2dgathercmpsfloatfloatint-function"></a><span data-ttu-id="431a5-105">Função Texture2D:: GatherCmp (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="431a5-105">Texture2D::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="431a5-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="431a5-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="431a5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="431a5-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="431a5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="431a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431a5-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="431a5-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431a5-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="431a5-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="431a5-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="431a5-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="431a5-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="431a5-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431a5-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="431a5-113">Type: **float2**</span></span>

<span data-ttu-id="431a5-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="431a5-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="431a5-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="431a5-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431a5-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="431a5-116">Type: **float**</span></span>

<span data-ttu-id="431a5-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="431a5-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="431a5-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="431a5-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="431a5-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="431a5-119">Type: **int2**</span></span>

<span data-ttu-id="431a5-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="431a5-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431a5-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="431a5-121">Return value</span></span>

<span data-ttu-id="431a5-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="431a5-122">Type: **float4**</span></span>

<span data-ttu-id="431a5-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="431a5-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="431a5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="431a5-124">Remarks</span></span>

<span data-ttu-id="431a5-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="431a5-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="431a5-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="431a5-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="431a5-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="431a5-127">Vertex</span></span> | <span data-ttu-id="431a5-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="431a5-128">Hull</span></span> | <span data-ttu-id="431a5-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="431a5-129">Domain</span></span> | <span data-ttu-id="431a5-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="431a5-130">Geometry</span></span> | <span data-ttu-id="431a5-131">16x16</span><span class="sxs-lookup"><span data-stu-id="431a5-131">Pixel</span></span> | <span data-ttu-id="431a5-132">Computação</span><span class="sxs-lookup"><span data-stu-id="431a5-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="431a5-133">x</span><span class="sxs-lookup"><span data-stu-id="431a5-133">x</span></span>      | <span data-ttu-id="431a5-134">x</span><span class="sxs-lookup"><span data-stu-id="431a5-134">x</span></span>    | <span data-ttu-id="431a5-135">x</span><span class="sxs-lookup"><span data-stu-id="431a5-135">x</span></span>      | <span data-ttu-id="431a5-136">x</span><span class="sxs-lookup"><span data-stu-id="431a5-136">x</span></span>        | <span data-ttu-id="431a5-137">x</span><span class="sxs-lookup"><span data-stu-id="431a5-137">x</span></span>     | <span data-ttu-id="431a5-138">x</span><span class="sxs-lookup"><span data-stu-id="431a5-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="431a5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="431a5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431a5-140">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="431a5-140">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="431a5-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="431a5-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




