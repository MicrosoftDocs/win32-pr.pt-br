---
title: 'Função ByteAddressBuffer:: Load4 (uint, uint)'
description: Obtém quatro valores e o status da operação.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- HLSL da função Load4
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007572"
---
# <a name="load4uint-uint-function"></a><span data-ttu-id="a002f-104">Função Load4 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="a002f-104">Load4(uint, uint) function</span></span>

<span data-ttu-id="a002f-105">Obtém quatro valores e o status da operação.</span><span class="sxs-lookup"><span data-stu-id="a002f-105">Gets four values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a002f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a002f-106">Syntax</span></span>

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="a002f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a002f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a002f-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a002f-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a002f-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a002f-109">Type: **uint**</span></span>

<span data-ttu-id="a002f-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="a002f-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="a002f-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a002f-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a002f-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a002f-112">Type: **uint**</span></span>

<span data-ttu-id="a002f-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="a002f-113">The status of the operation.</span></span> <span data-ttu-id="a002f-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a002f-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a002f-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a002f-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a002f-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="a002f-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a002f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a002f-117">Return value</span></span>

<span data-ttu-id="a002f-118">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="a002f-118">Type: **uint4**</span></span>

<span data-ttu-id="a002f-119">Quatro valores.</span><span class="sxs-lookup"><span data-stu-id="a002f-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a002f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a002f-120">Remarks</span></span>

<span data-ttu-id="a002f-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a002f-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a002f-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="a002f-122">Vertex</span></span> | <span data-ttu-id="a002f-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a002f-123">Hull</span></span> | <span data-ttu-id="a002f-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="a002f-124">Domain</span></span> | <span data-ttu-id="a002f-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="a002f-125">Geometry</span></span> | <span data-ttu-id="a002f-126">16x16</span><span class="sxs-lookup"><span data-stu-id="a002f-126">Pixel</span></span> | <span data-ttu-id="a002f-127">Computação</span><span class="sxs-lookup"><span data-stu-id="a002f-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a002f-128">x</span><span class="sxs-lookup"><span data-stu-id="a002f-128">x</span></span>      | <span data-ttu-id="a002f-129">x</span><span class="sxs-lookup"><span data-stu-id="a002f-129">x</span></span>    | <span data-ttu-id="a002f-130">x</span><span class="sxs-lookup"><span data-stu-id="a002f-130">x</span></span>      | <span data-ttu-id="a002f-131">x</span><span class="sxs-lookup"><span data-stu-id="a002f-131">x</span></span>        | <span data-ttu-id="a002f-132">x</span><span class="sxs-lookup"><span data-stu-id="a002f-132">x</span></span>     | <span data-ttu-id="a002f-133">x</span><span class="sxs-lookup"><span data-stu-id="a002f-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a002f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a002f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a002f-135">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="a002f-135">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="a002f-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="a002f-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 