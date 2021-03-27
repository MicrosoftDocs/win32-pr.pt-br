---
title: Função WaveActiveSum
description: Soma o valor da expressão em todas as pistas ativas na onda atual e a Replica para todas as pistas na onda atual.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- HLSL da função WaveActiveSum
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917783"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="32595-104">Função WaveActiveSum</span><span class="sxs-lookup"><span data-stu-id="32595-104">WaveActiveSum function</span></span>

<span data-ttu-id="32595-105">Soma o valor da expressão em todas as pistas ativas na onda atual e a Replica para todas as pistas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="32595-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="32595-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32595-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="32595-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32595-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32595-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="32595-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="32595-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="32595-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32595-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32595-110">Return value</span></span>

<span data-ttu-id="32595-111">O valor da soma.</span><span class="sxs-lookup"><span data-stu-id="32595-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32595-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="32595-112">Remarks</span></span>

<span data-ttu-id="32595-113">A ordem das operações é indefinida.</span><span class="sxs-lookup"><span data-stu-id="32595-113">The order of operations is undefined.</span></span>

<span data-ttu-id="32595-114">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="32595-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="32595-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32595-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="32595-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="32595-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32595-117">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="32595-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="32595-118">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="32595-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




