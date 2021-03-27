---
title: Função WaveReadLaneFirst
description: Retorna o valor da expressão para a pista ativa da onda atual com o menor índice.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- HLSL da função WaveReadLaneFirst
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104967234"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="3bcda-104">Função WaveReadLaneFirst</span><span class="sxs-lookup"><span data-stu-id="3bcda-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="3bcda-105">Retorna o valor da expressão para a pista ativa da onda atual com o menor índice.</span><span class="sxs-lookup"><span data-stu-id="3bcda-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcda-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bcda-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="3bcda-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bcda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bcda-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="3bcda-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="3bcda-109">A expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="3bcda-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bcda-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bcda-110">Return value</span></span>

<span data-ttu-id="3bcda-111">O valor resultante é uniforme em toda a onda.</span><span class="sxs-lookup"><span data-stu-id="3bcda-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bcda-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bcda-112">Remarks</span></span>

<span data-ttu-id="3bcda-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3bcda-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="3bcda-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bcda-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bcda-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="3bcda-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="3bcda-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="3bcda-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




