---
title: 'Função RWStructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função RWStructuredBuffer:: GetDimensions'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968283"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="d41ff-105">Função RWStructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="d41ff-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="d41ff-106">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="d41ff-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41ff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d41ff-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="d41ff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d41ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41ff-109">*numStructs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d41ff-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d41ff-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d41ff-110">Type: **uint**</span></span>

<span data-ttu-id="d41ff-111">O número de estruturas no recurso.</span><span class="sxs-lookup"><span data-stu-id="d41ff-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d41ff-112">*Stride* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d41ff-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d41ff-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d41ff-113">Type: **uint**</span></span>

<span data-ttu-id="d41ff-114">O stride, em bytes, de cada elemento da estrutura.</span><span class="sxs-lookup"><span data-stu-id="d41ff-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41ff-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d41ff-115">Return value</span></span>

<span data-ttu-id="d41ff-116">Nothing</span><span class="sxs-lookup"><span data-stu-id="d41ff-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="d41ff-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d41ff-117">Remarks</span></span>

<span data-ttu-id="d41ff-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d41ff-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d41ff-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="d41ff-119">Vertex</span></span> | <span data-ttu-id="d41ff-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="d41ff-120">Hull</span></span> | <span data-ttu-id="d41ff-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="d41ff-121">Domain</span></span> | <span data-ttu-id="d41ff-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="d41ff-122">Geometry</span></span> | <span data-ttu-id="d41ff-123">16x16</span><span class="sxs-lookup"><span data-stu-id="d41ff-123">Pixel</span></span> | <span data-ttu-id="d41ff-124">Computação</span><span class="sxs-lookup"><span data-stu-id="d41ff-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d41ff-125">x</span><span class="sxs-lookup"><span data-stu-id="d41ff-125">x</span></span>     | <span data-ttu-id="d41ff-126">x</span><span class="sxs-lookup"><span data-stu-id="d41ff-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d41ff-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d41ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41ff-128">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="d41ff-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="d41ff-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d41ff-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




