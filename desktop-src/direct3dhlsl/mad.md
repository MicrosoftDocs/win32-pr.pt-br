---
title: Função mad
description: Executa uma operação aritmética de multiplicar/adicionar em três valores.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- HLSL da função Mad
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453787"
---
# <a name="mad-function"></a><span data-ttu-id="900e7-104">Função mad</span><span class="sxs-lookup"><span data-stu-id="900e7-104">mad function</span></span>

<span data-ttu-id="900e7-105">Executa uma operação aritmética de multiplicar/adicionar em três valores.</span><span class="sxs-lookup"><span data-stu-id="900e7-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="900e7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="900e7-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="900e7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="900e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="900e7-108">*mvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="900e7-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e7-109">Tipo: **numérico**</span><span class="sxs-lookup"><span data-stu-id="900e7-109">Type: **numeric**</span></span>

<span data-ttu-id="900e7-110">O valor de multiplicação.</span><span class="sxs-lookup"><span data-stu-id="900e7-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="900e7-111">*aValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="900e7-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e7-112">Tipo: **numérico**</span><span class="sxs-lookup"><span data-stu-id="900e7-112">Type: **numeric**</span></span>

<span data-ttu-id="900e7-113">O primeiro valor de adição.</span><span class="sxs-lookup"><span data-stu-id="900e7-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="900e7-114">*bValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="900e7-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="900e7-115">Tipo: **numérico**</span><span class="sxs-lookup"><span data-stu-id="900e7-115">Type: **numeric**</span></span>

<span data-ttu-id="900e7-116">O segundo valor de adição.</span><span class="sxs-lookup"><span data-stu-id="900e7-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="900e7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="900e7-117">Return value</span></span>

<span data-ttu-id="900e7-118">Tipo: **numérico**</span><span class="sxs-lookup"><span data-stu-id="900e7-118">Type: **numeric**</span></span>

<span data-ttu-id="900e7-119">O resultado de *mvalue* \* *aValue*  +  *bValue*.</span><span class="sxs-lookup"><span data-stu-id="900e7-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="900e7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="900e7-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="900e7-121">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="900e7-121">Minimum Shader Model</span></span>

<span data-ttu-id="900e7-122">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="900e7-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="900e7-123">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="900e7-123">Shader Model</span></span>                                                                | <span data-ttu-id="900e7-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="900e7-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="900e7-125">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="900e7-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="900e7-126">sim</span><span class="sxs-lookup"><span data-stu-id="900e7-126">yes</span></span>       |



 

<span data-ttu-id="900e7-127">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="900e7-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="900e7-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="900e7-128">Vertex</span></span> | <span data-ttu-id="900e7-129">Envoltória</span><span class="sxs-lookup"><span data-stu-id="900e7-129">Hull</span></span> | <span data-ttu-id="900e7-130">Domínio</span><span class="sxs-lookup"><span data-stu-id="900e7-130">Domain</span></span> | <span data-ttu-id="900e7-131">Geometria</span><span class="sxs-lookup"><span data-stu-id="900e7-131">Geometry</span></span> | <span data-ttu-id="900e7-132">16x16</span><span class="sxs-lookup"><span data-stu-id="900e7-132">Pixel</span></span> | <span data-ttu-id="900e7-133">Computação</span><span class="sxs-lookup"><span data-stu-id="900e7-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="900e7-134">x</span><span class="sxs-lookup"><span data-stu-id="900e7-134">x</span></span>      | <span data-ttu-id="900e7-135">x</span><span class="sxs-lookup"><span data-stu-id="900e7-135">x</span></span>    | <span data-ttu-id="900e7-136">x</span><span class="sxs-lookup"><span data-stu-id="900e7-136">x</span></span>      | <span data-ttu-id="900e7-137">x</span><span class="sxs-lookup"><span data-stu-id="900e7-137">x</span></span>        | <span data-ttu-id="900e7-138">x</span><span class="sxs-lookup"><span data-stu-id="900e7-138">x</span></span>     | <span data-ttu-id="900e7-139">x</span><span class="sxs-lookup"><span data-stu-id="900e7-139">x</span></span>       |



 

<span data-ttu-id="900e7-140">Os autores de sombreador podem usar o **Mad** instrinsic para direcionar explicitamente a instrução de hardware **Mad** na saída do sombreador compilado, que é particularmente útil com sombreadores que marcam os resultados com a palavra-chave [precisa](dx-graphics-hlsl-appendix-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="900e7-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="900e7-141">A instrução **Mad** pode ser implementada no hardware como "fundido", que oferece maior precisão do que a implementação de uma instrução **Mul** seguida por uma instrução **Add** , ou como uma adição de **Mul**  +  .</span><span class="sxs-lookup"><span data-stu-id="900e7-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="900e7-142">Se os autores de sombreador usarem o **Mad** instrinsic para calcular um resultado de que o sombreador está marcado como preciso, eles indicarão ao hardware para usar qualquer implementação válida da instrução **Mad** (com fusível ou não), desde que a implementação seja consistente para todos os usos dessa **Mad** intrínseca em qualquer sombreador no hardware.</span><span class="sxs-lookup"><span data-stu-id="900e7-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="900e7-143">Os sombreadores podem aproveitar as possíveis melhorias de desempenho usando uma instrução **Mad** nativa (versus **Mul**  +  **Add**) em algum hardware.</span><span class="sxs-lookup"><span data-stu-id="900e7-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="900e7-144">O resultado da execução de uma instrução de hardware **Mad** nativo pode ou não ser diferente de executar um **Mul** seguido por um **Add**.</span><span class="sxs-lookup"><span data-stu-id="900e7-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="900e7-145">No entanto, seja qual for o resultado, o resultado deve ser consistente para que a mesma operação ocorra em vários sombreadores ou partes diferentes de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="900e7-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="900e7-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="900e7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="900e7-147">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="900e7-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="900e7-148">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="900e7-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




