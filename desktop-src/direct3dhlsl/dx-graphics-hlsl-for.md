---
title: Instrução for
description: Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- para instrução HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cbcf06f28a327e18aa9f31b417dc1911411d0c9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119072"
---
# <a name="for-statement"></a><span data-ttu-id="66c8c-104">Instrução for</span><span class="sxs-lookup"><span data-stu-id="66c8c-104">for Statement</span></span>

<span data-ttu-id="66c8c-105">Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="66c8c-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="66c8c-106">\[*Atributo* \] para ( *Inicializador; Condicional; Iterador* ) { *Bloco de instrução*; }</span><span class="sxs-lookup"><span data-stu-id="66c8c-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="66c8c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66c8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c8c-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*</span><span class="sxs-lookup"><span data-stu-id="66c8c-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="66c8c-109">Um parâmetro opcional que controla como a instrução é compilada.</span><span class="sxs-lookup"><span data-stu-id="66c8c-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="66c8c-110">Quando nenhum atributo for especificado, o compilador tentará primeiro emitir uma versão rolada do loop e, se isso falhar, ou se algumas operações serão mais fáceis se o loop tiver sido desenrolado, retornará para uma versão não listada do loop.</span><span class="sxs-lookup"><span data-stu-id="66c8c-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="66c8c-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="66c8c-111">Attribute</span></span>             | <span data-ttu-id="66c8c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="66c8c-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c8c-113">unroll(x)</span><span class="sxs-lookup"><span data-stu-id="66c8c-113">unroll(x)</span></span>             | <span data-ttu-id="66c8c-114">Unroll the loop until it stops executing.</span><span class="sxs-lookup"><span data-stu-id="66c8c-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="66c8c-115">Opcionalmente, pode especificar o número máximo de vezes que o loop deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="66c8c-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="66c8c-116">Não compatível com o **\[ atributo loop. \]**</span><span class="sxs-lookup"><span data-stu-id="66c8c-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="66c8c-117">loop</span><span class="sxs-lookup"><span data-stu-id="66c8c-117">loop</span></span>                  | <span data-ttu-id="66c8c-118">Gere o código que usa o controle de fluxo para executar cada iteração do loop.</span><span class="sxs-lookup"><span data-stu-id="66c8c-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="66c8c-119">Não compatível com o **\[ atributo unroll. \]**</span><span class="sxs-lookup"><span data-stu-id="66c8c-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="66c8c-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="66c8c-120">fastopt</span></span>               | <span data-ttu-id="66c8c-121">Reduz o tempo de compilação, mas produz otimizações menos agressivas.</span><span class="sxs-lookup"><span data-stu-id="66c8c-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="66c8c-122">Se você usar esse atributo, o compilador não desenrola os loops.</span><span class="sxs-lookup"><span data-stu-id="66c8c-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="66c8c-123">Esse atributo afeta apenas destinos de modelo de sombreador que suportam instruções [de quebra.](dx-graphics-hlsl-break.md)</span><span class="sxs-lookup"><span data-stu-id="66c8c-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="66c8c-124">Esse atributo está disponível no modelo de sombreador [ \_ versus 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) e posterior.</span><span class="sxs-lookup"><span data-stu-id="66c8c-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="66c8c-125">Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e posterior quando o compilador compila loops.</span><span class="sxs-lookup"><span data-stu-id="66c8c-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="66c8c-126">O compilador simula loops por padrão para avaliar se ele pode unroll-los.</span><span class="sxs-lookup"><span data-stu-id="66c8c-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="66c8c-127">Se você não quiser que o compilador unroll loops, use esse atributo para reduzir o tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="66c8c-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="66c8c-128">permitir \_ condição \_ uav</span><span class="sxs-lookup"><span data-stu-id="66c8c-128">allow\_uav\_condition</span></span> | <span data-ttu-id="66c8c-129">Permite que uma condição de encerramento de loop do sombreador de computação seja baseada em uma leitura UAV.</span><span class="sxs-lookup"><span data-stu-id="66c8c-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="66c8c-130">O loop não deve conter intrínsecos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="66c8c-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="66c8c-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*</span><span class="sxs-lookup"><span data-stu-id="66c8c-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="66c8c-132">O valor inicial do contador de loops.</span><span class="sxs-lookup"><span data-stu-id="66c8c-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="66c8c-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*</span><span class="sxs-lookup"><span data-stu-id="66c8c-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="66c8c-134">Uma expressão [condicional](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="66c8c-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="66c8c-135">Se a expressão condicional for avaliada como true, o bloco de instrução será executado.</span><span class="sxs-lookup"><span data-stu-id="66c8c-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="66c8c-136">O loop termina quando a expressão é avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="66c8c-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="66c8c-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterador*</span><span class="sxs-lookup"><span data-stu-id="66c8c-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="66c8c-138">Atualize o valor do contador de loop.</span><span class="sxs-lookup"><span data-stu-id="66c8c-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="66c8c-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*</span><span class="sxs-lookup"><span data-stu-id="66c8c-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="66c8c-140">Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="66c8c-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66c8c-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="66c8c-141">Remarks</span></span>

<span data-ttu-id="66c8c-142">Os **\[ atributos \] unroll** **\[ e loop \]** são mutuamente exclusivos e gerarão erros do compilador quando ambos são especificados.</span><span class="sxs-lookup"><span data-stu-id="66c8c-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="66c8c-143">Os **\[ atributos \] de condição fastopt** e **\[ \_ allow uav \_ \]** serão ignorados se **\[ o unroll \]** for especificado.</span><span class="sxs-lookup"><span data-stu-id="66c8c-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="66c8c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="66c8c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c8c-145">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="66c8c-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





