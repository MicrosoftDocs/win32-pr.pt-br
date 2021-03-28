---
title: 'Função Texture2D:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função Texture2D:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: 69B1F8FF-CE29-49DD-B756-3308E11D866D
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
ms.openlocfilehash: 2d872623d7dcc8ea599e3c790493f2e1a8596b91
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989158"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="71526-105">Função Texture2D:: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint)</span><span class="sxs-lookup"><span data-stu-id="71526-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="71526-106">Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="71526-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="71526-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71526-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="71526-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71526-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71526-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="71526-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="71526-110">Type: **SamplerState**</span></span>

<span data-ttu-id="71526-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="71526-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="71526-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="71526-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="71526-113">Type: **float**</span></span>

<span data-ttu-id="71526-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="71526-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="71526-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71526-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="71526-116">Type: **float**</span></span>

<span data-ttu-id="71526-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="71526-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="71526-118">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71526-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="71526-119">Type: **int2**</span></span>

<span data-ttu-id="71526-120">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="71526-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="71526-121">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71526-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="71526-122">Type: **int2**</span></span>

<span data-ttu-id="71526-123">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="71526-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="71526-124">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71526-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="71526-125">Type: **int2**</span></span>

<span data-ttu-id="71526-126">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="71526-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="71526-127">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71526-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-128">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="71526-128">Type: **int2**</span></span>

<span data-ttu-id="71526-129">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="71526-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="71526-130">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="71526-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71526-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="71526-131">Type: **uint**</span></span>

<span data-ttu-id="71526-132">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="71526-132">The status of the operation.</span></span> <span data-ttu-id="71526-133">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="71526-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="71526-134">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="71526-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="71526-135">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="71526-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71526-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71526-136">Return value</span></span>

<span data-ttu-id="71526-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="71526-137">Type: **TemplateType**</span></span>

<span data-ttu-id="71526-138">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="71526-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="71526-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="71526-139">Remarks</span></span>

<span data-ttu-id="71526-140">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="71526-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="71526-141">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="71526-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="71526-142">Vértice</span><span class="sxs-lookup"><span data-stu-id="71526-142">Vertex</span></span> | <span data-ttu-id="71526-143">Envoltória</span><span class="sxs-lookup"><span data-stu-id="71526-143">Hull</span></span> | <span data-ttu-id="71526-144">Domínio</span><span class="sxs-lookup"><span data-stu-id="71526-144">Domain</span></span> | <span data-ttu-id="71526-145">Geometria</span><span class="sxs-lookup"><span data-stu-id="71526-145">Geometry</span></span> | <span data-ttu-id="71526-146">16x16</span><span class="sxs-lookup"><span data-stu-id="71526-146">Pixel</span></span> | <span data-ttu-id="71526-147">Computação</span><span class="sxs-lookup"><span data-stu-id="71526-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="71526-148">x</span><span class="sxs-lookup"><span data-stu-id="71526-148">x</span></span>      | <span data-ttu-id="71526-149">x</span><span class="sxs-lookup"><span data-stu-id="71526-149">x</span></span>    | <span data-ttu-id="71526-150">x</span><span class="sxs-lookup"><span data-stu-id="71526-150">x</span></span>      | <span data-ttu-id="71526-151">x</span><span class="sxs-lookup"><span data-stu-id="71526-151">x</span></span>        | <span data-ttu-id="71526-152">x</span><span class="sxs-lookup"><span data-stu-id="71526-152">x</span></span>     | <span data-ttu-id="71526-153">x</span><span class="sxs-lookup"><span data-stu-id="71526-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71526-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="71526-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71526-155">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="71526-155">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 
