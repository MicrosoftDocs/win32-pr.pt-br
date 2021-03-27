---
title: 'Função Texture2DArray:: GatherBlue (S, float, int)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: GatherBlue (S, float, int)'
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
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
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989165"
---
# <a name="texture2darraygatherbluesfloatint-function"></a><span data-ttu-id="2cbb8-105">Função Texture2DArray:: GatherBlue (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="2cbb8-105">Texture2DArray::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="2cbb8-106">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbb8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cbb8-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="2cbb8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cbb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbb8-109">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2cbb8-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbb8-110">Tipo: **amostra**</span><span class="sxs-lookup"><span data-stu-id="2cbb8-110">Type: **sampler**</span></span>

<span data-ttu-id="2cbb8-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2cbb8-112">*local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2cbb8-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbb8-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="2cbb8-113">Type: **float3**</span></span>

<span data-ttu-id="2cbb8-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="2cbb8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2cbb8-115">*deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cbb8-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbb8-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="2cbb8-116">Type: **int2**</span></span>

<span data-ttu-id="2cbb8-117">Um deslocamento que é aplicado à coordenada de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbb8-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cbb8-118">Return value</span></span>

<span data-ttu-id="2cbb8-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2cbb8-119">Type: **TemplateType**</span></span>

<span data-ttu-id="2cbb8-120">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbb8-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cbb8-121">Remarks</span></span>

<span data-ttu-id="2cbb8-122">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="2cbb8-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2cbb8-123">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2cbb8-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2cbb8-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="2cbb8-124">Vertex</span></span> | <span data-ttu-id="2cbb8-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2cbb8-125">Hull</span></span> | <span data-ttu-id="2cbb8-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="2cbb8-126">Domain</span></span> | <span data-ttu-id="2cbb8-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="2cbb8-127">Geometry</span></span> | <span data-ttu-id="2cbb8-128">16x16</span><span class="sxs-lookup"><span data-stu-id="2cbb8-128">Pixel</span></span> | <span data-ttu-id="2cbb8-129">Computação</span><span class="sxs-lookup"><span data-stu-id="2cbb8-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2cbb8-130">x</span><span class="sxs-lookup"><span data-stu-id="2cbb8-130">x</span></span>      | <span data-ttu-id="2cbb8-131">x</span><span class="sxs-lookup"><span data-stu-id="2cbb8-131">x</span></span>    | <span data-ttu-id="2cbb8-132">x</span><span class="sxs-lookup"><span data-stu-id="2cbb8-132">x</span></span>      | <span data-ttu-id="2cbb8-133">x</span><span class="sxs-lookup"><span data-stu-id="2cbb8-133">x</span></span>        | <span data-ttu-id="2cbb8-134">x</span><span class="sxs-lookup"><span data-stu-id="2cbb8-134">x</span></span>     | <span data-ttu-id="2cbb8-135">x</span><span class="sxs-lookup"><span data-stu-id="2cbb8-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2cbb8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cbb8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbb8-137">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="2cbb8-137">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="2cbb8-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2cbb8-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




