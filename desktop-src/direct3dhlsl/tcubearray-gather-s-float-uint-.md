---
title: 'Função TextureCubeArray:: gather (S, float, uint)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função TextureCubeArray:: gather (S, float, uint)'
ms.assetid: B5C1843C-8DE4-4007-B619-2CC09B8A023B
keywords:
- Coletar HLSL da função
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9c3f7be9189daa045f378f62856ddb68a2be89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837867"
---
# <a name="texturecubearraygathersfloatuint-function"></a><span data-ttu-id="24658-105">Função TextureCubeArray:: gather (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="24658-105">TextureCubeArray::Gather(S,float,uint) function</span></span>

<span data-ttu-id="24658-106">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="24658-106">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="24658-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24658-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="24658-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24658-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24658-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="24658-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24658-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="24658-110">Type: **SamplerState**</span></span>

<span data-ttu-id="24658-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="24658-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="24658-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="24658-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24658-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="24658-113">Type: **float**</span></span>

<span data-ttu-id="24658-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="24658-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="24658-115">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="24658-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24658-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="24658-116">Type: **uint**</span></span>

<span data-ttu-id="24658-117">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="24658-117">The status of the operation.</span></span> <span data-ttu-id="24658-118">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="24658-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="24658-119">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="24658-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="24658-120">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="24658-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24658-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24658-121">Return value</span></span>

<span data-ttu-id="24658-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="24658-122">Type: **TemplateType**</span></span>

<span data-ttu-id="24658-123">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="24658-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="24658-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="24658-124">Remarks</span></span>

<span data-ttu-id="24658-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="24658-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="24658-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="24658-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="24658-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="24658-127">Vertex</span></span> | <span data-ttu-id="24658-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="24658-128">Hull</span></span> | <span data-ttu-id="24658-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="24658-129">Domain</span></span> | <span data-ttu-id="24658-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="24658-130">Geometry</span></span> | <span data-ttu-id="24658-131">16x16</span><span class="sxs-lookup"><span data-stu-id="24658-131">Pixel</span></span> | <span data-ttu-id="24658-132">Computação</span><span class="sxs-lookup"><span data-stu-id="24658-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="24658-133">x</span><span class="sxs-lookup"><span data-stu-id="24658-133">x</span></span>      | <span data-ttu-id="24658-134">x</span><span class="sxs-lookup"><span data-stu-id="24658-134">x</span></span>    | <span data-ttu-id="24658-135">x</span><span class="sxs-lookup"><span data-stu-id="24658-135">x</span></span>      | <span data-ttu-id="24658-136">x</span><span class="sxs-lookup"><span data-stu-id="24658-136">x</span></span>        | <span data-ttu-id="24658-137">x</span><span class="sxs-lookup"><span data-stu-id="24658-137">x</span></span>     | <span data-ttu-id="24658-138">x</span><span class="sxs-lookup"><span data-stu-id="24658-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="24658-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="24658-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24658-140">Reunir métodos</span><span class="sxs-lookup"><span data-stu-id="24658-140">Gather methods</span></span>](texturecubearray-gather.md)
</dt> <dt>

[<span data-ttu-id="24658-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="24658-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
