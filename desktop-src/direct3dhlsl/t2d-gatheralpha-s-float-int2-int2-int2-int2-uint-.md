---
title: 'Função Texture2D:: GatherAlpha (S, float, Int2, Int2, Int2, Int2, uint)'
description: 'Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função Texture2D:: GatherAlpha (S, float, Int2, Int2, Int2, Int2, uint)'
ms.assetid: C088BC6A-397C-4702-9BFA-0B2F10C833BD
keywords:
- HLSL da função GatherAlpha
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fddf9ebc8358bfc911f05d1f6e0cb34e8cfb5da
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298356"
---
# <a name="texture2dgatheralphasfloatint2int2int2int2uint-function"></a><span data-ttu-id="33834-105">Função Texture2D:: GatherAlpha (S, float, Int2, Int2, Int2, Int2, uint)</span><span class="sxs-lookup"><span data-stu-id="33834-105">Texture2D::GatherAlpha(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="33834-106">Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="33834-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="33834-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33834-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="33834-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33834-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33834-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="33834-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="33834-110">Type: **SamplerState**</span></span>

<span data-ttu-id="33834-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="33834-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="33834-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="33834-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="33834-113">Type: **float**</span></span>

<span data-ttu-id="33834-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="33834-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="33834-115">*Offset1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33834-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-116">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="33834-116">Type: **int2**</span></span>

<span data-ttu-id="33834-117">O primeiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="33834-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="33834-118">*Offset2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33834-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-119">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="33834-119">Type: **int2**</span></span>

<span data-ttu-id="33834-120">O segundo componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="33834-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="33834-121">*Offset3* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33834-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-122">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="33834-122">Type: **int2**</span></span>

<span data-ttu-id="33834-123">O terceiro componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="33834-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="33834-124">*Offset4* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33834-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-125">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="33834-125">Type: **int2**</span></span>

<span data-ttu-id="33834-126">O quarto componente de deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="33834-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="33834-127">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="33834-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33834-128">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="33834-128">Type: **uint**</span></span>

<span data-ttu-id="33834-129">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="33834-129">The status of the operation.</span></span> <span data-ttu-id="33834-130">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="33834-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="33834-131">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="33834-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="33834-132">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="33834-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33834-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33834-133">Return value</span></span>

<span data-ttu-id="33834-134">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="33834-134">Type: **TemplateType**</span></span>

<span data-ttu-id="33834-135">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="33834-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="33834-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="33834-136">Remarks</span></span>

<span data-ttu-id="33834-137">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="33834-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="33834-138">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="33834-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="33834-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="33834-139">Vertex</span></span> | <span data-ttu-id="33834-140">Envoltória</span><span class="sxs-lookup"><span data-stu-id="33834-140">Hull</span></span> | <span data-ttu-id="33834-141">Domínio</span><span class="sxs-lookup"><span data-stu-id="33834-141">Domain</span></span> | <span data-ttu-id="33834-142">Geometria</span><span class="sxs-lookup"><span data-stu-id="33834-142">Geometry</span></span> | <span data-ttu-id="33834-143">16x16</span><span class="sxs-lookup"><span data-stu-id="33834-143">Pixel</span></span> | <span data-ttu-id="33834-144">Computação</span><span class="sxs-lookup"><span data-stu-id="33834-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="33834-145">x</span><span class="sxs-lookup"><span data-stu-id="33834-145">x</span></span>      | <span data-ttu-id="33834-146">x</span><span class="sxs-lookup"><span data-stu-id="33834-146">x</span></span>    | <span data-ttu-id="33834-147">x</span><span class="sxs-lookup"><span data-stu-id="33834-147">x</span></span>      | <span data-ttu-id="33834-148">x</span><span class="sxs-lookup"><span data-stu-id="33834-148">x</span></span>        | <span data-ttu-id="33834-149">x</span><span class="sxs-lookup"><span data-stu-id="33834-149">x</span></span>     | <span data-ttu-id="33834-150">x</span><span class="sxs-lookup"><span data-stu-id="33834-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="33834-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="33834-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33834-152">Métodos GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="33834-152">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> </dl>

 

 
