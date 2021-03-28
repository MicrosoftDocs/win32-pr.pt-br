---
title: 'Função ConsumeStructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função ConsumeStructuredBuffer:: GetDimensions'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989142"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="b80b4-105">Função ConsumeStructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="b80b4-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="b80b4-106">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="b80b4-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b80b4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b80b4-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="b80b4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b80b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b80b4-109">*numStructs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b80b4-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b80b4-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b80b4-110">Type: **uint**</span></span>

<span data-ttu-id="b80b4-111">O número de estruturas.</span><span class="sxs-lookup"><span data-stu-id="b80b4-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="b80b4-112">*Stride* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b80b4-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b80b4-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b80b4-113">Type: **uint**</span></span>

<span data-ttu-id="b80b4-114">O stride, em bytes, de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="b80b4-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b80b4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b80b4-115">Return value</span></span>

<span data-ttu-id="b80b4-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b80b4-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b80b4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b80b4-117">Remarks</span></span>

<span data-ttu-id="b80b4-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b80b4-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b80b4-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="b80b4-119">Vertex</span></span> | <span data-ttu-id="b80b4-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b80b4-120">Hull</span></span> | <span data-ttu-id="b80b4-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="b80b4-121">Domain</span></span> | <span data-ttu-id="b80b4-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="b80b4-122">Geometry</span></span> | <span data-ttu-id="b80b4-123">16x16</span><span class="sxs-lookup"><span data-stu-id="b80b4-123">Pixel</span></span> | <span data-ttu-id="b80b4-124">Computação</span><span class="sxs-lookup"><span data-stu-id="b80b4-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b80b4-125">x</span><span class="sxs-lookup"><span data-stu-id="b80b4-125">x</span></span>      | <span data-ttu-id="b80b4-126">x</span><span class="sxs-lookup"><span data-stu-id="b80b4-126">x</span></span>    | <span data-ttu-id="b80b4-127">x</span><span class="sxs-lookup"><span data-stu-id="b80b4-127">x</span></span>      | <span data-ttu-id="b80b4-128">x</span><span class="sxs-lookup"><span data-stu-id="b80b4-128">x</span></span>        | <span data-ttu-id="b80b4-129">x</span><span class="sxs-lookup"><span data-stu-id="b80b4-129">x</span></span>     | <span data-ttu-id="b80b4-130">x</span><span class="sxs-lookup"><span data-stu-id="b80b4-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b80b4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b80b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b80b4-132">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="b80b4-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="b80b4-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b80b4-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




