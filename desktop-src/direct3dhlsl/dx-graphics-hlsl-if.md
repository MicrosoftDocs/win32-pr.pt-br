---
title: Instrução if
description: Executar condicionalmente uma série de instruções, com base na avaliação da expressão condicional.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Instrução If HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104007046"
---
# <a name="if-statement"></a><span data-ttu-id="31036-104">Instrução if</span><span class="sxs-lookup"><span data-stu-id="31036-104">if Statement</span></span>

<span data-ttu-id="31036-105">Executar condicionalmente uma série de instruções, com base na avaliação da expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="31036-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                               |
|---------------------------------------------------------------|
| <span data-ttu-id="31036-106">\[*Atributo* \] If ( *condicional* ) { *bloco de instruções*;}</span><span class="sxs-lookup"><span data-stu-id="31036-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="31036-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31036-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31036-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span><span class="sxs-lookup"><span data-stu-id="31036-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="31036-109">Um parâmetro opcional que controla como a instrução é compilada.</span><span class="sxs-lookup"><span data-stu-id="31036-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31036-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="31036-110">Attribute</span></span></th>
<th><span data-ttu-id="31036-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="31036-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31036-112">branch</span><span class="sxs-lookup"><span data-stu-id="31036-112">branch</span></span></td>
<td><span data-ttu-id="31036-113">Avalie apenas um lado da instrução If dependendo da condição fornecida.</span><span class="sxs-lookup"><span data-stu-id="31036-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="31036-114">Quando você usa o modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> ou o <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que usa a ramificação dinâmica, você consome recursos.</span><span class="sxs-lookup"><span data-stu-id="31036-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="31036-115">Portanto, se você usar a ramificação dinâmica de forma excessiva ao direcionar esses perfis, poderá receber erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="31036-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31036-116">mesclar</span><span class="sxs-lookup"><span data-stu-id="31036-116">flatten</span></span></td>
<td><span data-ttu-id="31036-117">Avalie ambos os lados da instrução If e escolha entre os dois valores resultantes.</span><span class="sxs-lookup"><span data-stu-id="31036-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="31036-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condiciona*</span><span class="sxs-lookup"><span data-stu-id="31036-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="31036-119">Uma [expressão](dx-graphics-hlsl-expressions.md)condicional.</span><span class="sxs-lookup"><span data-stu-id="31036-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="31036-120">A expressão é avaliada e, se for true, o bloco de instrução será executado.</span><span class="sxs-lookup"><span data-stu-id="31036-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="31036-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloco de instrução*</span><span class="sxs-lookup"><span data-stu-id="31036-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="31036-122">Uma ou mais [instruções HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="31036-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31036-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="31036-123">Remarks</span></span>

<span data-ttu-id="31036-124">Quando o compilador usa o método Branch para compilar uma instrução If, ele gerará um código que avaliará apenas um lado da instrução If dependendo da condição fornecida.</span><span class="sxs-lookup"><span data-stu-id="31036-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="31036-125">Por exemplo, na instrução If:</span><span class="sxs-lookup"><span data-stu-id="31036-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="31036-126">A instrução **If** tem um bloco de else implícito, que é equivalente a x = x.</span><span class="sxs-lookup"><span data-stu-id="31036-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="31036-127">Como dissemos ao compilador para usar o método Branch com o atributo Branch anterior, o código compilado avaliará x e executará apenas o lado que deve ser executado; se x for zero, ele executará o lado **mais** e, se for diferente de zero, ele executará o lado de **seguida** .</span><span class="sxs-lookup"><span data-stu-id="31036-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="31036-128">Por outro lado, se o atributo de **achatamento** for usado, o código compilado avaliará ambos os lados da instrução **If** e escolherá entre os dois valores resultantes usando o valor original de x.</span><span class="sxs-lookup"><span data-stu-id="31036-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="31036-129">Aqui está um exemplo de uso do atributo achatar:</span><span class="sxs-lookup"><span data-stu-id="31036-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="31036-130">Há certos casos em que usar os atributos Branch ou achatamento pode gerar um erro de compilação.</span><span class="sxs-lookup"><span data-stu-id="31036-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="31036-131">O atributo Branch poderá falhar se qualquer lado da instrução If contiver uma função de gradiente, como [**tex2D**](dx-graphics-hlsl-tex2d.md).</span><span class="sxs-lookup"><span data-stu-id="31036-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="31036-132">O atributo achata pode falhar se qualquer lado da instrução If contiver uma instrução Stream Append ou qualquer outra instrução que tenha efeitos colaterais.</span><span class="sxs-lookup"><span data-stu-id="31036-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="31036-133">Uma instrução **If** também pode usar um bloco opcional ELSE.</span><span class="sxs-lookup"><span data-stu-id="31036-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="31036-134">Se a expressão **If** for true, o código no bloco de instrução associado à instrução If será processado.</span><span class="sxs-lookup"><span data-stu-id="31036-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="31036-135">Caso contrário, o bloco de instrução associado ao bloco opcional else será processado.</span><span class="sxs-lookup"><span data-stu-id="31036-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="31036-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="31036-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31036-137">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="31036-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





