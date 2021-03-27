---
title: Função WaveActiveProduct
description: Multiplica os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- HLSL da função WaveActiveProduct
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824063"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="2aed4-104">Função WaveActiveProduct</span><span class="sxs-lookup"><span data-stu-id="2aed4-104">WaveActiveProduct function</span></span>

<span data-ttu-id="2aed4-105">Multiplica os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="2aed4-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aed4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aed4-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="2aed4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2aed4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aed4-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="2aed4-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="2aed4-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="2aed4-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aed4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2aed4-110">Return value</span></span>

<span data-ttu-id="2aed4-111">O valor do produto.</span><span class="sxs-lookup"><span data-stu-id="2aed4-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aed4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aed4-112">Remarks</span></span>

<span data-ttu-id="2aed4-113">A ordem das operações é indefinida.</span><span class="sxs-lookup"><span data-stu-id="2aed4-113">The order of operations is undefined.</span></span>

<span data-ttu-id="2aed4-114">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2aed4-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="2aed4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aed4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aed4-116">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="2aed4-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="2aed4-117">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="2aed4-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




