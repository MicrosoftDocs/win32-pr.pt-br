---
title: 'Função ByteAddressBuffer:: Load3 (UINT)'
description: 'Obtém três valores. | Função ByteAddressBuffer:: Load3 (UINT)'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
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
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968495"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="708a6-105">Função ByteAddressBuffer:: Load3 (UINT)</span><span class="sxs-lookup"><span data-stu-id="708a6-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="708a6-106">Obtém três valores.</span><span class="sxs-lookup"><span data-stu-id="708a6-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="708a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="708a6-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="708a6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="708a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708a6-109">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="708a6-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708a6-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="708a6-110">Type: **uint**</span></span>

<span data-ttu-id="708a6-111">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="708a6-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708a6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="708a6-112">Return value</span></span>

<span data-ttu-id="708a6-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="708a6-113">Type: **uint3**</span></span>

<span data-ttu-id="708a6-114">Três valores.</span><span class="sxs-lookup"><span data-stu-id="708a6-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="708a6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="708a6-115">Remarks</span></span>

<span data-ttu-id="708a6-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="708a6-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="708a6-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="708a6-117">Vertex</span></span> | <span data-ttu-id="708a6-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="708a6-118">Hull</span></span> | <span data-ttu-id="708a6-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="708a6-119">Domain</span></span> | <span data-ttu-id="708a6-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="708a6-120">Geometry</span></span> | <span data-ttu-id="708a6-121">16x16</span><span class="sxs-lookup"><span data-stu-id="708a6-121">Pixel</span></span> | <span data-ttu-id="708a6-122">Computação</span><span class="sxs-lookup"><span data-stu-id="708a6-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="708a6-123">x</span><span class="sxs-lookup"><span data-stu-id="708a6-123">x</span></span>      | <span data-ttu-id="708a6-124">x</span><span class="sxs-lookup"><span data-stu-id="708a6-124">x</span></span>    | <span data-ttu-id="708a6-125">x</span><span class="sxs-lookup"><span data-stu-id="708a6-125">x</span></span>      | <span data-ttu-id="708a6-126">x</span><span class="sxs-lookup"><span data-stu-id="708a6-126">x</span></span>        | <span data-ttu-id="708a6-127">x</span><span class="sxs-lookup"><span data-stu-id="708a6-127">x</span></span>     | <span data-ttu-id="708a6-128">x</span><span class="sxs-lookup"><span data-stu-id="708a6-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="708a6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="708a6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708a6-130">Métodos Load3</span><span class="sxs-lookup"><span data-stu-id="708a6-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="708a6-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="708a6-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




