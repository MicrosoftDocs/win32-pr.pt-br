---
title: 'Função Texture2D:: GatherBlue (S, float, int)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: GatherBlue (S, float, int)'
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
keywords:
- HLSL da função GatherBlue
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54885ccd8f31fdf55270b6c9ac2dbafa1805d866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968391"
---
# <a name="texture2dgatherbluesfloatint-function"></a><span data-ttu-id="00d1c-105">Função Texture2D:: GatherBlue (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="00d1c-105">Texture2D::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="00d1c-106">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="00d1c-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d1c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00d1c-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="00d1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00d1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d1c-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="00d1c-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d1c-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="00d1c-110">Type: **sampler**</span></span>

<span data-ttu-id="00d1c-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="00d1c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="00d1c-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="00d1c-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d1c-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="00d1c-113">Type: **float2**</span></span>

<span data-ttu-id="00d1c-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="00d1c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="00d1c-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00d1c-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d1c-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="00d1c-116">Type: **int2**</span></span>

<span data-ttu-id="00d1c-117">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="00d1c-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d1c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00d1c-118">Return value</span></span>

<span data-ttu-id="00d1c-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="00d1c-119">Type: **TemplateType**</span></span>

<span data-ttu-id="00d1c-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="00d1c-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d1c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="00d1c-121">Remarks</span></span>

<span data-ttu-id="00d1c-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="00d1c-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="00d1c-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="00d1c-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="00d1c-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="00d1c-124">Vertex</span></span> | <span data-ttu-id="00d1c-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="00d1c-125">Hull</span></span> | <span data-ttu-id="00d1c-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="00d1c-126">Domain</span></span> | <span data-ttu-id="00d1c-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="00d1c-127">Geometry</span></span> | <span data-ttu-id="00d1c-128">16x16</span><span class="sxs-lookup"><span data-stu-id="00d1c-128">Pixel</span></span> | <span data-ttu-id="00d1c-129">Computação</span><span class="sxs-lookup"><span data-stu-id="00d1c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="00d1c-130">x</span><span class="sxs-lookup"><span data-stu-id="00d1c-130">x</span></span>      | <span data-ttu-id="00d1c-131">x</span><span class="sxs-lookup"><span data-stu-id="00d1c-131">x</span></span>    | <span data-ttu-id="00d1c-132">x</span><span class="sxs-lookup"><span data-stu-id="00d1c-132">x</span></span>      | <span data-ttu-id="00d1c-133">x</span><span class="sxs-lookup"><span data-stu-id="00d1c-133">x</span></span>        | <span data-ttu-id="00d1c-134">x</span><span class="sxs-lookup"><span data-stu-id="00d1c-134">x</span></span>     | <span data-ttu-id="00d1c-135">x</span><span class="sxs-lookup"><span data-stu-id="00d1c-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="00d1c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="00d1c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d1c-137">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="00d1c-137">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="00d1c-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="00d1c-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




