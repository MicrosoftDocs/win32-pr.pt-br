---
title: 'Função RWByteAddressBuffer:: Load3 (uint, uint)'
description: Obtém três valores e retorna o status da operação.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
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
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294339"
---
# <a name="load3uintuint-function"></a><span data-ttu-id="59817-104">Função Load3 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="59817-104">Load3(uint,uint) function</span></span>

<span data-ttu-id="59817-105">Obtém três valores e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="59817-105">Gets three values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="59817-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59817-106">Syntax</span></span>


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="59817-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59817-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59817-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="59817-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59817-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="59817-109">Type: **uint**</span></span>

<span data-ttu-id="59817-110">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="59817-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="59817-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="59817-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59817-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="59817-112">Type: **uint**</span></span>

<span data-ttu-id="59817-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="59817-113">The status of the operation.</span></span> <span data-ttu-id="59817-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="59817-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="59817-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="59817-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="59817-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="59817-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59817-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59817-117">Return value</span></span>

<span data-ttu-id="59817-118">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="59817-118">Type: **uint3**</span></span>

<span data-ttu-id="59817-119">Três valores.</span><span class="sxs-lookup"><span data-stu-id="59817-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="59817-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="59817-120">Remarks</span></span>

<span data-ttu-id="59817-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="59817-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="59817-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="59817-122">Vertex</span></span> | <span data-ttu-id="59817-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="59817-123">Hull</span></span> | <span data-ttu-id="59817-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="59817-124">Domain</span></span> | <span data-ttu-id="59817-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="59817-125">Geometry</span></span> | <span data-ttu-id="59817-126">16x16</span><span class="sxs-lookup"><span data-stu-id="59817-126">Pixel</span></span> | <span data-ttu-id="59817-127">Computação</span><span class="sxs-lookup"><span data-stu-id="59817-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="59817-128">x</span><span class="sxs-lookup"><span data-stu-id="59817-128">x</span></span>     | <span data-ttu-id="59817-129">x</span><span class="sxs-lookup"><span data-stu-id="59817-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="59817-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="59817-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59817-131">Métodos Load3</span><span class="sxs-lookup"><span data-stu-id="59817-131">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 