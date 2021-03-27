---
title: 'Função Texture2D:: GatherBlue (S, float, Int2, Int2, Int2, Int2, uint)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função Texture2D:: GatherBlue (S, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: 74B2DAEC-3A94-441D-8A9E-286C2D2E9C8E
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
ms.openlocfilehash: 60df5e94c348af95b81efc8f1b913ac6f7875a79
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298355"
---
# <a name="texture2dgatherbluesfloatint2int2int2int2uint-function"></a><span data-ttu-id="23767-105">Função Texture2D:: GatherBlue (S, float, Int2, Int2, Int2, Int2, uint)</span><span class="sxs-lookup"><span data-stu-id="23767-105">Texture2D::GatherBlue(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="23767-106">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="23767-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="23767-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23767-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="23767-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23767-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23767-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="23767-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="23767-110">Type: **SamplerState**</span></span>

<span data-ttu-id="23767-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="23767-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="23767-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="23767-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="23767-113">Type: **float**</span></span>

<span data-ttu-id="23767-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="23767-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="23767-115">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23767-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="23767-116">Type: **int2**</span></span>

<span data-ttu-id="23767-117">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="23767-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23767-118">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23767-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="23767-119">Type: **int2**</span></span>

<span data-ttu-id="23767-120">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="23767-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23767-121">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23767-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="23767-122">Type: **int2**</span></span>

<span data-ttu-id="23767-123">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="23767-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23767-124">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23767-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="23767-125">Type: **int2**</span></span>

<span data-ttu-id="23767-126">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="23767-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23767-127">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="23767-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23767-128">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="23767-128">Type: **uint**</span></span>

<span data-ttu-id="23767-129">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="23767-129">The status of the operation.</span></span> <span data-ttu-id="23767-130">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="23767-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="23767-131">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="23767-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="23767-132">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="23767-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23767-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23767-133">Return value</span></span>

<span data-ttu-id="23767-134">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="23767-134">Type: **TemplateType**</span></span>

<span data-ttu-id="23767-135">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="23767-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="23767-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="23767-136">Remarks</span></span>

<span data-ttu-id="23767-137">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="23767-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="23767-138">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="23767-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="23767-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="23767-139">Vertex</span></span> | <span data-ttu-id="23767-140">Envoltória</span><span class="sxs-lookup"><span data-stu-id="23767-140">Hull</span></span> | <span data-ttu-id="23767-141">Domínio</span><span class="sxs-lookup"><span data-stu-id="23767-141">Domain</span></span> | <span data-ttu-id="23767-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="23767-142">Geometry</span></span> | <span data-ttu-id="23767-143">16x16</span><span class="sxs-lookup"><span data-stu-id="23767-143">Pixel</span></span> | <span data-ttu-id="23767-144">Computação</span><span class="sxs-lookup"><span data-stu-id="23767-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="23767-145">x</span><span class="sxs-lookup"><span data-stu-id="23767-145">x</span></span>      | <span data-ttu-id="23767-146">x</span><span class="sxs-lookup"><span data-stu-id="23767-146">x</span></span>    | <span data-ttu-id="23767-147">x</span><span class="sxs-lookup"><span data-stu-id="23767-147">x</span></span>      | <span data-ttu-id="23767-148">x</span><span class="sxs-lookup"><span data-stu-id="23767-148">x</span></span>        | <span data-ttu-id="23767-149">x</span><span class="sxs-lookup"><span data-stu-id="23767-149">x</span></span>     | <span data-ttu-id="23767-150">x</span><span class="sxs-lookup"><span data-stu-id="23767-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="23767-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="23767-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23767-152">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="23767-152">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> </dl>

 

 
