---
title: Função WaveActiveBitXor
description: Retorna o XOR bit a bit de todos os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- HLSL da função WaveActiveBitXor
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008597"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="855ba-104">Função WaveActiveBitXor</span><span class="sxs-lookup"><span data-stu-id="855ba-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="855ba-105">Retorna o XOR bit a bit de todos os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="855ba-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="855ba-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="855ba-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="855ba-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="855ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="855ba-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="855ba-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="855ba-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="855ba-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="855ba-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="855ba-110">Return value</span></span>

<span data-ttu-id="855ba-111">O valor de XOR de bits.</span><span class="sxs-lookup"><span data-stu-id="855ba-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="855ba-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="855ba-112">Remarks</span></span>

<span data-ttu-id="855ba-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="855ba-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="855ba-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="855ba-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="855ba-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="855ba-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="855ba-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="855ba-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




