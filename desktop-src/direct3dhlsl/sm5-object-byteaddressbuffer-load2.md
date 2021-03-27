---
title: 'Função ByteAddressBuffer:: Load2 (UINT)'
description: 'Obtém dois valores. | Função ByteAddressBuffer:: Load2 (UINT)'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- HLSL da função Load2
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663861"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="fc6e4-105">Função ByteAddressBuffer:: Load2 (UINT)</span><span class="sxs-lookup"><span data-stu-id="fc6e4-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="fc6e4-106">Obtém dois valores.</span><span class="sxs-lookup"><span data-stu-id="fc6e4-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc6e4-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="fc6e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc6e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6e4-109">*endereço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc6e4-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6e4-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fc6e4-110">Type: **uint**</span></span>

<span data-ttu-id="fc6e4-111">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="fc6e4-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc6e4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc6e4-112">Return value</span></span>

<span data-ttu-id="fc6e4-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="fc6e4-113">Type: **uint2**</span></span>

<span data-ttu-id="fc6e4-114">Dois valores.</span><span class="sxs-lookup"><span data-stu-id="fc6e4-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6e4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc6e4-115">Remarks</span></span>

<span data-ttu-id="fc6e4-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fc6e4-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fc6e4-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="fc6e4-117">Vertex</span></span> | <span data-ttu-id="fc6e4-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="fc6e4-118">Hull</span></span> | <span data-ttu-id="fc6e4-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="fc6e4-119">Domain</span></span> | <span data-ttu-id="fc6e4-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="fc6e4-120">Geometry</span></span> | <span data-ttu-id="fc6e4-121">16x16</span><span class="sxs-lookup"><span data-stu-id="fc6e4-121">Pixel</span></span> | <span data-ttu-id="fc6e4-122">Computação</span><span class="sxs-lookup"><span data-stu-id="fc6e4-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fc6e4-123">x</span><span class="sxs-lookup"><span data-stu-id="fc6e4-123">x</span></span>      | <span data-ttu-id="fc6e4-124">x</span><span class="sxs-lookup"><span data-stu-id="fc6e4-124">x</span></span>    | <span data-ttu-id="fc6e4-125">x</span><span class="sxs-lookup"><span data-stu-id="fc6e4-125">x</span></span>      | <span data-ttu-id="fc6e4-126">x</span><span class="sxs-lookup"><span data-stu-id="fc6e4-126">x</span></span>        | <span data-ttu-id="fc6e4-127">x</span><span class="sxs-lookup"><span data-stu-id="fc6e4-127">x</span></span>     | <span data-ttu-id="fc6e4-128">x</span><span class="sxs-lookup"><span data-stu-id="fc6e4-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fc6e4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc6e4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6e4-130">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="fc6e4-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="fc6e4-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fc6e4-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




