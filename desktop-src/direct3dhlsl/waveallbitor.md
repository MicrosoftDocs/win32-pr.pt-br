---
title: Função WaveActiveBitOr
description: Retorna o valor de bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- HLSL da função WaveActiveBitOr
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008599"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="d6c13-104">Função WaveActiveBitOr</span><span class="sxs-lookup"><span data-stu-id="d6c13-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="d6c13-105">Retorna o valor de bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="d6c13-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c13-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6c13-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="d6c13-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6c13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c13-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="d6c13-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c13-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="d6c13-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c13-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6c13-110">Return value</span></span>

<span data-ttu-id="d6c13-111">O valor or</span><span class="sxs-lookup"><span data-stu-id="d6c13-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c13-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6c13-112">Remarks</span></span>

<span data-ttu-id="d6c13-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d6c13-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="d6c13-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6c13-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c13-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="d6c13-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="d6c13-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="d6c13-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




