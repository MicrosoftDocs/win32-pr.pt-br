---
title: 'Função Texture2D:: GatherCmp (S, float, float, int, uint)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2D:: GatherCmp (S, float, float, int, uint)'
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- HLSL da função GatherCmp
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968480"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="c32a6-105">Função Texture2D:: GatherCmp (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="c32a6-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="c32a6-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="c32a6-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c32a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c32a6-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c32a6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c32a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32a6-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c32a6-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32a6-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="c32a6-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c32a6-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="c32a6-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c32a6-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c32a6-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32a6-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c32a6-113">Type: **float**</span></span>

<span data-ttu-id="c32a6-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="c32a6-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c32a6-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c32a6-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32a6-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c32a6-116">Type: **float**</span></span>

<span data-ttu-id="c32a6-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="c32a6-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="c32a6-118">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c32a6-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32a6-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c32a6-119">Type: **int2**</span></span>

<span data-ttu-id="c32a6-120">O deslocamento em texels aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c32a6-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="c32a6-121">Deve ser um valor literal.</span><span class="sxs-lookup"><span data-stu-id="c32a6-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="c32a6-122">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c32a6-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c32a6-123">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c32a6-123">Type: **uint**</span></span>

<span data-ttu-id="c32a6-124">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="c32a6-124">The status of the operation.</span></span> <span data-ttu-id="c32a6-125">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c32a6-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c32a6-126">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c32a6-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c32a6-127">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c32a6-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32a6-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c32a6-128">Return value</span></span>

<span data-ttu-id="c32a6-129">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c32a6-129">Type: **TemplateType**</span></span>

<span data-ttu-id="c32a6-130">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="c32a6-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32a6-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="c32a6-131">Remarks</span></span>

<span data-ttu-id="c32a6-132">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="c32a6-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c32a6-133">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c32a6-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c32a6-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="c32a6-134">Vertex</span></span> | <span data-ttu-id="c32a6-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c32a6-135">Hull</span></span> | <span data-ttu-id="c32a6-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="c32a6-136">Domain</span></span> | <span data-ttu-id="c32a6-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="c32a6-137">Geometry</span></span> | <span data-ttu-id="c32a6-138">16x16</span><span class="sxs-lookup"><span data-stu-id="c32a6-138">Pixel</span></span> | <span data-ttu-id="c32a6-139">Computação</span><span class="sxs-lookup"><span data-stu-id="c32a6-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c32a6-140">x</span><span class="sxs-lookup"><span data-stu-id="c32a6-140">x</span></span>      | <span data-ttu-id="c32a6-141">x</span><span class="sxs-lookup"><span data-stu-id="c32a6-141">x</span></span>    | <span data-ttu-id="c32a6-142">x</span><span class="sxs-lookup"><span data-stu-id="c32a6-142">x</span></span>      | <span data-ttu-id="c32a6-143">x</span><span class="sxs-lookup"><span data-stu-id="c32a6-143">x</span></span>        | <span data-ttu-id="c32a6-144">x</span><span class="sxs-lookup"><span data-stu-id="c32a6-144">x</span></span>     | <span data-ttu-id="c32a6-145">x</span><span class="sxs-lookup"><span data-stu-id="c32a6-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c32a6-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c32a6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32a6-147">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="c32a6-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
