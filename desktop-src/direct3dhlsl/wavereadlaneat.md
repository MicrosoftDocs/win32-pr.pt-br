---
title: Função WaveReadLaneAt
description: Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- HLSL da função WaveReadLaneAt
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2020
ms.locfileid: "104365800"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="5195d-104">Função WaveReadLaneAt</span><span class="sxs-lookup"><span data-stu-id="5195d-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="5195d-105">Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada.</span><span class="sxs-lookup"><span data-stu-id="5195d-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="5195d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5195d-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="5195d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5195d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5195d-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="5195d-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="5195d-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="5195d-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="5195d-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="5195d-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="5195d-111">O índice da pista para a qual o resultado de *expr* será retornado.</span><span class="sxs-lookup"><span data-stu-id="5195d-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5195d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5195d-112">Return value</span></span>

<span data-ttu-id="5195d-113">O valor resultante é o resultado de *expr*.</span><span class="sxs-lookup"><span data-stu-id="5195d-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="5195d-114">Será uniforme se *laneIndex* for uniforme.</span><span class="sxs-lookup"><span data-stu-id="5195d-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="5195d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5195d-115">Remarks</span></span>

<span data-ttu-id="5195d-116">Essa função é efetivamente uma difusão do valor na pista laneIndex'th.</span><span class="sxs-lookup"><span data-stu-id="5195d-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="5195d-117">Essa função tem suporte do modelo de sombreador 6,0, nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="5195d-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="5195d-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="5195d-118">Vertex</span></span> | <span data-ttu-id="5195d-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="5195d-119">Hull</span></span> | <span data-ttu-id="5195d-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="5195d-120">Domain</span></span> | <span data-ttu-id="5195d-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="5195d-121">Geometry</span></span> | <span data-ttu-id="5195d-122">16x16</span><span class="sxs-lookup"><span data-stu-id="5195d-122">Pixel</span></span> | <span data-ttu-id="5195d-123">Computação</span><span class="sxs-lookup"><span data-stu-id="5195d-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5195d-124">x</span><span class="sxs-lookup"><span data-stu-id="5195d-124">x</span></span>     | <span data-ttu-id="5195d-125">x</span><span class="sxs-lookup"><span data-stu-id="5195d-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5195d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5195d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5195d-127">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="5195d-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="5195d-128">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="5195d-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




