---
title: Função WaveActiveBitAnd
description: Retorna o bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- HLSL da função WaveActiveBitAnd
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008605"
---
# <a name="waveactivebitand-function"></a><span data-ttu-id="8af47-104">Função WaveActiveBitAnd</span><span class="sxs-lookup"><span data-stu-id="8af47-104">WaveActiveBitAnd function</span></span>

<span data-ttu-id="8af47-105">Retorna o bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="8af47-105">Returns the bitwise AND of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af47-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8af47-106">Syntax</span></span>


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="8af47-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8af47-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af47-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="8af47-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="8af47-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="8af47-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af47-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8af47-110">Return value</span></span>

<span data-ttu-id="8af47-111">O bit e o valor.</span><span class="sxs-lookup"><span data-stu-id="8af47-111">The bitwise AND value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af47-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8af47-112">Remarks</span></span>

<span data-ttu-id="8af47-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8af47-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="8af47-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="8af47-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af47-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="8af47-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="8af47-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="8af47-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




