---
title: Instrução do (Ocidl. h)
description: Execute uma série de instruções continuamente até que a expressão condicional falhe.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- HLSL da instrução
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172991"
---
# <a name="do-statement"></a><span data-ttu-id="a5d0c-104">Instrução do</span><span class="sxs-lookup"><span data-stu-id="a5d0c-104">do Statement</span></span>

<span data-ttu-id="a5d0c-105">Execute uma série de instruções continuamente até que a expressão condicional falhe.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-105">Execute a series of statements continuously until the conditional expression fails.</span></span>



|                                                                     |
|---------------------------------------------------------------------|
| <span data-ttu-id="a5d0c-106">\[*Atributo* \] { *Statement Block*;} while ( *condicional* );</span><span class="sxs-lookup"><span data-stu-id="a5d0c-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a5d0c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5d0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d0c-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span><span class="sxs-lookup"><span data-stu-id="a5d0c-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="a5d0c-109">Um parâmetro opcional que controla como a instrução é compilada.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="a5d0c-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="a5d0c-110">Attribute</span></span> | <span data-ttu-id="a5d0c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5d0c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d0c-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="a5d0c-112">fastopt</span></span>   | <span data-ttu-id="a5d0c-113">Reduz o tempo de compilação, mas produz otimizações menos agressivas.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="a5d0c-114">Se você usar esse atributo, o compilador não desrolará loops.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="a5d0c-115">Esse atributo afeta somente os destinos de modelo de sombreador que dão suporte a instruções de [quebra](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d0c-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="a5d0c-116">Esse atributo está disponível no modelo do sombreador [versus \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) e no [sombreador, modelo 3](dx-graphics-hlsl-sm3.md) e posterior.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="a5d0c-117">Ele é particularmente útil no [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e mais tarde, quando o compilador compila loops.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="a5d0c-118">O compilador simula loops por padrão para avaliar se ele pode desroll-los.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="a5d0c-119">Se você não quiser que o compilador desverta loops, use esse atributo para reduzir o tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a5d0c-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*</span><span class="sxs-lookup"><span data-stu-id="a5d0c-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="a5d0c-121">Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="a5d0c-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5d0c-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*</span><span class="sxs-lookup"><span data-stu-id="a5d0c-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="a5d0c-123">Uma [expressão](dx-graphics-hlsl-expressions.md)condicional.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="a5d0c-124">O bloco de instrução é executado antes da expressão ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="a5d0c-125">O loop é encerrado quando a expressão é avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="a5d0c-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5d0c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d0c-126">Requirements</span></span>



| <span data-ttu-id="a5d0c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d0c-127">Requirement</span></span> | <span data-ttu-id="a5d0c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a5d0c-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d0c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5d0c-129">Header</span></span><br/> | <dl> <span data-ttu-id="a5d0c-130"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d0c-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d0c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5d0c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d0c-132">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="a5d0c-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





