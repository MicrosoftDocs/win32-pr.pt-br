---
title: Instrução for
description: Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- HLSL de instrução for
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084167"
---
# <a name="for-statement"></a><span data-ttu-id="e7330-104">Instrução for</span><span class="sxs-lookup"><span data-stu-id="e7330-104">for Statement</span></span>

<span data-ttu-id="e7330-105">Executa iterativamente uma série de instruções, com base na avaliação da expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="e7330-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7330-106">\[*Atributo* \] para ( *inicializador; Condiciona Iterador* ) { *bloco de instruções*;}</span><span class="sxs-lookup"><span data-stu-id="e7330-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="e7330-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7330-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7330-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span><span class="sxs-lookup"><span data-stu-id="e7330-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="e7330-109">Um parâmetro opcional que controla como a instrução é compilada.</span><span class="sxs-lookup"><span data-stu-id="e7330-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="e7330-110">Quando nenhum atributo for especificado, o compilador tentará primeiro emitir uma versão revertida do loop e, se isso falhar, ou se algumas operações forem mais fáceis se o loop fosse cancelado, o voltará a uma versão não lançada do loop.</span><span class="sxs-lookup"><span data-stu-id="e7330-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="e7330-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="e7330-111">Attribute</span></span>             | <span data-ttu-id="e7330-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7330-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7330-113">não acumular (x)</span><span class="sxs-lookup"><span data-stu-id="e7330-113">unroll(x)</span></span>             | <span data-ttu-id="e7330-114">Desverta o loop até que ele pare de ser executado.</span><span class="sxs-lookup"><span data-stu-id="e7330-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="e7330-115">Opcionalmente, pode especificar o número máximo de vezes que o loop é executado.</span><span class="sxs-lookup"><span data-stu-id="e7330-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="e7330-116">Não compatível com o atributo **\[ loop \]** .</span><span class="sxs-lookup"><span data-stu-id="e7330-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e7330-117">loop</span><span class="sxs-lookup"><span data-stu-id="e7330-117">loop</span></span>                  | <span data-ttu-id="e7330-118">Gere o código que usa o controle de fluxo para executar cada iteração do loop.</span><span class="sxs-lookup"><span data-stu-id="e7330-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="e7330-119">Não compatível com o atributo **\[ unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="e7330-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e7330-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="e7330-120">fastopt</span></span>               | <span data-ttu-id="e7330-121">Reduz o tempo de compilação, mas produz otimizações menos agressivas.</span><span class="sxs-lookup"><span data-stu-id="e7330-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="e7330-122">Se você usar esse atributo, o compilador não desrolará loops.</span><span class="sxs-lookup"><span data-stu-id="e7330-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="e7330-123">Esse atributo afeta somente os destinos de modelo de sombreador que dão suporte a instruções de [quebra](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="e7330-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="e7330-124">Esse atributo está disponível no modelo do sombreador [versus \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e no [sombreador, modelo 3](dx-graphics-hlsl-sm3.md) e posterior.</span><span class="sxs-lookup"><span data-stu-id="e7330-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="e7330-125">Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e mais tarde, quando o compilador compila loops.</span><span class="sxs-lookup"><span data-stu-id="e7330-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="e7330-126">O compilador simula loops por padrão para avaliar se ele pode desroll-los.</span><span class="sxs-lookup"><span data-stu-id="e7330-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="e7330-127">Se você não quiser que o compilador desverta loops, use esse atributo para reduzir o tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="e7330-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="e7330-128">permitir \_ \_ condição UAV</span><span class="sxs-lookup"><span data-stu-id="e7330-128">allow\_uav\_condition</span></span> | <span data-ttu-id="e7330-129">Permite que uma condição de encerramento de loop de sombreador de computação seja baseada em uma leitura de UAV.</span><span class="sxs-lookup"><span data-stu-id="e7330-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="e7330-130">O loop não deve conter intrínsecos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e7330-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="e7330-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*</span><span class="sxs-lookup"><span data-stu-id="e7330-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="e7330-132">O valor inicial do contador de loops.</span><span class="sxs-lookup"><span data-stu-id="e7330-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="e7330-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*</span><span class="sxs-lookup"><span data-stu-id="e7330-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="e7330-134">Uma [expressão](dx-graphics-hlsl-expressions.md)condicional.</span><span class="sxs-lookup"><span data-stu-id="e7330-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="e7330-135">Se a expressão condicional for avaliada como true, o bloco de instrução será executado.</span><span class="sxs-lookup"><span data-stu-id="e7330-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="e7330-136">O loop termina quando a expressão é avaliada como falsa.</span><span class="sxs-lookup"><span data-stu-id="e7330-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="e7330-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Repeti*</span><span class="sxs-lookup"><span data-stu-id="e7330-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="e7330-138">Atualize o valor do contador de loop.</span><span class="sxs-lookup"><span data-stu-id="e7330-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="e7330-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*</span><span class="sxs-lookup"><span data-stu-id="e7330-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="e7330-140">Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="e7330-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7330-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7330-141">Remarks</span></span>

<span data-ttu-id="e7330-142">Os atributos **\[ desroll \]** e **\[ loop \]** são mutuamente exclusivos e gerarão erros de compilador quando ambos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="e7330-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="e7330-143">Os atributos de **\[ \_ \_ condição \]** **\[ \] fastopt** e Allow UAV serão ignorados se o **\[ canroll \]** for especificado.</span><span class="sxs-lookup"><span data-stu-id="e7330-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7330-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7330-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7330-145">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="e7330-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





