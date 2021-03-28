---
title: 'Função RWBuffer:: Operator'
description: 'Retorna uma variável de recurso. | Função RWBuffer:: Operator'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989140"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="aca9c-105">Função RWBuffer:: Operator</span><span class="sxs-lookup"><span data-stu-id="aca9c-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="aca9c-106">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="aca9c-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca9c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aca9c-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="aca9c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aca9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca9c-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aca9c-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca9c-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="aca9c-110">Type: **uint**</span></span>

<span data-ttu-id="aca9c-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="aca9c-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca9c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aca9c-112">Return value</span></span>

<span data-ttu-id="aca9c-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="aca9c-113">Type: **R**</span></span>

<span data-ttu-id="aca9c-114">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="aca9c-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca9c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aca9c-115">Remarks</span></span>

<span data-ttu-id="aca9c-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="aca9c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aca9c-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="aca9c-117">Vertex</span></span> | <span data-ttu-id="aca9c-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="aca9c-118">Hull</span></span> | <span data-ttu-id="aca9c-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="aca9c-119">Domain</span></span> | <span data-ttu-id="aca9c-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="aca9c-120">Geometry</span></span> | <span data-ttu-id="aca9c-121">16x16</span><span class="sxs-lookup"><span data-stu-id="aca9c-121">Pixel</span></span> | <span data-ttu-id="aca9c-122">Computação</span><span class="sxs-lookup"><span data-stu-id="aca9c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aca9c-123">x</span><span class="sxs-lookup"><span data-stu-id="aca9c-123">x</span></span>      | <span data-ttu-id="aca9c-124">x</span><span class="sxs-lookup"><span data-stu-id="aca9c-124">x</span></span>    | <span data-ttu-id="aca9c-125">x</span><span class="sxs-lookup"><span data-stu-id="aca9c-125">x</span></span>      | <span data-ttu-id="aca9c-126">x</span><span class="sxs-lookup"><span data-stu-id="aca9c-126">x</span></span>        | <span data-ttu-id="aca9c-127">x</span><span class="sxs-lookup"><span data-stu-id="aca9c-127">x</span></span>     | <span data-ttu-id="aca9c-128">x</span><span class="sxs-lookup"><span data-stu-id="aca9c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aca9c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="aca9c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca9c-130">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="aca9c-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="aca9c-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="aca9c-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




