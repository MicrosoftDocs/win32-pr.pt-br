---
title: 'Função Texture2D:: gather (S, float, int)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2D:: gather (S, float, int)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
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
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663909"
---
# <a name="texture2dgathersfloatint-function"></a><span data-ttu-id="56e9f-105">Função Texture2D:: gather (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="56e9f-105">Texture2D::Gather(S,float,int) function</span></span>

<span data-ttu-id="56e9f-106">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="56e9f-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e9f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56e9f-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="56e9f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56e9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e9f-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="56e9f-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e9f-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="56e9f-110">Type: **sampler**</span></span>

<span data-ttu-id="56e9f-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="56e9f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="56e9f-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="56e9f-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e9f-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="56e9f-113">Type: **float2**</span></span>

<span data-ttu-id="56e9f-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="56e9f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="56e9f-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56e9f-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e9f-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="56e9f-116">Type: **int2**</span></span>

<span data-ttu-id="56e9f-117">O deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="56e9f-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e9f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56e9f-118">Return value</span></span>

<span data-ttu-id="56e9f-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="56e9f-119">Type: **TemplateType**</span></span>

<span data-ttu-id="56e9f-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="56e9f-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e9f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="56e9f-121">Remarks</span></span>

<span data-ttu-id="56e9f-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="56e9f-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="56e9f-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="56e9f-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="56e9f-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="56e9f-124">Vertex</span></span> | <span data-ttu-id="56e9f-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="56e9f-125">Hull</span></span> | <span data-ttu-id="56e9f-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="56e9f-126">Domain</span></span> | <span data-ttu-id="56e9f-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="56e9f-127">Geometry</span></span> | <span data-ttu-id="56e9f-128">16x16</span><span class="sxs-lookup"><span data-stu-id="56e9f-128">Pixel</span></span> | <span data-ttu-id="56e9f-129">Computação</span><span class="sxs-lookup"><span data-stu-id="56e9f-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="56e9f-130">x</span><span class="sxs-lookup"><span data-stu-id="56e9f-130">x</span></span>      | <span data-ttu-id="56e9f-131">x</span><span class="sxs-lookup"><span data-stu-id="56e9f-131">x</span></span>    | <span data-ttu-id="56e9f-132">x</span><span class="sxs-lookup"><span data-stu-id="56e9f-132">x</span></span>      | <span data-ttu-id="56e9f-133">x</span><span class="sxs-lookup"><span data-stu-id="56e9f-133">x</span></span>        | <span data-ttu-id="56e9f-134">x</span><span class="sxs-lookup"><span data-stu-id="56e9f-134">x</span></span>     | <span data-ttu-id="56e9f-135">x</span><span class="sxs-lookup"><span data-stu-id="56e9f-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56e9f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="56e9f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e9f-137">Reunir métodos</span><span class="sxs-lookup"><span data-stu-id="56e9f-137">Gather methods</span></span>](texture2d-gather.md)
</dt> <dt>

[<span data-ttu-id="56e9f-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="56e9f-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




