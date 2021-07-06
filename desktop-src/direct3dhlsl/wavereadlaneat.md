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
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316478"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="3ee0c-104">Função WaveReadLaneAt</span><span class="sxs-lookup"><span data-stu-id="3ee0c-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="3ee0c-105">Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee0c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ee0c-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="3ee0c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ee0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee0c-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="3ee0c-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="3ee0c-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="3ee0c-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="3ee0c-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="3ee0c-111">O índice da pista para a qual o resultado de *expr* será retornado.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee0c-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3ee0c-112">Return value</span></span>

<span data-ttu-id="3ee0c-113">O valor resultante é o resultado de *expr*.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="3ee0c-114">Será uniforme se *laneIndex* for uniforme.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ee0c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ee0c-115">Remarks</span></span>

<span data-ttu-id="3ee0c-116">Essa função é efetivamente uma difusão do valor na pista do *laneIndex*' th.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="3ee0c-117">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3ee0c-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ee0c-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3ee0c-118">See also</span></span>

* [<span data-ttu-id="3ee0c-119">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="3ee0c-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="3ee0c-120">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="3ee0c-120">Shader Model 6</span></span>](shader-model-6-0.md)
