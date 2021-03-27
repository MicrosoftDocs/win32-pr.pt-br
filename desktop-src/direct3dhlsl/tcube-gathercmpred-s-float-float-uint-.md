---
title: 'Função TextureCube:: GatherCmpRed (S, float, float, uint)'
description: 'Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de bloco. | Função TextureCube:: GatherCmpRed (S, float, float, uint)'
ms.assetid: 99ADA450-9665-4870-924E-E4DAEFA912D5
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
ms.openlocfilehash: e77cd1d062be60033648942597a91f7d5ab4b951
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930475"
---
# <a name="texturecubegathercmpredsfloatfloatuint-function"></a><span data-ttu-id="cda36-105">Função TextureCube:: GatherCmpRed (S, float, float, uint)</span><span class="sxs-lookup"><span data-stu-id="cda36-105">TextureCube::GatherCmpRed(S,float,float,uint) function</span></span>

<span data-ttu-id="cda36-106">Para quatro valores de Texel que seriam usados em uma operação de filtragem de bi linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação junto com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="cda36-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda36-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cda36-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="cda36-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cda36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda36-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="cda36-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda36-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="cda36-110">Type: **SamplerState**</span></span>

<span data-ttu-id="cda36-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="cda36-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="cda36-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cda36-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda36-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cda36-113">Type: **float**</span></span>

<span data-ttu-id="cda36-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="cda36-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="cda36-115">*Comparevalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cda36-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda36-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cda36-116">Type: **float**</span></span>

<span data-ttu-id="cda36-117">Um valor para comparar cada valor de amostra.</span><span class="sxs-lookup"><span data-stu-id="cda36-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="cda36-118">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="cda36-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cda36-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cda36-119">Type: **uint**</span></span>

<span data-ttu-id="cda36-120">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="cda36-120">The status of the operation.</span></span> <span data-ttu-id="cda36-121">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="cda36-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cda36-122">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="cda36-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cda36-123">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="cda36-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda36-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cda36-124">Return value</span></span>

<span data-ttu-id="cda36-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="cda36-125">Type: **TemplateType**</span></span>

<span data-ttu-id="cda36-126">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="cda36-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda36-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cda36-127">Remarks</span></span>

<span data-ttu-id="cda36-128">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="cda36-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="cda36-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="cda36-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cda36-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="cda36-130">Vertex</span></span> | <span data-ttu-id="cda36-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="cda36-131">Hull</span></span> | <span data-ttu-id="cda36-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="cda36-132">Domain</span></span> | <span data-ttu-id="cda36-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="cda36-133">Geometry</span></span> | <span data-ttu-id="cda36-134">16x16</span><span class="sxs-lookup"><span data-stu-id="cda36-134">Pixel</span></span> | <span data-ttu-id="cda36-135">Computação</span><span class="sxs-lookup"><span data-stu-id="cda36-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cda36-136">x</span><span class="sxs-lookup"><span data-stu-id="cda36-136">x</span></span>      | <span data-ttu-id="cda36-137">x</span><span class="sxs-lookup"><span data-stu-id="cda36-137">x</span></span>    | <span data-ttu-id="cda36-138">x</span><span class="sxs-lookup"><span data-stu-id="cda36-138">x</span></span>      | <span data-ttu-id="cda36-139">x</span><span class="sxs-lookup"><span data-stu-id="cda36-139">x</span></span>        | <span data-ttu-id="cda36-140">x</span><span class="sxs-lookup"><span data-stu-id="cda36-140">x</span></span>     | <span data-ttu-id="cda36-141">x</span><span class="sxs-lookup"><span data-stu-id="cda36-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cda36-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="cda36-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda36-143">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="cda36-143">GatherCmpRed methods</span></span>](texturecube-gathercmpred.md)
</dt> <dt>

[<span data-ttu-id="cda36-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="cda36-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
