---
title: 'Função Texture2D:: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2D:: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: E7EB3D17-3110-4167-B255-C451BA4EFB27
keywords:
- HLSL da função GatherCmpGreen
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b490fd47bd9346c4f514867de63df7a4d090e5b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172778"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="e9034-105">Função Texture2D:: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint)</span><span class="sxs-lookup"><span data-stu-id="e9034-105">Texture2D::GatherCmpGreen(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="e9034-106">Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="e9034-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9034-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9034-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e9034-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9034-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e9034-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="e9034-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e9034-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="e9034-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e9034-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e9034-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e9034-113">Type: **float**</span></span>

<span data-ttu-id="e9034-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="e9034-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e9034-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9034-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e9034-116">Type: **float**</span></span>

<span data-ttu-id="e9034-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="e9034-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="e9034-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9034-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="e9034-119">Type: **int2**</span></span>

<span data-ttu-id="e9034-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e9034-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e9034-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9034-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="e9034-122">Type: **int2**</span></span>

<span data-ttu-id="e9034-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e9034-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e9034-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9034-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="e9034-125">Type: **int2**</span></span>

<span data-ttu-id="e9034-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e9034-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e9034-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9034-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="e9034-128">Type: **int2**</span></span>

<span data-ttu-id="e9034-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="e9034-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e9034-130">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e9034-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9034-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e9034-131">Type: **uint**</span></span>

<span data-ttu-id="e9034-132">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="e9034-132">The status of the operation.</span></span> <span data-ttu-id="e9034-133">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e9034-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e9034-134">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e9034-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e9034-135">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="e9034-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9034-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9034-136">Return value</span></span>

<span data-ttu-id="e9034-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="e9034-137">Type: **TemplateType**</span></span>

<span data-ttu-id="e9034-138">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9034-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9034-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9034-139">Remarks</span></span>

<span data-ttu-id="e9034-140">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="e9034-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e9034-141">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e9034-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e9034-142">Vértice</span><span class="sxs-lookup"><span data-stu-id="e9034-142">Vertex</span></span> | <span data-ttu-id="e9034-143">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e9034-143">Hull</span></span> | <span data-ttu-id="e9034-144">Domínio</span><span class="sxs-lookup"><span data-stu-id="e9034-144">Domain</span></span> | <span data-ttu-id="e9034-145">Geometria</span><span class="sxs-lookup"><span data-stu-id="e9034-145">Geometry</span></span> | <span data-ttu-id="e9034-146">16x16</span><span class="sxs-lookup"><span data-stu-id="e9034-146">Pixel</span></span> | <span data-ttu-id="e9034-147">Computação</span><span class="sxs-lookup"><span data-stu-id="e9034-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e9034-148">x</span><span class="sxs-lookup"><span data-stu-id="e9034-148">x</span></span>      | <span data-ttu-id="e9034-149">x</span><span class="sxs-lookup"><span data-stu-id="e9034-149">x</span></span>    | <span data-ttu-id="e9034-150">x</span><span class="sxs-lookup"><span data-stu-id="e9034-150">x</span></span>      | <span data-ttu-id="e9034-151">x</span><span class="sxs-lookup"><span data-stu-id="e9034-151">x</span></span>        | <span data-ttu-id="e9034-152">x</span><span class="sxs-lookup"><span data-stu-id="e9034-152">x</span></span>     | <span data-ttu-id="e9034-153">x</span><span class="sxs-lookup"><span data-stu-id="e9034-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e9034-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9034-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9034-155">Métodos GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="e9034-155">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 
