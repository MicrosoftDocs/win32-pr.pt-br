---
title: 'Função Texture2DArray:: GatherRed (S, float, int, uint)'
description: 'Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função Texture2DArray:: GatherRed (S, float, int, uint)'
ms.assetid: 9FAFB594-5844-4A2D-9B45-7973B5F85E13
keywords:
- HLSL da função GatherRed
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fdd250cb25f6085100bb88204cae6e67a3fc0b3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663929"
---
# <a name="texture2darraygatherredsfloatintuint-function"></a><span data-ttu-id="85254-105">Função Texture2DArray:: GatherRed (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="85254-105">Texture2DArray::GatherRed(S,float,int,uint) function</span></span>

<span data-ttu-id="85254-106">Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="85254-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="85254-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85254-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="85254-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85254-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85254-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="85254-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85254-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="85254-110">Type: **SamplerState**</span></span>

<span data-ttu-id="85254-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="85254-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="85254-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="85254-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85254-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="85254-113">Type: **float**</span></span>

<span data-ttu-id="85254-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="85254-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="85254-115">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85254-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85254-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="85254-116">Type: **int**</span></span>

<span data-ttu-id="85254-117">O deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="85254-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="85254-118">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="85254-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85254-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="85254-119">Type: **uint**</span></span>

<span data-ttu-id="85254-120">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="85254-120">The status of the operation.</span></span> <span data-ttu-id="85254-121">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="85254-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="85254-122">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="85254-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="85254-123">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="85254-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85254-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85254-124">Return value</span></span>

<span data-ttu-id="85254-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="85254-125">Type: **TemplateType**</span></span>

<span data-ttu-id="85254-126">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="85254-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="85254-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="85254-127">Remarks</span></span>

<span data-ttu-id="85254-128">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="85254-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="85254-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="85254-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="85254-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="85254-130">Vertex</span></span> | <span data-ttu-id="85254-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="85254-131">Hull</span></span> | <span data-ttu-id="85254-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="85254-132">Domain</span></span> | <span data-ttu-id="85254-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="85254-133">Geometry</span></span> | <span data-ttu-id="85254-134">16x16</span><span class="sxs-lookup"><span data-stu-id="85254-134">Pixel</span></span> | <span data-ttu-id="85254-135">Computação</span><span class="sxs-lookup"><span data-stu-id="85254-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="85254-136">x</span><span class="sxs-lookup"><span data-stu-id="85254-136">x</span></span>      | <span data-ttu-id="85254-137">x</span><span class="sxs-lookup"><span data-stu-id="85254-137">x</span></span>    | <span data-ttu-id="85254-138">x</span><span class="sxs-lookup"><span data-stu-id="85254-138">x</span></span>      | <span data-ttu-id="85254-139">x</span><span class="sxs-lookup"><span data-stu-id="85254-139">x</span></span>        | <span data-ttu-id="85254-140">x</span><span class="sxs-lookup"><span data-stu-id="85254-140">x</span></span>     | <span data-ttu-id="85254-141">x</span><span class="sxs-lookup"><span data-stu-id="85254-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="85254-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="85254-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85254-143">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="85254-143">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 
