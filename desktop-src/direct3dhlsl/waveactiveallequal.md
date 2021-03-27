---
title: Função WaveActiveAllEqual
description: Retornará true se a expressão for a mesma para cada pista ativa na onda atual (e, portanto, uniforme em toda a ti).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- HLSL da função WaveActiveAllEqual
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103642974"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="bc187-104">Função WaveActiveAllEqual</span><span class="sxs-lookup"><span data-stu-id="bc187-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="bc187-105">Retornará true se a expressão for a mesma para cada pista ativa na onda atual (e, portanto, uniforme em toda a ti).</span><span class="sxs-lookup"><span data-stu-id="bc187-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc187-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc187-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="bc187-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc187-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc187-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="bc187-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="bc187-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="bc187-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc187-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc187-110">Return value</span></span>

<span data-ttu-id="bc187-111">True se a expressão for a mesma para todas as pistas ativas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="bc187-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc187-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc187-112">Remarks</span></span>

<span data-ttu-id="bc187-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bc187-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="bc187-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc187-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc187-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="bc187-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="bc187-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="bc187-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




