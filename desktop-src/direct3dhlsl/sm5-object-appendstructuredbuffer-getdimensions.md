---
title: 'Função AppendStructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função AppendStructuredBuffer:: GetDimensions'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968286"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="50aca-105">Função AppendStructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="50aca-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="50aca-106">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="50aca-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="50aca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50aca-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="50aca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50aca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50aca-109">*numStructs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50aca-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50aca-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="50aca-110">Type: **uint**</span></span>

<span data-ttu-id="50aca-111">O número de estruturas.</span><span class="sxs-lookup"><span data-stu-id="50aca-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="50aca-112">*Stride* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50aca-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50aca-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="50aca-113">Type: **uint**</span></span>

<span data-ttu-id="50aca-114">O número de bytes em cada elemento.</span><span class="sxs-lookup"><span data-stu-id="50aca-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50aca-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50aca-115">Return value</span></span>

<span data-ttu-id="50aca-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50aca-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50aca-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="50aca-117">Remarks</span></span>

<span data-ttu-id="50aca-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="50aca-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="50aca-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="50aca-119">Vertex</span></span> | <span data-ttu-id="50aca-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="50aca-120">Hull</span></span> | <span data-ttu-id="50aca-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="50aca-121">Domain</span></span> | <span data-ttu-id="50aca-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="50aca-122">Geometry</span></span> | <span data-ttu-id="50aca-123">16x16</span><span class="sxs-lookup"><span data-stu-id="50aca-123">Pixel</span></span> | <span data-ttu-id="50aca-124">Computação</span><span class="sxs-lookup"><span data-stu-id="50aca-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="50aca-125">x</span><span class="sxs-lookup"><span data-stu-id="50aca-125">x</span></span>      | <span data-ttu-id="50aca-126">x</span><span class="sxs-lookup"><span data-stu-id="50aca-126">x</span></span>    | <span data-ttu-id="50aca-127">x</span><span class="sxs-lookup"><span data-stu-id="50aca-127">x</span></span>      | <span data-ttu-id="50aca-128">x</span><span class="sxs-lookup"><span data-stu-id="50aca-128">x</span></span>        | <span data-ttu-id="50aca-129">x</span><span class="sxs-lookup"><span data-stu-id="50aca-129">x</span></span>     | <span data-ttu-id="50aca-130">x</span><span class="sxs-lookup"><span data-stu-id="50aca-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="50aca-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="50aca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50aca-132">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="50aca-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="50aca-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="50aca-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




