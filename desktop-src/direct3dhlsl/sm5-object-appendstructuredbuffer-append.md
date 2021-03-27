---
title: 'Função AppendStructuredBuffer:: Append'
description: Anexa um valor ao final do buffer.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Acrescentar função HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103916835"
---
# <a name="append-function"></a><span data-ttu-id="3d775-104">Função Append</span><span class="sxs-lookup"><span data-stu-id="3d775-104">Append function</span></span>

<span data-ttu-id="3d775-105">Anexa um valor ao final do buffer.</span><span class="sxs-lookup"><span data-stu-id="3d775-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d775-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d775-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="3d775-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d775-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d775-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3d775-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d775-109">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="3d775-109">Type: **T**</span></span>

<span data-ttu-id="3d775-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d775-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d775-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d775-111">Return value</span></span>

<span data-ttu-id="3d775-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3d775-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="3d775-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d775-113">Remarks</span></span>

<span data-ttu-id="3d775-114">T pode ser qualquer tipo de dados, incluindo estruturas.</span><span class="sxs-lookup"><span data-stu-id="3d775-114">T can be any data type including structures.</span></span>

<span data-ttu-id="3d775-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3d775-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3d775-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="3d775-116">Vertex</span></span> | <span data-ttu-id="3d775-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3d775-117">Hull</span></span> | <span data-ttu-id="3d775-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="3d775-118">Domain</span></span> | <span data-ttu-id="3d775-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="3d775-119">Geometry</span></span> | <span data-ttu-id="3d775-120">16x16</span><span class="sxs-lookup"><span data-stu-id="3d775-120">Pixel</span></span> | <span data-ttu-id="3d775-121">Computação</span><span class="sxs-lookup"><span data-stu-id="3d775-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3d775-122">x</span><span class="sxs-lookup"><span data-stu-id="3d775-122">x</span></span>      | <span data-ttu-id="3d775-123">x</span><span class="sxs-lookup"><span data-stu-id="3d775-123">x</span></span>    | <span data-ttu-id="3d775-124">x</span><span class="sxs-lookup"><span data-stu-id="3d775-124">x</span></span>      | <span data-ttu-id="3d775-125">x</span><span class="sxs-lookup"><span data-stu-id="3d775-125">x</span></span>        | <span data-ttu-id="3d775-126">x</span><span class="sxs-lookup"><span data-stu-id="3d775-126">x</span></span>     | <span data-ttu-id="3d775-127">x</span><span class="sxs-lookup"><span data-stu-id="3d775-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3d775-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d775-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d775-129">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="3d775-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="3d775-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3d775-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




