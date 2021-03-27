---
title: Função WaveActiveAnyTrue
description: Retornará true se a expressão for verdadeira em qualquer uma das pistas ativas na onda atual.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- HLSL da função WaveActiveAnyTrue
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104988716"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="cdc75-104">Função WaveActiveAnyTrue</span><span class="sxs-lookup"><span data-stu-id="cdc75-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="cdc75-105">Retornará true se a expressão for verdadeira em qualquer uma das pistas ativas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="cdc75-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc75-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdc75-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="cdc75-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdc75-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc75-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="cdc75-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc75-109">A expressão booliana a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="cdc75-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc75-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cdc75-110">Return value</span></span>

<span data-ttu-id="cdc75-111">True se a expressão for verdadeira em qualquer pista.</span><span class="sxs-lookup"><span data-stu-id="cdc75-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc75-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdc75-112">Remarks</span></span>

<span data-ttu-id="cdc75-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cdc75-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="cdc75-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdc75-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc75-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="cdc75-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="cdc75-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="cdc75-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




