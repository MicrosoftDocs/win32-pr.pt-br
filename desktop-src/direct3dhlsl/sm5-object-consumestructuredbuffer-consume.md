---
title: 'Função ConsumeStructuredBuffer:: consume'
description: Remove um valor do final do buffer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Consumir função HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104006791"
---
# <a name="consume-function"></a><span data-ttu-id="9b6e5-104">Função de consumo</span><span class="sxs-lookup"><span data-stu-id="9b6e5-104">Consume function</span></span>

<span data-ttu-id="9b6e5-105">Remove um valor do final do buffer.</span><span class="sxs-lookup"><span data-stu-id="9b6e5-105">Removes a value from the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6e5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b6e5-106">Syntax</span></span>

``` syntax
T Consume(void);
```

## <a name="parameters"></a><span data-ttu-id="9b6e5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b6e5-107">Parameters</span></span>

<span data-ttu-id="9b6e5-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9b6e5-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b6e5-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9b6e5-109">Return value</span></span>

<span data-ttu-id="9b6e5-110">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="9b6e5-110">Type: **T**</span></span>

<span data-ttu-id="9b6e5-111">O valor removido (pode ser uma estrutura).</span><span class="sxs-lookup"><span data-stu-id="9b6e5-111">The value removed (can be a structure).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b6e5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b6e5-112">Remarks</span></span>

<span data-ttu-id="9b6e5-113">T pode ser qualquer tipo de dados, incluindo uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="9b6e5-113">T can be any data type including a structure.</span></span>

<span data-ttu-id="9b6e5-114">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9b6e5-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9b6e5-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="9b6e5-115">Vertex</span></span> | <span data-ttu-id="9b6e5-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9b6e5-116">Hull</span></span> | <span data-ttu-id="9b6e5-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="9b6e5-117">Domain</span></span> | <span data-ttu-id="9b6e5-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="9b6e5-118">Geometry</span></span> | <span data-ttu-id="9b6e5-119">16x16</span><span class="sxs-lookup"><span data-stu-id="9b6e5-119">Pixel</span></span> | <span data-ttu-id="9b6e5-120">Computação</span><span class="sxs-lookup"><span data-stu-id="9b6e5-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b6e5-121">x</span><span class="sxs-lookup"><span data-stu-id="9b6e5-121">x</span></span>      | <span data-ttu-id="9b6e5-122">x</span><span class="sxs-lookup"><span data-stu-id="9b6e5-122">x</span></span>    | <span data-ttu-id="9b6e5-123">x</span><span class="sxs-lookup"><span data-stu-id="9b6e5-123">x</span></span>      | <span data-ttu-id="9b6e5-124">x</span><span class="sxs-lookup"><span data-stu-id="9b6e5-124">x</span></span>        | <span data-ttu-id="9b6e5-125">x</span><span class="sxs-lookup"><span data-stu-id="9b6e5-125">x</span></span>     | <span data-ttu-id="9b6e5-126">x</span><span class="sxs-lookup"><span data-stu-id="9b6e5-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9b6e5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b6e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6e5-128">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="9b6e5-128">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="9b6e5-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9b6e5-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




