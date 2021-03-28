---
title: 'Função Texture2DArray:: gather (S, float, int)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: gather (S, float, int)'
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Coletar HLSL da função
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989145"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="03ea3-105">Função Texture2DArray:: gather (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="03ea3-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="03ea3-106">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="03ea3-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ea3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03ea3-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="03ea3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03ea3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ea3-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="03ea3-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ea3-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="03ea3-110">Type: **sampler**</span></span>

<span data-ttu-id="03ea3-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="03ea3-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="03ea3-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="03ea3-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ea3-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="03ea3-113">Type: **float3**</span></span>

<span data-ttu-id="03ea3-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="03ea3-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="03ea3-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03ea3-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ea3-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="03ea3-116">Type: **int2**</span></span>

<span data-ttu-id="03ea3-117">O deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="03ea3-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ea3-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03ea3-118">Return value</span></span>

<span data-ttu-id="03ea3-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="03ea3-119">Type: **TemplateType**</span></span>

<span data-ttu-id="03ea3-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="03ea3-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="03ea3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="03ea3-121">Remarks</span></span>

<span data-ttu-id="03ea3-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="03ea3-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="03ea3-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="03ea3-123">Vertex</span></span> | <span data-ttu-id="03ea3-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="03ea3-124">Hull</span></span> | <span data-ttu-id="03ea3-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="03ea3-125">Domain</span></span> | <span data-ttu-id="03ea3-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="03ea3-126">Geometry</span></span> | <span data-ttu-id="03ea3-127">16x16</span><span class="sxs-lookup"><span data-stu-id="03ea3-127">Pixel</span></span> | <span data-ttu-id="03ea3-128">Computação</span><span class="sxs-lookup"><span data-stu-id="03ea3-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="03ea3-129">x</span><span class="sxs-lookup"><span data-stu-id="03ea3-129">x</span></span>      | <span data-ttu-id="03ea3-130">x</span><span class="sxs-lookup"><span data-stu-id="03ea3-130">x</span></span>    | <span data-ttu-id="03ea3-131">x</span><span class="sxs-lookup"><span data-stu-id="03ea3-131">x</span></span>      | <span data-ttu-id="03ea3-132">x</span><span class="sxs-lookup"><span data-stu-id="03ea3-132">x</span></span>        | <span data-ttu-id="03ea3-133">x</span><span class="sxs-lookup"><span data-stu-id="03ea3-133">x</span></span>     | <span data-ttu-id="03ea3-134">x</span><span class="sxs-lookup"><span data-stu-id="03ea3-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="03ea3-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="03ea3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ea3-136">Reunir métodos</span><span class="sxs-lookup"><span data-stu-id="03ea3-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="03ea3-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="03ea3-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




