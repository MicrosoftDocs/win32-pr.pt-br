---
title: 'Função Texture2DArray:: GatherGreen (S, float, int)'
description: 'Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: GatherGreen (S, float, int)'
ms.assetid: bfe9ab9f-64f7-4a50-aa46-2ec6effebce2
keywords:
- HLSL da função GatherGreen
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48a5d968ffe5eeb12fdb0240d1823a9b1834ae19
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172622"
---
# <a name="texture2darraygathergreensfloatint-function"></a><span data-ttu-id="bae66-105">Função Texture2DArray:: GatherGreen (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="bae66-105">Texture2DArray::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="bae66-106">Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="bae66-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae66-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bae66-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="bae66-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bae66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae66-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="bae66-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae66-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="bae66-110">Type: **sampler**</span></span>

<span data-ttu-id="bae66-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="bae66-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="bae66-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="bae66-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae66-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="bae66-113">Type: **float3**</span></span>

<span data-ttu-id="bae66-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="bae66-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="bae66-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bae66-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bae66-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="bae66-116">Type: **int2**</span></span>

<span data-ttu-id="bae66-117">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="bae66-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae66-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bae66-118">Return value</span></span>

<span data-ttu-id="bae66-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="bae66-119">Type: **TemplateType**</span></span>

<span data-ttu-id="bae66-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="bae66-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="bae66-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bae66-121">Remarks</span></span>

<span data-ttu-id="bae66-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="bae66-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="bae66-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="bae66-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bae66-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="bae66-124">Vertex</span></span> | <span data-ttu-id="bae66-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="bae66-125">Hull</span></span> | <span data-ttu-id="bae66-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="bae66-126">Domain</span></span> | <span data-ttu-id="bae66-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="bae66-127">Geometry</span></span> | <span data-ttu-id="bae66-128">16x16</span><span class="sxs-lookup"><span data-stu-id="bae66-128">Pixel</span></span> | <span data-ttu-id="bae66-129">Computação</span><span class="sxs-lookup"><span data-stu-id="bae66-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bae66-130">x</span><span class="sxs-lookup"><span data-stu-id="bae66-130">x</span></span>      | <span data-ttu-id="bae66-131">x</span><span class="sxs-lookup"><span data-stu-id="bae66-131">x</span></span>    | <span data-ttu-id="bae66-132">x</span><span class="sxs-lookup"><span data-stu-id="bae66-132">x</span></span>      | <span data-ttu-id="bae66-133">x</span><span class="sxs-lookup"><span data-stu-id="bae66-133">x</span></span>        | <span data-ttu-id="bae66-134">x</span><span class="sxs-lookup"><span data-stu-id="bae66-134">x</span></span>     | <span data-ttu-id="bae66-135">x</span><span class="sxs-lookup"><span data-stu-id="bae66-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bae66-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="bae66-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae66-137">Métodos GatherGreen</span><span class="sxs-lookup"><span data-stu-id="bae66-137">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="bae66-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bae66-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




