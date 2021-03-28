---
title: 'Função WavePrefixSum '
description: Retorna a soma de todos os valores nas pistas ativas com índices menores do que este.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- HLSL da função WavePrefixSum
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/31/2021
ms.locfileid: "104968258"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="c62cc-104">Função WavePrefixSum </span><span class="sxs-lookup"><span data-stu-id="c62cc-104">WavePrefixSum function</span></span>

<span data-ttu-id="c62cc-105">Retorna a soma de todos os valores nas pistas ativas com índices menores do que este.</span><span class="sxs-lookup"><span data-stu-id="c62cc-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62cc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c62cc-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="c62cc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c62cc-107">Parameters</span></span>

<span data-ttu-id="c62cc-108">*value*</span><span class="sxs-lookup"><span data-stu-id="c62cc-108">*value*</span></span> 

<span data-ttu-id="c62cc-109">O valor a ser somado.</span><span class="sxs-lookup"><span data-stu-id="c62cc-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="c62cc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c62cc-110">Return value</span></span>

<span data-ttu-id="c62cc-111">A soma dos valores.</span><span class="sxs-lookup"><span data-stu-id="c62cc-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62cc-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c62cc-112">Remarks</span></span>

<span data-ttu-id="c62cc-113">A ordem das operações nessa rotina não pode ser garantida.</span><span class="sxs-lookup"><span data-stu-id="c62cc-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="c62cc-114">Portanto, efetivamente, o \[ \] sinalizador preciso é ignorado dentro dele.</span><span class="sxs-lookup"><span data-stu-id="c62cc-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="c62cc-115">Uma soma de sufixo pode ser calculada adicionando a soma de prefixo ao valor da raia atual.</span><span class="sxs-lookup"><span data-stu-id="c62cc-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="c62cc-116">Observe que a pista ativa com o índice mais baixo sempre receberá um 0 para sua soma de prefixo.</span><span class="sxs-lookup"><span data-stu-id="c62cc-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="c62cc-117">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c62cc-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="c62cc-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c62cc-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="c62cc-119">Em um computador com um tamanho de onda de 8 e todas as pistas ativas, exceto pistas 0 e 4, os valores a seguir seriam retornados de WavePrefixSum.</span><span class="sxs-lookup"><span data-stu-id="c62cc-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="c62cc-120">índice de Lane</span><span class="sxs-lookup"><span data-stu-id="c62cc-120">lane index</span></span> | <span data-ttu-id="c62cc-121">status</span><span class="sxs-lookup"><span data-stu-id="c62cc-121">status</span></span>   | <span data-ttu-id="c62cc-122">prefixSum</span><span class="sxs-lookup"><span data-stu-id="c62cc-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="c62cc-123">0</span><span class="sxs-lookup"><span data-stu-id="c62cc-123">0</span></span>          | <span data-ttu-id="c62cc-124">inativos</span><span class="sxs-lookup"><span data-stu-id="c62cc-124">inactive</span></span> | <span data-ttu-id="c62cc-125">N/D</span><span class="sxs-lookup"><span data-stu-id="c62cc-125">n/a</span></span>           |
| <span data-ttu-id="c62cc-126">1</span><span class="sxs-lookup"><span data-stu-id="c62cc-126">1</span></span>          | <span data-ttu-id="c62cc-127">ativo</span><span class="sxs-lookup"><span data-stu-id="c62cc-127">active</span></span>   | <span data-ttu-id="c62cc-128">= 0</span><span class="sxs-lookup"><span data-stu-id="c62cc-128">= 0</span></span>           |
| <span data-ttu-id="c62cc-129">2</span><span class="sxs-lookup"><span data-stu-id="c62cc-129">2</span></span>          | <span data-ttu-id="c62cc-130">ativo</span><span class="sxs-lookup"><span data-stu-id="c62cc-130">active</span></span>   | <span data-ttu-id="c62cc-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="c62cc-131">= 0+2</span></span>         |
| <span data-ttu-id="c62cc-132">3</span><span class="sxs-lookup"><span data-stu-id="c62cc-132">3</span></span>          | <span data-ttu-id="c62cc-133">ativo</span><span class="sxs-lookup"><span data-stu-id="c62cc-133">active</span></span>   | <span data-ttu-id="c62cc-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="c62cc-134">= 0+2+2</span></span>       |
| <span data-ttu-id="c62cc-135">4</span><span class="sxs-lookup"><span data-stu-id="c62cc-135">4</span></span>          | <span data-ttu-id="c62cc-136">inativos</span><span class="sxs-lookup"><span data-stu-id="c62cc-136">inactive</span></span> | <span data-ttu-id="c62cc-137">N/D</span><span class="sxs-lookup"><span data-stu-id="c62cc-137">n/a</span></span>           |
| <span data-ttu-id="c62cc-138">5</span><span class="sxs-lookup"><span data-stu-id="c62cc-138">5</span></span>          | <span data-ttu-id="c62cc-139">ativo</span><span class="sxs-lookup"><span data-stu-id="c62cc-139">active</span></span>   | <span data-ttu-id="c62cc-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="c62cc-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="c62cc-141">6</span><span class="sxs-lookup"><span data-stu-id="c62cc-141">6</span></span>          | <span data-ttu-id="c62cc-142">ativo</span><span class="sxs-lookup"><span data-stu-id="c62cc-142">active</span></span>   | <span data-ttu-id="c62cc-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="c62cc-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="c62cc-144">7</span><span class="sxs-lookup"><span data-stu-id="c62cc-144">7</span></span>          | <span data-ttu-id="c62cc-145">ativo</span><span class="sxs-lookup"><span data-stu-id="c62cc-145">active</span></span>   | <span data-ttu-id="c62cc-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="c62cc-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="c62cc-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c62cc-147">See also</span></span>

[<span data-ttu-id="c62cc-148">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="c62cc-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="c62cc-149">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="c62cc-149">Shader Model 6</span></span>](shader-model-6-0.md)
