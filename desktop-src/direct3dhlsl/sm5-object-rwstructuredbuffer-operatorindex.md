---
title: 'Função RWStructuredBuffer:: Operator'
description: 'Retorna uma variável de recurso. | Função RWStructuredBuffer:: Operator'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
keywords:
- Função Operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506387"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="07b3c-105">Função RWStructuredBuffer:: Operator</span><span class="sxs-lookup"><span data-stu-id="07b3c-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="07b3c-106">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="07b3c-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b3c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07b3c-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="07b3c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07b3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b3c-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07b3c-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07b3c-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="07b3c-110">Type: **uint**</span></span>

<span data-ttu-id="07b3c-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="07b3c-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b3c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07b3c-112">Return value</span></span>

<span data-ttu-id="07b3c-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="07b3c-113">Type: **R**</span></span>

<span data-ttu-id="07b3c-114">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="07b3c-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="07b3c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="07b3c-115">Remarks</span></span>

<span data-ttu-id="07b3c-116">Um recurso estruturado pode ser indexado ainda mais com base nos nomes de componentes das estruturas.</span><span class="sxs-lookup"><span data-stu-id="07b3c-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="07b3c-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="07b3c-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="07b3c-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="07b3c-118">Vertex</span></span> | <span data-ttu-id="07b3c-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="07b3c-119">Hull</span></span> | <span data-ttu-id="07b3c-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="07b3c-120">Domain</span></span> | <span data-ttu-id="07b3c-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="07b3c-121">Geometry</span></span> | <span data-ttu-id="07b3c-122">16x16</span><span class="sxs-lookup"><span data-stu-id="07b3c-122">Pixel</span></span> | <span data-ttu-id="07b3c-123">Computação</span><span class="sxs-lookup"><span data-stu-id="07b3c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="07b3c-124">x</span><span class="sxs-lookup"><span data-stu-id="07b3c-124">x</span></span>     | <span data-ttu-id="07b3c-125">x</span><span class="sxs-lookup"><span data-stu-id="07b3c-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="07b3c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="07b3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b3c-127">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="07b3c-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="07b3c-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="07b3c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




