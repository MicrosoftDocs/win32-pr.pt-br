---
title: 'Função Texture1D:: Load (int, int, uint)'
description: 'Lê os dados de textura e retorna o status da operação. | Função Texture1D:: Load (int, int, uint)'
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968417"
---
# <a name="texture1dloadintintuint-function"></a><span data-ttu-id="43646-105">Função Texture1D:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="43646-105">Texture1D::Load(int,int,uint) function</span></span>

<span data-ttu-id="43646-106">Lê os dados de textura e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="43646-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="43646-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43646-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="43646-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43646-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43646-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="43646-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43646-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="43646-110">Type: **int**</span></span>

<span data-ttu-id="43646-111">As coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="43646-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="43646-112">*Deslocamento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43646-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43646-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="43646-113">Type: **int**</span></span>

<span data-ttu-id="43646-114">Um deslocamento aplicado às coordenadas de textura antes da amostragem.</span><span class="sxs-lookup"><span data-stu-id="43646-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="43646-115">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="43646-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43646-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="43646-116">Type: **uint**</span></span>

<span data-ttu-id="43646-117">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="43646-117">The status of the operation.</span></span> <span data-ttu-id="43646-118">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="43646-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="43646-119">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="43646-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="43646-120">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="43646-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43646-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43646-121">Return value</span></span>

<span data-ttu-id="43646-122">Tipo:</span><span class="sxs-lookup"><span data-stu-id="43646-122">Type:</span></span>

<span data-ttu-id="43646-123">O tipo de retorno corresponde ao tipo na declaração para o objeto [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="43646-123">The return type matches the type in the declaration for the [**Texture1D**](sm5-object-texture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="43646-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="43646-124">Remarks</span></span>

<span data-ttu-id="43646-125">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="43646-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="43646-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="43646-126">Vertex</span></span> | <span data-ttu-id="43646-127">Envoltória</span><span class="sxs-lookup"><span data-stu-id="43646-127">Hull</span></span> | <span data-ttu-id="43646-128">Domínio</span><span class="sxs-lookup"><span data-stu-id="43646-128">Domain</span></span> | <span data-ttu-id="43646-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="43646-129">Geometry</span></span> | <span data-ttu-id="43646-130">16x16</span><span class="sxs-lookup"><span data-stu-id="43646-130">Pixel</span></span> | <span data-ttu-id="43646-131">Computação</span><span class="sxs-lookup"><span data-stu-id="43646-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="43646-132">x</span><span class="sxs-lookup"><span data-stu-id="43646-132">x</span></span>      | <span data-ttu-id="43646-133">x</span><span class="sxs-lookup"><span data-stu-id="43646-133">x</span></span>    | <span data-ttu-id="43646-134">x</span><span class="sxs-lookup"><span data-stu-id="43646-134">x</span></span>      | <span data-ttu-id="43646-135">x</span><span class="sxs-lookup"><span data-stu-id="43646-135">x</span></span>        | <span data-ttu-id="43646-136">x</span><span class="sxs-lookup"><span data-stu-id="43646-136">x</span></span>     | <span data-ttu-id="43646-137">x</span><span class="sxs-lookup"><span data-stu-id="43646-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="43646-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="43646-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43646-139">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="43646-139">Load methods</span></span>](texture1d-load.md)
</dt> <dt>

[<span data-ttu-id="43646-140">**Texture1D**</span><span class="sxs-lookup"><span data-stu-id="43646-140">**Texture1D**</span></span>](sm5-object-texture1d.md)
</dt> </dl>

 

 
