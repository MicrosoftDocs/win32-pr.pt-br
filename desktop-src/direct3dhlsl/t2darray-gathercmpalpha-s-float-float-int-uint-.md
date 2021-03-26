---
title: 'Função Texture2DArray:: GatherCmpAlpha (S, float, float, int, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2DArray:: GatherCmpAlpha (S, float, float, int, uint)'
ms.assetid: DCCF7F40-8A0D-47B8-910A-508382D3AE3F
keywords:
- HLSL da função GatherCmpAlpha
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: afd427c5af46f333deb0b05de551f8081d9bd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298179"
---
# <a name="texture2darraygathercmpalphasfloatfloatintuint-function"></a><span data-ttu-id="febea-105">Função Texture2DArray:: GatherCmpAlpha (S, float, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="febea-105">Texture2DArray::GatherCmpAlpha(S,float,float,int,uint) function</span></span>

<span data-ttu-id="febea-106">Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="febea-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="febea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="febea-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="febea-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="febea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="febea-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="febea-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="febea-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="febea-110">Type: **SamplerState**</span></span>

<span data-ttu-id="febea-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="febea-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="febea-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="febea-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="febea-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="febea-113">Type: **float**</span></span>

<span data-ttu-id="febea-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="febea-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="febea-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="febea-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="febea-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="febea-116">Type: **float**</span></span>

<span data-ttu-id="febea-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="febea-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="febea-118">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="febea-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="febea-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="febea-119">Type: **int**</span></span>

<span data-ttu-id="febea-120">O deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="febea-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="febea-121">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="febea-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="febea-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="febea-122">Type: **uint**</span></span>

<span data-ttu-id="febea-123">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="febea-123">The status of the operation.</span></span> <span data-ttu-id="febea-124">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="febea-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="febea-125">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="febea-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="febea-126">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="febea-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="febea-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="febea-127">Return value</span></span>

<span data-ttu-id="febea-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="febea-128">Type: **TemplateType**</span></span>

<span data-ttu-id="febea-129">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="febea-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="febea-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="febea-130">Remarks</span></span>

<span data-ttu-id="febea-131">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="febea-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="febea-132">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="febea-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="febea-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="febea-133">Vertex</span></span> | <span data-ttu-id="febea-134">Envoltória</span><span class="sxs-lookup"><span data-stu-id="febea-134">Hull</span></span> | <span data-ttu-id="febea-135">Domínio</span><span class="sxs-lookup"><span data-stu-id="febea-135">Domain</span></span> | <span data-ttu-id="febea-136">Geometria</span><span class="sxs-lookup"><span data-stu-id="febea-136">Geometry</span></span> | <span data-ttu-id="febea-137">16x16</span><span class="sxs-lookup"><span data-stu-id="febea-137">Pixel</span></span> | <span data-ttu-id="febea-138">Computação</span><span class="sxs-lookup"><span data-stu-id="febea-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="febea-139">x</span><span class="sxs-lookup"><span data-stu-id="febea-139">x</span></span>      | <span data-ttu-id="febea-140">x</span><span class="sxs-lookup"><span data-stu-id="febea-140">x</span></span>    | <span data-ttu-id="febea-141">x</span><span class="sxs-lookup"><span data-stu-id="febea-141">x</span></span>      | <span data-ttu-id="febea-142">x</span><span class="sxs-lookup"><span data-stu-id="febea-142">x</span></span>        | <span data-ttu-id="febea-143">x</span><span class="sxs-lookup"><span data-stu-id="febea-143">x</span></span>     | <span data-ttu-id="febea-144">x</span><span class="sxs-lookup"><span data-stu-id="febea-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="febea-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="febea-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="febea-146">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="febea-146">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> </dl>

 

 
