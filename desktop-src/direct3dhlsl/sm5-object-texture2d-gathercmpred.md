---
title: 'Função Texture2D:: GatherCmpRed (S, float, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação. | Função Texture2D:: GatherCmpRed (S, float, float, int)'
ms.assetid: bd5fdd3b-c1b0-4cb0-aec5-9fe020420e6c
keywords:
- HLSL da função GatherCmpRed
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e221dbe60141eb809d41361a0a6a93d8bf2a7d7e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298267"
---
# <a name="texture2dgathercmpredsfloatfloatint-function"></a><span data-ttu-id="3a361-105">Função Texture2D:: GatherCmpRed (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="3a361-105">Texture2D::GatherCmpRed(S,float,float,int) function</span></span>

<span data-ttu-id="3a361-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="3a361-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a361-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a361-107">Syntax</span></span>

``` syntax
float4 GatherCmpRed(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="3a361-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a361-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a361-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3a361-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a361-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="3a361-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="3a361-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="3a361-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="3a361-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3a361-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a361-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="3a361-113">Type: **float2**</span></span>

<span data-ttu-id="3a361-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="3a361-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="3a361-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3a361-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a361-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3a361-116">Type: **float**</span></span>

<span data-ttu-id="3a361-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="3a361-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="3a361-118">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a361-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a361-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="3a361-119">Type: **int2**</span></span>

<span data-ttu-id="3a361-120">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="3a361-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a361-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a361-121">Return value</span></span>

<span data-ttu-id="3a361-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="3a361-122">Type: **float4**</span></span>

<span data-ttu-id="3a361-123">Um valor de quatro componentes, cada componente é o resultado de uma comparação por componente.</span><span class="sxs-lookup"><span data-stu-id="3a361-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a361-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a361-124">Remarks</span></span>

<span data-ttu-id="3a361-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="3a361-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3a361-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3a361-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3a361-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="3a361-127">Vertex</span></span> | <span data-ttu-id="3a361-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3a361-128">Hull</span></span> | <span data-ttu-id="3a361-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="3a361-129">Domain</span></span> | <span data-ttu-id="3a361-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="3a361-130">Geometry</span></span> | <span data-ttu-id="3a361-131">16x16</span><span class="sxs-lookup"><span data-stu-id="3a361-131">Pixel</span></span> | <span data-ttu-id="3a361-132">Computação</span><span class="sxs-lookup"><span data-stu-id="3a361-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3a361-133">x</span><span class="sxs-lookup"><span data-stu-id="3a361-133">x</span></span>      | <span data-ttu-id="3a361-134">x</span><span class="sxs-lookup"><span data-stu-id="3a361-134">x</span></span>    | <span data-ttu-id="3a361-135">x</span><span class="sxs-lookup"><span data-stu-id="3a361-135">x</span></span>      | <span data-ttu-id="3a361-136">x</span><span class="sxs-lookup"><span data-stu-id="3a361-136">x</span></span>        | <span data-ttu-id="3a361-137">x</span><span class="sxs-lookup"><span data-stu-id="3a361-137">x</span></span>     | <span data-ttu-id="3a361-138">x</span><span class="sxs-lookup"><span data-stu-id="3a361-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a361-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a361-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a361-140">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="3a361-140">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> <dt>

[<span data-ttu-id="3a361-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3a361-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




