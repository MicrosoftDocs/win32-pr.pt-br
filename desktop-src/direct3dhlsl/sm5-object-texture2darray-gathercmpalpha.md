---
title: 'Função Texture2DArray:: GatherCmpAlpha (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação. | Função Texture2DArray:: GatherCmpAlpha (S, float, float, int)'
ms.assetid: d5fc78eb-2378-4e63-a712-c6f4ef9fc729
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
ms.openlocfilehash: 42f11131ebf377ddc64be5309c3edf77214ddd4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298401"
---
# <a name="texture2darraygathercmpalphasfloatfloatint-function"></a><span data-ttu-id="1e1c0-105">Função Texture2DArray:: GatherCmpAlpha (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="1e1c0-105">Texture2DArray::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="1e1c0-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1c0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e1c0-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="1e1c0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e1c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e1c0-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1e1c0-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1c0-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="1e1c0-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="1e1c0-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1e1c0-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1e1c0-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1c0-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="1e1c0-113">Type: **float3**</span></span>

<span data-ttu-id="1e1c0-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="1e1c0-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1e1c0-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1e1c0-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1c0-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1e1c0-116">Type: **float**</span></span>

<span data-ttu-id="1e1c0-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1e1c0-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1e1c0-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1c0-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1e1c0-119">Type: **int2**</span></span>

<span data-ttu-id="1e1c0-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e1c0-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e1c0-121">Return value</span></span>

<span data-ttu-id="1e1c0-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="1e1c0-122">Type: **float4**</span></span>

<span data-ttu-id="1e1c0-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e1c0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e1c0-124">Remarks</span></span>

<span data-ttu-id="1e1c0-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="1e1c0-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1e1c0-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1e1c0-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1e1c0-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="1e1c0-127">Vertex</span></span> | <span data-ttu-id="1e1c0-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1e1c0-128">Hull</span></span> | <span data-ttu-id="1e1c0-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="1e1c0-129">Domain</span></span> | <span data-ttu-id="1e1c0-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="1e1c0-130">Geometry</span></span> | <span data-ttu-id="1e1c0-131">16x16</span><span class="sxs-lookup"><span data-stu-id="1e1c0-131">Pixel</span></span> | <span data-ttu-id="1e1c0-132">Computação</span><span class="sxs-lookup"><span data-stu-id="1e1c0-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1e1c0-133">x</span><span class="sxs-lookup"><span data-stu-id="1e1c0-133">x</span></span>      | <span data-ttu-id="1e1c0-134">x</span><span class="sxs-lookup"><span data-stu-id="1e1c0-134">x</span></span>    | <span data-ttu-id="1e1c0-135">x</span><span class="sxs-lookup"><span data-stu-id="1e1c0-135">x</span></span>      | <span data-ttu-id="1e1c0-136">x</span><span class="sxs-lookup"><span data-stu-id="1e1c0-136">x</span></span>        | <span data-ttu-id="1e1c0-137">x</span><span class="sxs-lookup"><span data-stu-id="1e1c0-137">x</span></span>     | <span data-ttu-id="1e1c0-138">x</span><span class="sxs-lookup"><span data-stu-id="1e1c0-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1e1c0-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e1c0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e1c0-140">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="1e1c0-140">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="1e1c0-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1e1c0-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




