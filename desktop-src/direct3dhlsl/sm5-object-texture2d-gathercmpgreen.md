---
title: 'Função Texture2D:: GatherCmpGreen (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação. | Função Texture2D:: GatherCmpGreen (S, float, float, int)'
ms.assetid: 5a11ce0c-56b2-460a-95d7-15688dd158ff
keywords:
- HLSL da função GatherCmpGreen
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9346d8b66f90ed780e48e6fcae88e71dc9d9ca1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298268"
---
# <a name="texture2dgathercmpgreensfloatfloatint-function"></a><span data-ttu-id="482a7-105">Função Texture2D:: GatherCmpGreen (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="482a7-105">Texture2D::GatherCmpGreen(S,float,float,int) function</span></span>

<span data-ttu-id="482a7-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="482a7-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="482a7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="482a7-107">Syntax</span></span>

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="482a7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="482a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="482a7-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="482a7-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482a7-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="482a7-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="482a7-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="482a7-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="482a7-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="482a7-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482a7-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="482a7-113">Type: **float2**</span></span>

<span data-ttu-id="482a7-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="482a7-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="482a7-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="482a7-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482a7-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="482a7-116">Type: **float**</span></span>

<span data-ttu-id="482a7-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="482a7-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="482a7-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="482a7-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="482a7-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="482a7-119">Type: **int2**</span></span>

<span data-ttu-id="482a7-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="482a7-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="482a7-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="482a7-121">Return value</span></span>

<span data-ttu-id="482a7-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="482a7-122">Type: **float4**</span></span>

<span data-ttu-id="482a7-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="482a7-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="482a7-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="482a7-124">Remarks</span></span>

<span data-ttu-id="482a7-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="482a7-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="482a7-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="482a7-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="482a7-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="482a7-127">Vertex</span></span> | <span data-ttu-id="482a7-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="482a7-128">Hull</span></span> | <span data-ttu-id="482a7-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="482a7-129">Domain</span></span> | <span data-ttu-id="482a7-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="482a7-130">Geometry</span></span> | <span data-ttu-id="482a7-131">16x16</span><span class="sxs-lookup"><span data-stu-id="482a7-131">Pixel</span></span> | <span data-ttu-id="482a7-132">Computação</span><span class="sxs-lookup"><span data-stu-id="482a7-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="482a7-133">x</span><span class="sxs-lookup"><span data-stu-id="482a7-133">x</span></span>      | <span data-ttu-id="482a7-134">x</span><span class="sxs-lookup"><span data-stu-id="482a7-134">x</span></span>    | <span data-ttu-id="482a7-135">x</span><span class="sxs-lookup"><span data-stu-id="482a7-135">x</span></span>      | <span data-ttu-id="482a7-136">x</span><span class="sxs-lookup"><span data-stu-id="482a7-136">x</span></span>        | <span data-ttu-id="482a7-137">x</span><span class="sxs-lookup"><span data-stu-id="482a7-137">x</span></span>     | <span data-ttu-id="482a7-138">x</span><span class="sxs-lookup"><span data-stu-id="482a7-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="482a7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="482a7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482a7-140">Métodos GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="482a7-140">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> <dt>

[<span data-ttu-id="482a7-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="482a7-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




