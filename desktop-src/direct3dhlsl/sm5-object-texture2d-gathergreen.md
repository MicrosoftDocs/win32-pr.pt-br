---
title: 'Função Texture2D:: GatherGreen (S, float, int)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação. | Função Texture2D:: GatherGreen (S, float, int)'
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
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
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989202"
---
# <a name="texture2dgathergreensfloatint-function"></a><span data-ttu-id="47507-105">Função Texture2D:: GatherGreen (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="47507-105">Texture2D::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="47507-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="47507-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="47507-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47507-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="47507-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47507-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47507-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="47507-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47507-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="47507-110">Type: **sampler**</span></span>

<span data-ttu-id="47507-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="47507-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="47507-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="47507-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47507-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="47507-113">Type: **float2**</span></span>

<span data-ttu-id="47507-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="47507-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="47507-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47507-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47507-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="47507-116">Type: **int2**</span></span>

<span data-ttu-id="47507-117">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="47507-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47507-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47507-118">Return value</span></span>

<span data-ttu-id="47507-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="47507-119">Type: **TemplateType**</span></span>

<span data-ttu-id="47507-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="47507-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="47507-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="47507-121">Remarks</span></span>

<span data-ttu-id="47507-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="47507-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="47507-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="47507-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="47507-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="47507-124">Vertex</span></span> | <span data-ttu-id="47507-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="47507-125">Hull</span></span> | <span data-ttu-id="47507-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="47507-126">Domain</span></span> | <span data-ttu-id="47507-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="47507-127">Geometry</span></span> | <span data-ttu-id="47507-128">16x16</span><span class="sxs-lookup"><span data-stu-id="47507-128">Pixel</span></span> | <span data-ttu-id="47507-129">Computação</span><span class="sxs-lookup"><span data-stu-id="47507-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="47507-130">x</span><span class="sxs-lookup"><span data-stu-id="47507-130">x</span></span>      | <span data-ttu-id="47507-131">x</span><span class="sxs-lookup"><span data-stu-id="47507-131">x</span></span>    | <span data-ttu-id="47507-132">x</span><span class="sxs-lookup"><span data-stu-id="47507-132">x</span></span>      | <span data-ttu-id="47507-133">x</span><span class="sxs-lookup"><span data-stu-id="47507-133">x</span></span>        | <span data-ttu-id="47507-134">x</span><span class="sxs-lookup"><span data-stu-id="47507-134">x</span></span>     | <span data-ttu-id="47507-135">x</span><span class="sxs-lookup"><span data-stu-id="47507-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="47507-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="47507-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47507-137">Métodos GatherGreen</span><span class="sxs-lookup"><span data-stu-id="47507-137">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="47507-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="47507-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




