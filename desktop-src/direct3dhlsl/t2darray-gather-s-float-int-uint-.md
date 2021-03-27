---
title: 'Função Texture2DArray:: gather (S, float, int, uint)'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Função Texture2DArray:: gather (S, float, int, uint)'
ms.assetid: 311A5042-19AA-41C7-8B22-2E34E4554250
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
ms.openlocfilehash: a1677fae87d8bbec3c0144cc8da0b5d13f0e0ae9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506408"
---
# <a name="texture2darraygathersfloatintuint-function"></a><span data-ttu-id="b4db2-105">Função Texture2DArray:: gather (S, float, int, uint)</span><span class="sxs-lookup"><span data-stu-id="b4db2-105">Texture2DArray::Gather(S,float,int,uint) function</span></span>

<span data-ttu-id="b4db2-106">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="b4db2-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4db2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4db2-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b4db2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4db2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4db2-109">*S* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="b4db2-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4db2-110">Tipo: **samplestate**</span><span class="sxs-lookup"><span data-stu-id="b4db2-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b4db2-111">O índice de amostra baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="b4db2-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b4db2-112">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b4db2-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4db2-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b4db2-113">Type: **float**</span></span>

<span data-ttu-id="b4db2-114">As coordenadas de exemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="b4db2-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b4db2-115">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4db2-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4db2-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b4db2-116">Type: **int**</span></span>

<span data-ttu-id="b4db2-117">O deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="b4db2-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="b4db2-118">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b4db2-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4db2-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b4db2-119">Type: **uint**</span></span>

<span data-ttu-id="b4db2-120">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="b4db2-120">The status of the operation.</span></span> <span data-ttu-id="b4db2-121">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b4db2-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b4db2-122">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b4db2-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b4db2-123">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="b4db2-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4db2-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4db2-124">Return value</span></span>

<span data-ttu-id="b4db2-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b4db2-125">Type: **TemplateType**</span></span>

<span data-ttu-id="b4db2-126">Um valor de quatro componentes cujo tipo é o mesmo que o tipo de modelo.</span><span class="sxs-lookup"><span data-stu-id="b4db2-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4db2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4db2-127">Remarks</span></span>

<span data-ttu-id="b4db2-128">Os exemplos de textura podem ser usados para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="b4db2-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b4db2-129">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b4db2-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b4db2-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="b4db2-130">Vertex</span></span> | <span data-ttu-id="b4db2-131">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b4db2-131">Hull</span></span> | <span data-ttu-id="b4db2-132">Domínio</span><span class="sxs-lookup"><span data-stu-id="b4db2-132">Domain</span></span> | <span data-ttu-id="b4db2-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="b4db2-133">Geometry</span></span> | <span data-ttu-id="b4db2-134">16x16</span><span class="sxs-lookup"><span data-stu-id="b4db2-134">Pixel</span></span> | <span data-ttu-id="b4db2-135">Computação</span><span class="sxs-lookup"><span data-stu-id="b4db2-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b4db2-136">x</span><span class="sxs-lookup"><span data-stu-id="b4db2-136">x</span></span>      | <span data-ttu-id="b4db2-137">x</span><span class="sxs-lookup"><span data-stu-id="b4db2-137">x</span></span>    | <span data-ttu-id="b4db2-138">x</span><span class="sxs-lookup"><span data-stu-id="b4db2-138">x</span></span>      | <span data-ttu-id="b4db2-139">x</span><span class="sxs-lookup"><span data-stu-id="b4db2-139">x</span></span>        | <span data-ttu-id="b4db2-140">x</span><span class="sxs-lookup"><span data-stu-id="b4db2-140">x</span></span>     | <span data-ttu-id="b4db2-141">x</span><span class="sxs-lookup"><span data-stu-id="b4db2-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b4db2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4db2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4db2-143">Reunir métodos</span><span class="sxs-lookup"><span data-stu-id="b4db2-143">Gather methods</span></span>](texture2darray-gather.md)
</dt> </dl>

 

 
