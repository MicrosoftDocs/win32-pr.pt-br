---
title: 'Função TextureCubeArray:: GatherBlue (S, float, uint)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função TextureCubeArray:: GatherBlue (S, float, uint)'
ms.assetid: 85606EE7-9B05-439F-B525-A1CD42FE32F6
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
ms.openlocfilehash: b96282bd57b6cbef248a7090ad4a297cd5a81740
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370888"
---
# <a name="texturecubearraygatherbluesfloatuint-function"></a><span data-ttu-id="ec03f-105">Função TextureCubeArray:: GatherBlue (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="ec03f-105">TextureCubeArray::GatherBlue(S,float,uint) function</span></span>

<span data-ttu-id="ec03f-106">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="ec03f-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec03f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec03f-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ec03f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec03f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec03f-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ec03f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec03f-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="ec03f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ec03f-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="ec03f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ec03f-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ec03f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec03f-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ec03f-113">Type: **float**</span></span>

<span data-ttu-id="ec03f-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="ec03f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ec03f-115">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="ec03f-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec03f-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ec03f-116">Type: **uint**</span></span>

<span data-ttu-id="ec03f-117">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="ec03f-117">The status of the operation.</span></span> <span data-ttu-id="ec03f-118">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ec03f-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ec03f-119">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ec03f-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ec03f-120">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ec03f-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec03f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec03f-121">Return value</span></span>

<span data-ttu-id="ec03f-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ec03f-122">Type: **TemplateType**</span></span>

<span data-ttu-id="ec03f-123">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="ec03f-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec03f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec03f-124">Remarks</span></span>

<span data-ttu-id="ec03f-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="ec03f-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ec03f-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ec03f-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ec03f-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="ec03f-127">Vertex</span></span> | <span data-ttu-id="ec03f-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ec03f-128">Hull</span></span> | <span data-ttu-id="ec03f-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="ec03f-129">Domain</span></span> | <span data-ttu-id="ec03f-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="ec03f-130">Geometry</span></span> | <span data-ttu-id="ec03f-131">16x16</span><span class="sxs-lookup"><span data-stu-id="ec03f-131">Pixel</span></span> | <span data-ttu-id="ec03f-132">Computação</span><span class="sxs-lookup"><span data-stu-id="ec03f-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ec03f-133">x</span><span class="sxs-lookup"><span data-stu-id="ec03f-133">x</span></span>      | <span data-ttu-id="ec03f-134">x</span><span class="sxs-lookup"><span data-stu-id="ec03f-134">x</span></span>    | <span data-ttu-id="ec03f-135">x</span><span class="sxs-lookup"><span data-stu-id="ec03f-135">x</span></span>      | <span data-ttu-id="ec03f-136">x</span><span class="sxs-lookup"><span data-stu-id="ec03f-136">x</span></span>        | <span data-ttu-id="ec03f-137">x</span><span class="sxs-lookup"><span data-stu-id="ec03f-137">x</span></span>     | <span data-ttu-id="ec03f-138">x</span><span class="sxs-lookup"><span data-stu-id="ec03f-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ec03f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec03f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec03f-140">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="ec03f-140">GatherBlue methods</span></span>](texturecubearray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="ec03f-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="ec03f-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
