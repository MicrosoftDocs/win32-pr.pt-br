---
title: Função WaveActiveAllTrue
description: Retornará true se a expressão for verdadeira em todas as pistas ativas na onda atual.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- HLSL da função WaveActiveAllTrue
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454453"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="fa01c-104">Função WaveActiveAllTrue</span><span class="sxs-lookup"><span data-stu-id="fa01c-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="fa01c-105">Retornará true se a expressão for verdadeira em todas as pistas ativas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="fa01c-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa01c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa01c-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="fa01c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa01c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa01c-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="fa01c-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="fa01c-109">A expressão booliana a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="fa01c-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa01c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa01c-110">Return value</span></span>

<span data-ttu-id="fa01c-111">True se a expressão for verdadeira em todas as pistas.</span><span class="sxs-lookup"><span data-stu-id="fa01c-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa01c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa01c-112">Remarks</span></span>

<span data-ttu-id="fa01c-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fa01c-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="fa01c-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa01c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa01c-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="fa01c-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="fa01c-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="fa01c-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




