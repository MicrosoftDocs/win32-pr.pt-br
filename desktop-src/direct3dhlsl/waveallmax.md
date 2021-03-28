---
title: Função WaveActiveMax
description: Retorna o valor máximo da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- HLSL da função WaveActiveMax
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2020
ms.locfileid: "104368979"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="c6440-104">Função WaveActiveMax</span><span class="sxs-lookup"><span data-stu-id="c6440-104">WaveActiveMax function</span></span>

<span data-ttu-id="c6440-105">Retorna o valor máximo da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="c6440-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6440-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6440-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="c6440-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6440-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6440-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="c6440-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="c6440-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="c6440-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6440-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6440-110">Return value</span></span>

<span data-ttu-id="c6440-111">O valor máximo.</span><span class="sxs-lookup"><span data-stu-id="c6440-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6440-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6440-112">Remarks</span></span>

<span data-ttu-id="c6440-113">A ordem das operações é indefinida.</span><span class="sxs-lookup"><span data-stu-id="c6440-113">The order of operations is undefined.</span></span>

<span data-ttu-id="c6440-114">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c6440-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="c6440-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6440-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="c6440-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6440-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6440-117">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="c6440-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="c6440-118">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="c6440-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




