---
title: 'Função Texture2DArray:: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2DArray:: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: 53AC1FE7-ECC8-489B-8FEF-5028009BC080
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
ms.openlocfilehash: 9878e5e9474717be9842887b2945591d5883cb07
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968508"
---
# <a name="texture2darraygathercmpgreensfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="1a03f-105">Função Texture2DArray:: GatherCmpGreen (S, float, float, Int2, Int2, Int2, Int2, uint)</span><span class="sxs-lookup"><span data-stu-id="1a03f-105">Texture2DArray::GatherCmpGreen(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="1a03f-106">Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="1a03f-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a03f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a03f-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1a03f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a03f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a03f-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="1a03f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1a03f-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="1a03f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1a03f-113">Type: **float**</span></span>

<span data-ttu-id="1a03f-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="1a03f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1a03f-116">Type: **float**</span></span>

<span data-ttu-id="1a03f-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="1a03f-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1a03f-119">Type: **int2**</span></span>

<span data-ttu-id="1a03f-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1a03f-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1a03f-122">Type: **int2**</span></span>

<span data-ttu-id="1a03f-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1a03f-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1a03f-125">Type: **int2**</span></span>

<span data-ttu-id="1a03f-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1a03f-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="1a03f-128">Type: **int2**</span></span>

<span data-ttu-id="1a03f-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="1a03f-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1a03f-130">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="1a03f-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a03f-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1a03f-131">Type: **uint**</span></span>

<span data-ttu-id="1a03f-132">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="1a03f-132">The status of the operation.</span></span> <span data-ttu-id="1a03f-133">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1a03f-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1a03f-134">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1a03f-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1a03f-135">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="1a03f-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a03f-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a03f-136">Return value</span></span>

<span data-ttu-id="1a03f-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1a03f-137">Type: **TemplateType**</span></span>

<span data-ttu-id="1a03f-138">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="1a03f-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a03f-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a03f-139">Remarks</span></span>

<span data-ttu-id="1a03f-140">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="1a03f-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1a03f-141">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1a03f-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1a03f-142">Vértice</span><span class="sxs-lookup"><span data-stu-id="1a03f-142">Vertex</span></span> | <span data-ttu-id="1a03f-143">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1a03f-143">Hull</span></span> | <span data-ttu-id="1a03f-144">Domínio</span><span class="sxs-lookup"><span data-stu-id="1a03f-144">Domain</span></span> | <span data-ttu-id="1a03f-145">Geometria</span><span class="sxs-lookup"><span data-stu-id="1a03f-145">Geometry</span></span> | <span data-ttu-id="1a03f-146">16x16</span><span class="sxs-lookup"><span data-stu-id="1a03f-146">Pixel</span></span> | <span data-ttu-id="1a03f-147">Computação</span><span class="sxs-lookup"><span data-stu-id="1a03f-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1a03f-148">x</span><span class="sxs-lookup"><span data-stu-id="1a03f-148">x</span></span>      | <span data-ttu-id="1a03f-149">x</span><span class="sxs-lookup"><span data-stu-id="1a03f-149">x</span></span>    | <span data-ttu-id="1a03f-150">x</span><span class="sxs-lookup"><span data-stu-id="1a03f-150">x</span></span>      | <span data-ttu-id="1a03f-151">x</span><span class="sxs-lookup"><span data-stu-id="1a03f-151">x</span></span>        | <span data-ttu-id="1a03f-152">x</span><span class="sxs-lookup"><span data-stu-id="1a03f-152">x</span></span>     | <span data-ttu-id="1a03f-153">x</span><span class="sxs-lookup"><span data-stu-id="1a03f-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1a03f-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a03f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a03f-155">Métodos GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="1a03f-155">GatherCmpGreen methods</span></span>](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 
