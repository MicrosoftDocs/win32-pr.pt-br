---
title: 'Função TextureCube:: GatherBlue (S, float, uint)'
description: 'Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco. | Função TextureCube:: GatherBlue (S, float, uint)'
ms.assetid: B2099321-3E81-4A77-A023-AF73594C68C8
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
ms.openlocfilehash: 59378e3a5754dbd55298d6040b40076a9e54eb74
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968486"
---
# <a name="texturecubegatherbluesfloatuint-function"></a><span data-ttu-id="92c91-105">Função TextureCube:: GatherBlue (S, float, uint)</span><span class="sxs-lookup"><span data-stu-id="92c91-105">TextureCube::GatherBlue(S,float,uint) function</span></span>

<span data-ttu-id="92c91-106">Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, juntamente com o status de mapeamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="92c91-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c91-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92c91-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="92c91-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92c91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c91-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="92c91-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c91-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="92c91-110">Type: **SamplerState**</span></span>

<span data-ttu-id="92c91-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="92c91-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="92c91-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="92c91-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c91-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="92c91-113">Type: **float**</span></span>

<span data-ttu-id="92c91-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="92c91-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="92c91-115">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="92c91-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92c91-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="92c91-116">Type: **uint**</span></span>

<span data-ttu-id="92c91-117">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="92c91-117">The status of the operation.</span></span> <span data-ttu-id="92c91-118">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="92c91-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="92c91-119">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="92c91-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="92c91-120">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="92c91-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c91-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92c91-121">Return value</span></span>

<span data-ttu-id="92c91-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="92c91-122">Type: **TemplateType**</span></span>

<span data-ttu-id="92c91-123">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="92c91-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c91-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="92c91-124">Remarks</span></span>

<span data-ttu-id="92c91-125">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="92c91-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="92c91-126">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="92c91-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="92c91-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="92c91-127">Vertex</span></span> | <span data-ttu-id="92c91-128">Envoltória</span><span class="sxs-lookup"><span data-stu-id="92c91-128">Hull</span></span> | <span data-ttu-id="92c91-129">Domínio</span><span class="sxs-lookup"><span data-stu-id="92c91-129">Domain</span></span> | <span data-ttu-id="92c91-130">Geometria</span><span class="sxs-lookup"><span data-stu-id="92c91-130">Geometry</span></span> | <span data-ttu-id="92c91-131">16x16</span><span class="sxs-lookup"><span data-stu-id="92c91-131">Pixel</span></span> | <span data-ttu-id="92c91-132">Computação</span><span class="sxs-lookup"><span data-stu-id="92c91-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="92c91-133">x</span><span class="sxs-lookup"><span data-stu-id="92c91-133">x</span></span>      | <span data-ttu-id="92c91-134">x</span><span class="sxs-lookup"><span data-stu-id="92c91-134">x</span></span>    | <span data-ttu-id="92c91-135">x</span><span class="sxs-lookup"><span data-stu-id="92c91-135">x</span></span>      | <span data-ttu-id="92c91-136">x</span><span class="sxs-lookup"><span data-stu-id="92c91-136">x</span></span>        | <span data-ttu-id="92c91-137">x</span><span class="sxs-lookup"><span data-stu-id="92c91-137">x</span></span>     | <span data-ttu-id="92c91-138">x</span><span class="sxs-lookup"><span data-stu-id="92c91-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="92c91-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="92c91-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c91-140">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="92c91-140">GatherBlue methods</span></span>](texturecube-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="92c91-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="92c91-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
