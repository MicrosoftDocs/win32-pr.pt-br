---
title: 'Função Texture2D:: GatherCmpAlpha (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação. | Função Texture2D:: GatherCmpAlpha (S, float, float, int)'
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
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
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370846"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a><span data-ttu-id="e3dfa-105">Função Texture2D:: GatherCmpAlpha (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="e3dfa-105">Texture2D::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="e3dfa-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="e3dfa-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dfa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3dfa-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="e3dfa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3dfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3dfa-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e3dfa-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dfa-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="e3dfa-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="e3dfa-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="e3dfa-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e3dfa-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e3dfa-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dfa-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="e3dfa-113">Type: **float2**</span></span>

<span data-ttu-id="e3dfa-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="e3dfa-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e3dfa-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e3dfa-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dfa-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e3dfa-116">Type: **float**</span></span>

<span data-ttu-id="e3dfa-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="e3dfa-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="e3dfa-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3dfa-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dfa-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="e3dfa-119">Type: **int2**</span></span>

<span data-ttu-id="e3dfa-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e3dfa-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3dfa-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3dfa-121">Return value</span></span>

<span data-ttu-id="e3dfa-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e3dfa-122">Type: **float4**</span></span>

<span data-ttu-id="e3dfa-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="e3dfa-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dfa-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3dfa-124">Remarks</span></span>

<span data-ttu-id="e3dfa-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="e3dfa-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e3dfa-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e3dfa-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e3dfa-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="e3dfa-127">Vertex</span></span> | <span data-ttu-id="e3dfa-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e3dfa-128">Hull</span></span> | <span data-ttu-id="e3dfa-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="e3dfa-129">Domain</span></span> | <span data-ttu-id="e3dfa-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="e3dfa-130">Geometry</span></span> | <span data-ttu-id="e3dfa-131">16x16</span><span class="sxs-lookup"><span data-stu-id="e3dfa-131">Pixel</span></span> | <span data-ttu-id="e3dfa-132">Computação</span><span class="sxs-lookup"><span data-stu-id="e3dfa-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e3dfa-133">x</span><span class="sxs-lookup"><span data-stu-id="e3dfa-133">x</span></span>      | <span data-ttu-id="e3dfa-134">x</span><span class="sxs-lookup"><span data-stu-id="e3dfa-134">x</span></span>    | <span data-ttu-id="e3dfa-135">x</span><span class="sxs-lookup"><span data-stu-id="e3dfa-135">x</span></span>      | <span data-ttu-id="e3dfa-136">x</span><span class="sxs-lookup"><span data-stu-id="e3dfa-136">x</span></span>        | <span data-ttu-id="e3dfa-137">x</span><span class="sxs-lookup"><span data-stu-id="e3dfa-137">x</span></span>     | <span data-ttu-id="e3dfa-138">x</span><span class="sxs-lookup"><span data-stu-id="e3dfa-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e3dfa-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3dfa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dfa-140">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="e3dfa-140">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="e3dfa-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e3dfa-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




