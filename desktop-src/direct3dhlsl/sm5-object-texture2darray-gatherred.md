---
title: 'Função Texture2DArray:: GatherRed (S, float, int)'
description: 'Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: GatherRed (S, float, int)'
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
keywords:
- HLSL da função GatherRed
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 431d08b77d13540bb48621a6d5ec76f4c775f796
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989200"
---
# <a name="texture2darraygatherredsfloatint-function"></a><span data-ttu-id="17fed-105">Função Texture2DArray:: GatherRed (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="17fed-105">Texture2DArray::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="17fed-106">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="17fed-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17fed-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="17fed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17fed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17fed-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="17fed-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fed-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="17fed-110">Type: **sampler**</span></span>

<span data-ttu-id="17fed-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="17fed-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="17fed-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="17fed-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fed-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="17fed-113">Type: **float3**</span></span>

<span data-ttu-id="17fed-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="17fed-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="17fed-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17fed-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fed-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="17fed-116">Type: **int2**</span></span>

<span data-ttu-id="17fed-117">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="17fed-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17fed-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17fed-118">Return value</span></span>

<span data-ttu-id="17fed-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="17fed-119">Type: **TemplateType**</span></span>

<span data-ttu-id="17fed-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="17fed-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="17fed-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="17fed-121">Remarks</span></span>

<span data-ttu-id="17fed-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="17fed-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="17fed-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="17fed-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="17fed-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="17fed-124">Vertex</span></span> | <span data-ttu-id="17fed-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="17fed-125">Hull</span></span> | <span data-ttu-id="17fed-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="17fed-126">Domain</span></span> | <span data-ttu-id="17fed-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="17fed-127">Geometry</span></span> | <span data-ttu-id="17fed-128">16x16</span><span class="sxs-lookup"><span data-stu-id="17fed-128">Pixel</span></span> | <span data-ttu-id="17fed-129">Computação</span><span class="sxs-lookup"><span data-stu-id="17fed-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="17fed-130">x</span><span class="sxs-lookup"><span data-stu-id="17fed-130">x</span></span>      | <span data-ttu-id="17fed-131">x</span><span class="sxs-lookup"><span data-stu-id="17fed-131">x</span></span>    | <span data-ttu-id="17fed-132">x</span><span class="sxs-lookup"><span data-stu-id="17fed-132">x</span></span>      | <span data-ttu-id="17fed-133">x</span><span class="sxs-lookup"><span data-stu-id="17fed-133">x</span></span>        | <span data-ttu-id="17fed-134">x</span><span class="sxs-lookup"><span data-stu-id="17fed-134">x</span></span>     | <span data-ttu-id="17fed-135">x</span><span class="sxs-lookup"><span data-stu-id="17fed-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="17fed-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="17fed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fed-137">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="17fed-137">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> <dt>

[<span data-ttu-id="17fed-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="17fed-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




