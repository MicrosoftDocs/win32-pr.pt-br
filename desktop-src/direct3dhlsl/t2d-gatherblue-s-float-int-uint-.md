---
title: 'Função Texture2D:: GatherBlue (S, float, int, uint)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função Texture2D:: GatherBlue (S, float, int, uint)'
ms.assetid: 9E2A57C3-4EC4-4414-B16A-64AF759F04E9
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
ms.openlocfilehash: 68eb7676cdb74eaff1087baa7879d41d098b4ace
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968482"
---
# <a name="texture2dgatherbluesfloatintuint-function"></a><span data-ttu-id="7df5b-105">Função Texture2D:: GatherBlue (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="7df5b-105">Texture2D::GatherBlue(S,float,int,uint) function</span></span>

<span data-ttu-id="7df5b-106">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="7df5b-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df5b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7df5b-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7df5b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7df5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df5b-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="7df5b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df5b-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="7df5b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="7df5b-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="7df5b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7df5b-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7df5b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df5b-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7df5b-113">Type: **float**</span></span>

<span data-ttu-id="7df5b-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="7df5b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7df5b-115">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7df5b-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7df5b-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7df5b-116">Type: **int**</span></span>

<span data-ttu-id="7df5b-117">O deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="7df5b-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7df5b-118">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7df5b-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7df5b-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7df5b-119">Type: **uint**</span></span>

<span data-ttu-id="7df5b-120">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="7df5b-120">The status of the operation.</span></span> <span data-ttu-id="7df5b-121">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7df5b-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7df5b-122">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7df5b-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7df5b-123">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="7df5b-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df5b-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7df5b-124">Return value</span></span>

<span data-ttu-id="7df5b-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="7df5b-125">Type: **TemplateType**</span></span>

<span data-ttu-id="7df5b-126">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="7df5b-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df5b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7df5b-127">Remarks</span></span>

<span data-ttu-id="7df5b-128">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="7df5b-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7df5b-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7df5b-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7df5b-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="7df5b-130">Vertex</span></span> | <span data-ttu-id="7df5b-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="7df5b-131">Hull</span></span> | <span data-ttu-id="7df5b-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="7df5b-132">Domain</span></span> | <span data-ttu-id="7df5b-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="7df5b-133">Geometry</span></span> | <span data-ttu-id="7df5b-134">16x16</span><span class="sxs-lookup"><span data-stu-id="7df5b-134">Pixel</span></span> | <span data-ttu-id="7df5b-135">Computação</span><span class="sxs-lookup"><span data-stu-id="7df5b-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7df5b-136">x</span><span class="sxs-lookup"><span data-stu-id="7df5b-136">x</span></span>      | <span data-ttu-id="7df5b-137">x</span><span class="sxs-lookup"><span data-stu-id="7df5b-137">x</span></span>    | <span data-ttu-id="7df5b-138">x</span><span class="sxs-lookup"><span data-stu-id="7df5b-138">x</span></span>      | <span data-ttu-id="7df5b-139">x</span><span class="sxs-lookup"><span data-stu-id="7df5b-139">x</span></span>        | <span data-ttu-id="7df5b-140">x</span><span class="sxs-lookup"><span data-stu-id="7df5b-140">x</span></span>     | <span data-ttu-id="7df5b-141">x</span><span class="sxs-lookup"><span data-stu-id="7df5b-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7df5b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df5b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df5b-143">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="7df5b-143">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> </dl>

 

 
