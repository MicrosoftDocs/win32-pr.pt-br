---
title: 'Função StructuredBuffer:: GetDimensions'
description: 'Obtém as dimensões do recurso. | Função StructuredBuffer:: GetDimensions'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298241"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="8cc09-105">Função StructuredBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="8cc09-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="8cc09-106">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="8cc09-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc09-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cc09-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="8cc09-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cc09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc09-109">*numStructs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc09-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc09-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8cc09-110">Type: **uint**</span></span>

<span data-ttu-id="8cc09-111">O número de estruturas no recurso.</span><span class="sxs-lookup"><span data-stu-id="8cc09-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8cc09-112">*Stride* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cc09-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc09-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8cc09-113">Type: **uint**</span></span>

<span data-ttu-id="8cc09-114">O stride, em bytes, de cada elemento da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8cc09-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc09-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cc09-115">Return value</span></span>

<span data-ttu-id="8cc09-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8cc09-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc09-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cc09-117">Remarks</span></span>

<span data-ttu-id="8cc09-118">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8cc09-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8cc09-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="8cc09-119">Vertex</span></span> | <span data-ttu-id="8cc09-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8cc09-120">Hull</span></span> | <span data-ttu-id="8cc09-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="8cc09-121">Domain</span></span> | <span data-ttu-id="8cc09-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="8cc09-122">Geometry</span></span> | <span data-ttu-id="8cc09-123">16x16</span><span class="sxs-lookup"><span data-stu-id="8cc09-123">Pixel</span></span> | <span data-ttu-id="8cc09-124">Computação</span><span class="sxs-lookup"><span data-stu-id="8cc09-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8cc09-125">x</span><span class="sxs-lookup"><span data-stu-id="8cc09-125">x</span></span>      | <span data-ttu-id="8cc09-126">x</span><span class="sxs-lookup"><span data-stu-id="8cc09-126">x</span></span>    | <span data-ttu-id="8cc09-127">x</span><span class="sxs-lookup"><span data-stu-id="8cc09-127">x</span></span>      | <span data-ttu-id="8cc09-128">x</span><span class="sxs-lookup"><span data-stu-id="8cc09-128">x</span></span>        | <span data-ttu-id="8cc09-129">x</span><span class="sxs-lookup"><span data-stu-id="8cc09-129">x</span></span>     | <span data-ttu-id="8cc09-130">x</span><span class="sxs-lookup"><span data-stu-id="8cc09-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8cc09-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc09-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc09-132">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="8cc09-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="8cc09-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8cc09-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




