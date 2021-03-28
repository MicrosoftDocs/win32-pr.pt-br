---
title: 'Função Texture2D:: GatherCmpBlue (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação. | Função Texture2D:: GatherCmpBlue (S, float, float, int)'
ms.assetid: d8e03c55-18f1-4598-a700-9ba3a680d78a
keywords:
- HLSL da função GatherCmpBlue
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eedeb21141c1e694effe4eb8c7be70c828aa0a3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989166"
---
# <a name="texture2dgathercmpbluesfloatfloatint-function"></a><span data-ttu-id="baec6-105">Função Texture2D:: GatherCmpBlue (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="baec6-105">Texture2D::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="baec6-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="baec6-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="baec6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baec6-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="baec6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baec6-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="baec6-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baec6-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="baec6-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="baec6-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="baec6-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="baec6-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="baec6-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baec6-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="baec6-113">Type: **float2**</span></span>

<span data-ttu-id="baec6-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="baec6-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="baec6-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="baec6-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baec6-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="baec6-116">Type: **float**</span></span>

<span data-ttu-id="baec6-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="baec6-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="baec6-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="baec6-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baec6-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="baec6-119">Type: **int2**</span></span>

<span data-ttu-id="baec6-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="baec6-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baec6-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baec6-121">Return value</span></span>

<span data-ttu-id="baec6-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="baec6-122">Type: **float4**</span></span>

<span data-ttu-id="baec6-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="baec6-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="baec6-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="baec6-124">Remarks</span></span>

<span data-ttu-id="baec6-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="baec6-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="baec6-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="baec6-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="baec6-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="baec6-127">Vertex</span></span> | <span data-ttu-id="baec6-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="baec6-128">Hull</span></span> | <span data-ttu-id="baec6-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="baec6-129">Domain</span></span> | <span data-ttu-id="baec6-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="baec6-130">Geometry</span></span> | <span data-ttu-id="baec6-131">16x16</span><span class="sxs-lookup"><span data-stu-id="baec6-131">Pixel</span></span> | <span data-ttu-id="baec6-132">Computação</span><span class="sxs-lookup"><span data-stu-id="baec6-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="baec6-133">x</span><span class="sxs-lookup"><span data-stu-id="baec6-133">x</span></span>      | <span data-ttu-id="baec6-134">x</span><span class="sxs-lookup"><span data-stu-id="baec6-134">x</span></span>    | <span data-ttu-id="baec6-135">x</span><span class="sxs-lookup"><span data-stu-id="baec6-135">x</span></span>      | <span data-ttu-id="baec6-136">x</span><span class="sxs-lookup"><span data-stu-id="baec6-136">x</span></span>        | <span data-ttu-id="baec6-137">x</span><span class="sxs-lookup"><span data-stu-id="baec6-137">x</span></span>     | <span data-ttu-id="baec6-138">x</span><span class="sxs-lookup"><span data-stu-id="baec6-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="baec6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="baec6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baec6-140">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="baec6-140">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="baec6-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="baec6-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




