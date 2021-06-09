---
title: Instrução While
description: Executa um bloco de instruções até que a expressão condicional falhe.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- Instrução while HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826669"
---
# <a name="while-statement"></a><span data-ttu-id="d72f4-104">Instrução While</span><span class="sxs-lookup"><span data-stu-id="d72f4-104">while Statement</span></span>

<span data-ttu-id="d72f4-105">Executa um bloco de instruções até que a expressão condicional falhe.</span><span class="sxs-lookup"><span data-stu-id="d72f4-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="d72f4-106">\[*Atributo* \] While ( *condicional* ) { *bloco de instruções*;}</span><span class="sxs-lookup"><span data-stu-id="d72f4-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="d72f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d72f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72f4-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span><span class="sxs-lookup"><span data-stu-id="d72f4-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="d72f4-109">Um parâmetro opcional que controla como a instrução é compilada.</span><span class="sxs-lookup"><span data-stu-id="d72f4-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="d72f4-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="d72f4-110">Attribute</span></span>             | <span data-ttu-id="d72f4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d72f4-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d72f4-112">não acumular (x)</span><span class="sxs-lookup"><span data-stu-id="d72f4-112">unroll(x)</span></span>             | <span data-ttu-id="d72f4-113">Desverta o loop até que ele pare de ser executado.</span><span class="sxs-lookup"><span data-stu-id="d72f4-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="d72f4-114">Opcionalmente, você pode especificar o número máximo de vezes que o loop pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="d72f4-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d72f4-115">loop</span><span class="sxs-lookup"><span data-stu-id="d72f4-115">loop</span></span>                  | <span data-ttu-id="d72f4-116">Usar instruções de controle de fluxo no sombreador compilado; Não desverta o loop.</span><span class="sxs-lookup"><span data-stu-id="d72f4-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d72f4-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="d72f4-117">fastopt</span></span>               | <span data-ttu-id="d72f4-118">Reduz o tempo de compilação, mas produz otimizações menos agressivas.</span><span class="sxs-lookup"><span data-stu-id="d72f4-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="d72f4-119">Se você usar esse atributo, o compilador não desrolará loops.</span><span class="sxs-lookup"><span data-stu-id="d72f4-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="d72f4-120">Esse atributo afeta somente os destinos de modelo de sombreador que dão suporte a instruções de [quebra](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="d72f4-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="d72f4-121">Esse atributo está disponível no modelo do sombreador [versus \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e no [sombreador, modelo 3](dx-graphics-hlsl-sm3.md) e posterior.</span><span class="sxs-lookup"><span data-stu-id="d72f4-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="d72f4-122">Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e mais tarde, quando o compilador compila loops.</span><span class="sxs-lookup"><span data-stu-id="d72f4-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="d72f4-123">O compilador simula loops por padrão para avaliar se ele pode desroll-los.</span><span class="sxs-lookup"><span data-stu-id="d72f4-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="d72f4-124">Se você não quiser que o compilador desverta loops, use esse atributo para reduzir o tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="d72f4-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="d72f4-125">permitir \_ \_ condição UAV</span><span class="sxs-lookup"><span data-stu-id="d72f4-125">allow\_uav\_condition</span></span> | <span data-ttu-id="d72f4-126">Permite que uma condição de encerramento de loop de sombreador de computação seja baseada em uma leitura de UAV.</span><span class="sxs-lookup"><span data-stu-id="d72f4-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="d72f4-127">O loop não deve conter intrínsecos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d72f4-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d72f4-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*</span><span class="sxs-lookup"><span data-stu-id="d72f4-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="d72f4-129">Uma [expressão](dx-graphics-hlsl-expressions.md)condicional.</span><span class="sxs-lookup"><span data-stu-id="d72f4-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="d72f4-130">Se a expressão for avaliada como true, o bloco de instrução será executado.</span><span class="sxs-lookup"><span data-stu-id="d72f4-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="d72f4-131">O loop termina quando a expressão é avaliada como falsa.</span><span class="sxs-lookup"><span data-stu-id="d72f4-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="d72f4-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*</span><span class="sxs-lookup"><span data-stu-id="d72f4-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="d72f4-133">Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="d72f4-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d72f4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d72f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72f4-135">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="d72f4-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





