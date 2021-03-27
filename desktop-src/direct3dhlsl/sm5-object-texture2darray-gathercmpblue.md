---
title: 'Função Texture2DArray:: GatherCmpBlue (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação. | Função Texture2DArray:: GatherCmpBlue (S, float, float, int)'
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
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
ms.openlocfilehash: 42c645333cc45c6de55a609439445936f65b85f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663892"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a><span data-ttu-id="766c3-105">Função Texture2DArray:: GatherCmpBlue (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="766c3-105">Texture2DArray::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="766c3-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="766c3-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="766c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="766c3-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="766c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="766c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="766c3-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="766c3-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="766c3-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="766c3-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="766c3-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="766c3-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="766c3-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="766c3-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="766c3-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="766c3-113">Type: **float3**</span></span>

<span data-ttu-id="766c3-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="766c3-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="766c3-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="766c3-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="766c3-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="766c3-116">Type: **float**</span></span>

<span data-ttu-id="766c3-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="766c3-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="766c3-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="766c3-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="766c3-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="766c3-119">Type: **int2**</span></span>

<span data-ttu-id="766c3-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="766c3-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="766c3-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="766c3-121">Return value</span></span>

<span data-ttu-id="766c3-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="766c3-122">Type: **float4**</span></span>

<span data-ttu-id="766c3-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="766c3-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="766c3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="766c3-124">Remarks</span></span>

<span data-ttu-id="766c3-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="766c3-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="766c3-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="766c3-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="766c3-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="766c3-127">Vertex</span></span> | <span data-ttu-id="766c3-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="766c3-128">Hull</span></span> | <span data-ttu-id="766c3-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="766c3-129">Domain</span></span> | <span data-ttu-id="766c3-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="766c3-130">Geometry</span></span> | <span data-ttu-id="766c3-131">16x16</span><span class="sxs-lookup"><span data-stu-id="766c3-131">Pixel</span></span> | <span data-ttu-id="766c3-132">Computação</span><span class="sxs-lookup"><span data-stu-id="766c3-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="766c3-133">x</span><span class="sxs-lookup"><span data-stu-id="766c3-133">x</span></span>      | <span data-ttu-id="766c3-134">x</span><span class="sxs-lookup"><span data-stu-id="766c3-134">x</span></span>    | <span data-ttu-id="766c3-135">x</span><span class="sxs-lookup"><span data-stu-id="766c3-135">x</span></span>      | <span data-ttu-id="766c3-136">x</span><span class="sxs-lookup"><span data-stu-id="766c3-136">x</span></span>        | <span data-ttu-id="766c3-137">x</span><span class="sxs-lookup"><span data-stu-id="766c3-137">x</span></span>     | <span data-ttu-id="766c3-138">x</span><span class="sxs-lookup"><span data-stu-id="766c3-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="766c3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="766c3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766c3-140">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="766c3-140">GatherCmpBlue methods</span></span>](texture2darray-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="766c3-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="766c3-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




