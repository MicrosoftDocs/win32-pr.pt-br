---
title: 'Função TextureCubeArray:: GatherCmp (S, float, float, uint)'
description: 'Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação junto com o status de mapeamento de bloco. | Função TextureCubeArray:: GatherCmp (S, float, float, uint)'
ms.assetid: 758CD159-58B6-42AE-92B3-5AA3C72FD0F1
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
ms.openlocfilehash: 73ef87805fa69529e1790c3ac2fed539cac57b0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298213"
---
# <a name="texturecubearraygathercmpsfloatfloatuint-function"></a><span data-ttu-id="ac816-105">Função TextureCubeArray:: GatherCmp (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="ac816-105">TextureCubeArray::GatherCmp(S,float,float,uint) function</span></span>

<span data-ttu-id="ac816-106">Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="ac816-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac816-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac816-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ac816-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac816-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac816-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ac816-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac816-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="ac816-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ac816-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="ac816-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ac816-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ac816-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac816-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ac816-113">Type: **float**</span></span>

<span data-ttu-id="ac816-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="ac816-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ac816-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac816-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac816-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ac816-116">Type: **float**</span></span>

<span data-ttu-id="ac816-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="ac816-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="ac816-118">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="ac816-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac816-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ac816-119">Type: **uint**</span></span>

<span data-ttu-id="ac816-120">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="ac816-120">The status of the operation.</span></span> <span data-ttu-id="ac816-121">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ac816-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ac816-122">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ac816-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ac816-123">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ac816-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac816-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac816-124">Return value</span></span>

<span data-ttu-id="ac816-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ac816-125">Type: **TemplateType**</span></span>

<span data-ttu-id="ac816-126">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="ac816-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac816-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac816-127">Remarks</span></span>

<span data-ttu-id="ac816-128">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="ac816-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ac816-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ac816-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ac816-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="ac816-130">Vertex</span></span> | <span data-ttu-id="ac816-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ac816-131">Hull</span></span> | <span data-ttu-id="ac816-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="ac816-132">Domain</span></span> | <span data-ttu-id="ac816-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="ac816-133">Geometry</span></span> | <span data-ttu-id="ac816-134">16x16</span><span class="sxs-lookup"><span data-stu-id="ac816-134">Pixel</span></span> | <span data-ttu-id="ac816-135">Computação</span><span class="sxs-lookup"><span data-stu-id="ac816-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac816-136">x</span><span class="sxs-lookup"><span data-stu-id="ac816-136">x</span></span>      | <span data-ttu-id="ac816-137">x</span><span class="sxs-lookup"><span data-stu-id="ac816-137">x</span></span>    | <span data-ttu-id="ac816-138">x</span><span class="sxs-lookup"><span data-stu-id="ac816-138">x</span></span>      | <span data-ttu-id="ac816-139">x</span><span class="sxs-lookup"><span data-stu-id="ac816-139">x</span></span>        | <span data-ttu-id="ac816-140">x</span><span class="sxs-lookup"><span data-stu-id="ac816-140">x</span></span>     | <span data-ttu-id="ac816-141">x</span><span class="sxs-lookup"><span data-stu-id="ac816-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ac816-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac816-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac816-143">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="ac816-143">GatherCmp methods</span></span>](texturecubearray-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="ac816-144">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="ac816-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
