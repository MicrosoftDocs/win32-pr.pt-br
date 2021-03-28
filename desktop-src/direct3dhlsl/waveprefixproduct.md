---
title: 'Função WavePrefixProduct '
description: Retorna o produto de todos os valores nas pistas ativas nesta onda com índices menores que esta raia.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- HLSL da função WavePrefixProduct
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366923"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="75704-104">Função WavePrefixProduct </span><span class="sxs-lookup"><span data-stu-id="75704-104">WavePrefixProduct function</span></span>

<span data-ttu-id="75704-105">Retorna o produto de todos os valores nas pistas ativas nesta onda com índices menores que esta raia.</span><span class="sxs-lookup"><span data-stu-id="75704-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="75704-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75704-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="75704-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75704-107">Parameters</span></span>

<span data-ttu-id="75704-108">*value*</span><span class="sxs-lookup"><span data-stu-id="75704-108">*value*</span></span> 

<span data-ttu-id="75704-109">O valor a ser multiplicado.</span><span class="sxs-lookup"><span data-stu-id="75704-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="75704-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75704-110">Return value</span></span>

<span data-ttu-id="75704-111">O produto de todos os valores.</span><span class="sxs-lookup"><span data-stu-id="75704-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="75704-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="75704-112">Remarks</span></span>

<span data-ttu-id="75704-113">A ordem das operações nessa rotina não pode ser garantida.</span><span class="sxs-lookup"><span data-stu-id="75704-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="75704-114">Portanto, efetivamente, o \[ \] sinalizador preciso é ignorado dentro dele.</span><span class="sxs-lookup"><span data-stu-id="75704-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="75704-115">Um produto de sufixo pode ser calculado multiplicando o prefixo do produto pelo valor da raia atual.</span><span class="sxs-lookup"><span data-stu-id="75704-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="75704-116">Observe que a pista ativa com o índice mais baixo sempre receberá um 1 para seu prefixo de produto.</span><span class="sxs-lookup"><span data-stu-id="75704-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="75704-117">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="75704-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="75704-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75704-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="75704-119">Em um computador com um tamanho de onda de 8 e todas as pistas ativas, exceto pistas 0 e 4, os valores a seguir seriam retornados de WavePrefixProduct.</span><span class="sxs-lookup"><span data-stu-id="75704-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="75704-120">índice de Lane</span><span class="sxs-lookup"><span data-stu-id="75704-120">lane index</span></span> | <span data-ttu-id="75704-121">status</span><span class="sxs-lookup"><span data-stu-id="75704-121">status</span></span>   | <span data-ttu-id="75704-122">prefixProduct</span><span class="sxs-lookup"><span data-stu-id="75704-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="75704-123">0</span><span class="sxs-lookup"><span data-stu-id="75704-123">0</span></span>          | <span data-ttu-id="75704-124">inativos</span><span class="sxs-lookup"><span data-stu-id="75704-124">inactive</span></span> | <span data-ttu-id="75704-125">N/D</span><span class="sxs-lookup"><span data-stu-id="75704-125">n/a</span></span>           |
| <span data-ttu-id="75704-126">1</span><span class="sxs-lookup"><span data-stu-id="75704-126">1</span></span>          | <span data-ttu-id="75704-127">ativo</span><span class="sxs-lookup"><span data-stu-id="75704-127">active</span></span>   | <span data-ttu-id="75704-128">= 1</span><span class="sxs-lookup"><span data-stu-id="75704-128">= 1</span></span>           |
| <span data-ttu-id="75704-129">2</span><span class="sxs-lookup"><span data-stu-id="75704-129">2</span></span>          | <span data-ttu-id="75704-130">ativo</span><span class="sxs-lookup"><span data-stu-id="75704-130">active</span></span>   | <span data-ttu-id="75704-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="75704-131">= 1\*2</span></span>        |
| <span data-ttu-id="75704-132">3</span><span class="sxs-lookup"><span data-stu-id="75704-132">3</span></span>          | <span data-ttu-id="75704-133">ativo</span><span class="sxs-lookup"><span data-stu-id="75704-133">active</span></span>   | <span data-ttu-id="75704-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="75704-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="75704-135">4</span><span class="sxs-lookup"><span data-stu-id="75704-135">4</span></span>          | <span data-ttu-id="75704-136">inativos</span><span class="sxs-lookup"><span data-stu-id="75704-136">inactive</span></span> | <span data-ttu-id="75704-137">N/D</span><span class="sxs-lookup"><span data-stu-id="75704-137">n/a</span></span>           |
| <span data-ttu-id="75704-138">5</span><span class="sxs-lookup"><span data-stu-id="75704-138">5</span></span>          | <span data-ttu-id="75704-139">ativo</span><span class="sxs-lookup"><span data-stu-id="75704-139">active</span></span>   | <span data-ttu-id="75704-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="75704-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="75704-141">6</span><span class="sxs-lookup"><span data-stu-id="75704-141">6</span></span>          | <span data-ttu-id="75704-142">ativo</span><span class="sxs-lookup"><span data-stu-id="75704-142">active</span></span>   | <span data-ttu-id="75704-143">= 1 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="75704-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="75704-144">7</span><span class="sxs-lookup"><span data-stu-id="75704-144">7</span></span>          | <span data-ttu-id="75704-145">ativo</span><span class="sxs-lookup"><span data-stu-id="75704-145">active</span></span>   | <span data-ttu-id="75704-146">= 1 \* 2 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="75704-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="75704-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="75704-147">See also</span></span>

[<span data-ttu-id="75704-148">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="75704-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="75704-149">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="75704-149">Shader Model 6</span></span>](shader-model-6-0.md)
