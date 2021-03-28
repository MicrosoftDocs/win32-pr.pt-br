---
title: 'Função Texture2D:: GatherAlpha (S, float, int)'
description: 'Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: GatherAlpha (S, float, int)'
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
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
ms.openlocfilehash: 36561e6bc16a84e0a377292ededf58df3c15f800
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968466"
---
# <a name="texture2dgatheralphasfloatint-function"></a><span data-ttu-id="3560b-105">Função Texture2D:: GatherAlpha (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="3560b-105">Texture2D::GatherAlpha(S,float,int) function</span></span>

<span data-ttu-id="3560b-106">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="3560b-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3560b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3560b-107">Syntax</span></span>

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="3560b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3560b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3560b-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3560b-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3560b-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="3560b-110">Type: **sampler**</span></span>

<span data-ttu-id="3560b-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="3560b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="3560b-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3560b-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3560b-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="3560b-113">Type: **float2**</span></span>

<span data-ttu-id="3560b-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="3560b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="3560b-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3560b-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3560b-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="3560b-116">Type: **int2**</span></span>

<span data-ttu-id="3560b-117">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="3560b-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3560b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3560b-118">Return value</span></span>

<span data-ttu-id="3560b-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="3560b-119">Type: **TemplateType**</span></span>

<span data-ttu-id="3560b-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="3560b-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3560b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3560b-121">Remarks</span></span>

<span data-ttu-id="3560b-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="3560b-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3560b-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3560b-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3560b-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="3560b-124">Vertex</span></span> | <span data-ttu-id="3560b-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3560b-125">Hull</span></span> | <span data-ttu-id="3560b-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="3560b-126">Domain</span></span> | <span data-ttu-id="3560b-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="3560b-127">Geometry</span></span> | <span data-ttu-id="3560b-128">16x16</span><span class="sxs-lookup"><span data-stu-id="3560b-128">Pixel</span></span> | <span data-ttu-id="3560b-129">Computação</span><span class="sxs-lookup"><span data-stu-id="3560b-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3560b-130">x</span><span class="sxs-lookup"><span data-stu-id="3560b-130">x</span></span>      | <span data-ttu-id="3560b-131">x</span><span class="sxs-lookup"><span data-stu-id="3560b-131">x</span></span>    | <span data-ttu-id="3560b-132">x</span><span class="sxs-lookup"><span data-stu-id="3560b-132">x</span></span>      | <span data-ttu-id="3560b-133">x</span><span class="sxs-lookup"><span data-stu-id="3560b-133">x</span></span>        | <span data-ttu-id="3560b-134">x</span><span class="sxs-lookup"><span data-stu-id="3560b-134">x</span></span>     | <span data-ttu-id="3560b-135">x</span><span class="sxs-lookup"><span data-stu-id="3560b-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3560b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3560b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3560b-137">Métodos GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="3560b-137">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="3560b-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3560b-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




