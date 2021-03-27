---
title: Função WaveActiveMin
description: Retorna o valor mínimo da expressão em todas as pistas ativas na onda atual, replicando-a de volta para todas as pistas ativas.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- HLSL da função WaveActiveMin
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008598"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="075eb-104">Função WaveActiveMin</span><span class="sxs-lookup"><span data-stu-id="075eb-104">WaveActiveMin function</span></span>

<span data-ttu-id="075eb-105">Retorna o valor mínimo da expressão em todas as pistas ativas na onda atual, replicando-a de volta para todas as pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="075eb-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="075eb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="075eb-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="075eb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="075eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075eb-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="075eb-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="075eb-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="075eb-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075eb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="075eb-110">Return value</span></span>

<span data-ttu-id="075eb-111">O valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="075eb-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="075eb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="075eb-112">Remarks</span></span>

<span data-ttu-id="075eb-113">A ordem das operações é indefinida.</span><span class="sxs-lookup"><span data-stu-id="075eb-113">The order of operations is undefined.</span></span>

<span data-ttu-id="075eb-114">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="075eb-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="075eb-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="075eb-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="075eb-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="075eb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075eb-117">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="075eb-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="075eb-118">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="075eb-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




