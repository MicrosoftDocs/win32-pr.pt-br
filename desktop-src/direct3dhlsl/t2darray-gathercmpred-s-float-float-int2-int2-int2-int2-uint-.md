---
title: 'Função Texture2DArray:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2DArray:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: E41E1328-AE31-445E-AF01-1DB201E8A278
keywords:
- HLSL da função GatherCmpRed
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12c6e3762ed4152d1e75bcb93c67663f92e923b1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968507"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="c5917-105">Função Texture2DArray:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint)</span><span class="sxs-lookup"><span data-stu-id="c5917-105">Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="c5917-106">Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="c5917-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5917-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5917-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
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



## <a name="parameters"></a><span data-ttu-id="c5917-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5917-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5917-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c5917-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="c5917-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c5917-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="c5917-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c5917-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c5917-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c5917-113">Type: **float**</span></span>

<span data-ttu-id="c5917-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="c5917-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c5917-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5917-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c5917-116">Type: **float**</span></span>

<span data-ttu-id="c5917-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="c5917-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="c5917-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5917-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c5917-119">Type: **int2**</span></span>

<span data-ttu-id="c5917-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c5917-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c5917-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5917-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c5917-122">Type: **int2**</span></span>

<span data-ttu-id="c5917-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c5917-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c5917-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5917-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c5917-125">Type: **int2**</span></span>

<span data-ttu-id="c5917-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c5917-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c5917-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5917-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="c5917-128">Type: **int2**</span></span>

<span data-ttu-id="c5917-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="c5917-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c5917-130">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c5917-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5917-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c5917-131">Type: **uint**</span></span>

<span data-ttu-id="c5917-132">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="c5917-132">The status of the operation.</span></span> <span data-ttu-id="c5917-133">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c5917-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c5917-134">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c5917-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c5917-135">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c5917-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5917-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5917-136">Return value</span></span>

<span data-ttu-id="c5917-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c5917-137">Type: **TemplateType**</span></span>

<span data-ttu-id="c5917-138">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="c5917-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5917-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5917-139">Remarks</span></span>

<span data-ttu-id="c5917-140">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="c5917-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c5917-141">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c5917-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c5917-142">Vértice</span><span class="sxs-lookup"><span data-stu-id="c5917-142">Vertex</span></span> | <span data-ttu-id="c5917-143">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c5917-143">Hull</span></span> | <span data-ttu-id="c5917-144">Domínio</span><span class="sxs-lookup"><span data-stu-id="c5917-144">Domain</span></span> | <span data-ttu-id="c5917-145">Geometria</span><span class="sxs-lookup"><span data-stu-id="c5917-145">Geometry</span></span> | <span data-ttu-id="c5917-146">16x16</span><span class="sxs-lookup"><span data-stu-id="c5917-146">Pixel</span></span> | <span data-ttu-id="c5917-147">Computação</span><span class="sxs-lookup"><span data-stu-id="c5917-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c5917-148">x</span><span class="sxs-lookup"><span data-stu-id="c5917-148">x</span></span>      | <span data-ttu-id="c5917-149">x</span><span class="sxs-lookup"><span data-stu-id="c5917-149">x</span></span>    | <span data-ttu-id="c5917-150">x</span><span class="sxs-lookup"><span data-stu-id="c5917-150">x</span></span>      | <span data-ttu-id="c5917-151">x</span><span class="sxs-lookup"><span data-stu-id="c5917-151">x</span></span>        | <span data-ttu-id="c5917-152">x</span><span class="sxs-lookup"><span data-stu-id="c5917-152">x</span></span>     | <span data-ttu-id="c5917-153">x</span><span class="sxs-lookup"><span data-stu-id="c5917-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c5917-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5917-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5917-155">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="c5917-155">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
