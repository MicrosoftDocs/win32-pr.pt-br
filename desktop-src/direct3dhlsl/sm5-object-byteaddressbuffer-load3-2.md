---
title: 'Função ByteAddressBuffer:: Load3 (uint, uint)'
description: Obtém três valores e o status da operação.
ms.assetid: 6AD8E957-F646-4749-A9B4-5C0C936D90E3
keywords:
- HLSL da função Load3
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bf3ffda082b8d2ae9cf22db59c1c38682563136
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294074"
---
# <a name="load3uint-uint-function"></a><span data-ttu-id="ca50d-104">Função Load3 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="ca50d-104">Load3(uint, uint) function</span></span>

<span data-ttu-id="ca50d-105">Obtém três valores e o status da operação.</span><span class="sxs-lookup"><span data-stu-id="ca50d-105">Gets three values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca50d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca50d-106">Syntax</span></span>

``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="ca50d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca50d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca50d-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ca50d-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca50d-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ca50d-109">Type: **uint**</span></span>

<span data-ttu-id="ca50d-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="ca50d-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="ca50d-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="ca50d-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca50d-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ca50d-112">Type: **uint**</span></span>

<span data-ttu-id="ca50d-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="ca50d-113">The status of the operation.</span></span> <span data-ttu-id="ca50d-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ca50d-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ca50d-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ca50d-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ca50d-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ca50d-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca50d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca50d-117">Return value</span></span>

<span data-ttu-id="ca50d-118">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="ca50d-118">Type: **uint3**</span></span>

<span data-ttu-id="ca50d-119">Três valores.</span><span class="sxs-lookup"><span data-stu-id="ca50d-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca50d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca50d-120">Remarks</span></span>

<span data-ttu-id="ca50d-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ca50d-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ca50d-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="ca50d-122">Vertex</span></span> | <span data-ttu-id="ca50d-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ca50d-123">Hull</span></span> | <span data-ttu-id="ca50d-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="ca50d-124">Domain</span></span> | <span data-ttu-id="ca50d-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="ca50d-125">Geometry</span></span> | <span data-ttu-id="ca50d-126">16x16</span><span class="sxs-lookup"><span data-stu-id="ca50d-126">Pixel</span></span> | <span data-ttu-id="ca50d-127">Computação</span><span class="sxs-lookup"><span data-stu-id="ca50d-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ca50d-128">x</span><span class="sxs-lookup"><span data-stu-id="ca50d-128">x</span></span>      | <span data-ttu-id="ca50d-129">x</span><span class="sxs-lookup"><span data-stu-id="ca50d-129">x</span></span>    | <span data-ttu-id="ca50d-130">x</span><span class="sxs-lookup"><span data-stu-id="ca50d-130">x</span></span>      | <span data-ttu-id="ca50d-131">x</span><span class="sxs-lookup"><span data-stu-id="ca50d-131">x</span></span>        | <span data-ttu-id="ca50d-132">x</span><span class="sxs-lookup"><span data-stu-id="ca50d-132">x</span></span>     | <span data-ttu-id="ca50d-133">x</span><span class="sxs-lookup"><span data-stu-id="ca50d-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ca50d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca50d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca50d-135">Métodos Load3</span><span class="sxs-lookup"><span data-stu-id="ca50d-135">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="ca50d-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="ca50d-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 