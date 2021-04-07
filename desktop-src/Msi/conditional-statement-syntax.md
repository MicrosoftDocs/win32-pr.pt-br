---
description: Esta seção descreve a sintaxe de instruções condicionais usadas pela função MsiEvaluateCondition e as tabelas de sequência de ação. Para obter mais informações, consulte exemplos de sintaxe de instrução condicional.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintaxe de instrução condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828034"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="19a4e-104">Sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="19a4e-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="19a4e-105">Esta seção descreve a sintaxe de instruções condicionais usadas pela função [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) e as [tabelas de sequência](using-a-sequence-table.md)de ação.</span><span class="sxs-lookup"><span data-stu-id="19a4e-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="19a4e-106">Para obter mais informações, consulte [exemplos de sintaxe de instrução condicional](examples-of-conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="19a4e-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="19a4e-107">Resumo da sintaxe da instrução condicional</span><span class="sxs-lookup"><span data-stu-id="19a4e-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="19a4e-108">Essa tabela e a lista a seguir resumem a sintaxe a ser usada em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="19a4e-109">Item</span><span class="sxs-lookup"><span data-stu-id="19a4e-109">Item</span></span>                | <span data-ttu-id="19a4e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="19a4e-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a4e-111">value</span><span class="sxs-lookup"><span data-stu-id="19a4e-111">value</span></span>               | <span data-ttu-id="19a4e-112">\|inteiro literal de símbolo \|</span><span class="sxs-lookup"><span data-stu-id="19a4e-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="19a4e-113">operador de comparação</span><span class="sxs-lookup"><span data-stu-id="19a4e-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="19a4e-114">Termo</span><span class="sxs-lookup"><span data-stu-id="19a4e-114">term</span></span>                | <span data-ttu-id="19a4e-115">valor \| do valor Comparison-operador value \| (expressão)\|</span><span class="sxs-lookup"><span data-stu-id="19a4e-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="19a4e-116">Fator booliano</span><span class="sxs-lookup"><span data-stu-id="19a4e-116">Boolean-factor</span></span>      | <span data-ttu-id="19a4e-117">termo \| **não** termo</span><span class="sxs-lookup"><span data-stu-id="19a4e-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="19a4e-118">Termo booliano</span><span class="sxs-lookup"><span data-stu-id="19a4e-118">Boolean-term</span></span>        | <span data-ttu-id="19a4e-119">\|Booliano booleano-fator **e** termo</span><span class="sxs-lookup"><span data-stu-id="19a4e-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="19a4e-120">expressão</span><span class="sxs-lookup"><span data-stu-id="19a4e-120">expression</span></span>          | <span data-ttu-id="19a4e-121">Valor booliano do termo booliano \| **ou** expressão</span><span class="sxs-lookup"><span data-stu-id="19a4e-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="19a4e-122">símbolo</span><span class="sxs-lookup"><span data-stu-id="19a4e-122">symbol</span></span>              | <span data-ttu-id="19a4e-123">Propriedade \| % Environment-variável \| $Component-Action \| ? estado do componente \| &recurso-ação \| ! recurso-estado</span><span class="sxs-lookup"><span data-stu-id="19a4e-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="19a4e-124">Os valores e nomes de símbolos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19a4e-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="19a4e-125">Os nomes de variáveis de ambiente não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19a4e-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="19a4e-126">O texto literal deve ser colocado entre aspas ("text").</span><span class="sxs-lookup"><span data-stu-id="19a4e-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="19a4e-127">O texto literal contendo aspas não pode ser usado em instruções condicionais porque não há caractere de escape para aspas dentro do texto literal.</span><span class="sxs-lookup"><span data-stu-id="19a4e-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="19a4e-128">Para fazer uma comparação com o texto literal contendo aspas, o texto literal deve ser colocado em uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="19a4e-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="19a4e-129">Por exemplo, para verificar se a propriedade SERVERname não contém aspas, defina uma propriedade chamada QUOTes na tabela de [Propriedades](property-table.md) com um valor de "e altere a condição para não servername><aspas.</span><span class="sxs-lookup"><span data-stu-id="19a4e-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="19a4e-130">Valores de propriedade inexistentes são tratados como cadeias de caracteres vazias.</span><span class="sxs-lookup"><span data-stu-id="19a4e-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="19a4e-131">Não há suporte para valores numéricos de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="19a4e-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="19a4e-132">Os operadores e a precedência são os mesmos das linguagens básica e SQL.</span><span class="sxs-lookup"><span data-stu-id="19a4e-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="19a4e-133">Não há suporte para operadores aritméticos.</span><span class="sxs-lookup"><span data-stu-id="19a4e-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="19a4e-134">Os parênteses podem ser usados para substituir a precedência do operador.</span><span class="sxs-lookup"><span data-stu-id="19a4e-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="19a4e-135">Os operadores não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19a4e-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="19a4e-136">Para comparações de cadeia de caracteres, um til "~" prefixado para o operador executa uma comparação que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19a4e-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="19a4e-137">A comparação de um inteiro com uma cadeia de caracteres ou um valor de propriedade que não pode ser convertido em um inteiro é sempre **msiEvaluateConditionFalse**, exceto pelo operador de comparação "<>", que retorna **msiEvaluateConditionTrue**.</span><span class="sxs-lookup"><span data-stu-id="19a4e-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="19a4e-138">Prefixos de acesso</span><span class="sxs-lookup"><span data-stu-id="19a4e-138">Access Prefixes</span></span>

<span data-ttu-id="19a4e-139">A tabela a seguir mostra os prefixos a serem usados para acessar várias informações do sistema e do instalador para uso em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="19a4e-140">Tipo de símbolo</span><span class="sxs-lookup"><span data-stu-id="19a4e-140">Symbol type</span></span>          | <span data-ttu-id="19a4e-141">Prefixo</span><span class="sxs-lookup"><span data-stu-id="19a4e-141">Prefix</span></span> | <span data-ttu-id="19a4e-142">Valor</span><span class="sxs-lookup"><span data-stu-id="19a4e-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="19a4e-143">Propriedade do instalador</span><span class="sxs-lookup"><span data-stu-id="19a4e-143">Installer property</span></span>   | <span data-ttu-id="19a4e-144">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="19a4e-144">(none)</span></span> | <span data-ttu-id="19a4e-145">Valor da tabela de propriedade ([Propriedade](property-table.md)).</span><span class="sxs-lookup"><span data-stu-id="19a4e-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="19a4e-146">Variável de ambiente</span><span class="sxs-lookup"><span data-stu-id="19a4e-146">Environment variable</span></span> | %      | <span data-ttu-id="19a4e-147">Valor da variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="19a4e-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="19a4e-148">Chave de tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="19a4e-148">Component table key</span></span>  | $      | <span data-ttu-id="19a4e-149">Estado de ação do componente.</span><span class="sxs-lookup"><span data-stu-id="19a4e-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="19a4e-150">Chave de tabela de componentes</span><span class="sxs-lookup"><span data-stu-id="19a4e-150">Component table key</span></span>  | <span data-ttu-id="19a4e-151">?</span><span class="sxs-lookup"><span data-stu-id="19a4e-151">?</span></span>      | <span data-ttu-id="19a4e-152">Estado de instalação do componente.</span><span class="sxs-lookup"><span data-stu-id="19a4e-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="19a4e-153">Chave da tabela de recursos</span><span class="sxs-lookup"><span data-stu-id="19a4e-153">Feature table key</span></span>    | &      | <span data-ttu-id="19a4e-154">Estado de ação do recurso.</span><span class="sxs-lookup"><span data-stu-id="19a4e-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="19a4e-155">Chave da tabela de recursos</span><span class="sxs-lookup"><span data-stu-id="19a4e-155">Feature table key</span></span>    | <span data-ttu-id="19a4e-156">!</span><span class="sxs-lookup"><span data-stu-id="19a4e-156">!</span></span>      | <span data-ttu-id="19a4e-157">Estado instalado do recurso.</span><span class="sxs-lookup"><span data-stu-id="19a4e-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="19a4e-158">Operadores lógicos</span><span class="sxs-lookup"><span data-stu-id="19a4e-158">Logical Operators</span></span>

<span data-ttu-id="19a4e-159">A tabela a seguir mostra os operadores lógicos em expressões condicionais, em ordem de precedência de alto para baixo.</span><span class="sxs-lookup"><span data-stu-id="19a4e-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="19a4e-160">Operador</span><span class="sxs-lookup"><span data-stu-id="19a4e-160">Operator</span></span> | <span data-ttu-id="19a4e-161">Significado</span><span class="sxs-lookup"><span data-stu-id="19a4e-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="19a4e-162">Not</span><span class="sxs-lookup"><span data-stu-id="19a4e-162">Not</span></span>      | <span data-ttu-id="19a4e-163">Operador unário de prefixo; inverte o estado do termo a seguir.</span><span class="sxs-lookup"><span data-stu-id="19a4e-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="19a4e-164">E</span><span class="sxs-lookup"><span data-stu-id="19a4e-164">And</span></span>      | <span data-ttu-id="19a4e-165">TRUE se ambos os termos forem verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="19a4e-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="19a4e-166">Ou</span><span class="sxs-lookup"><span data-stu-id="19a4e-166">Or</span></span>       | <span data-ttu-id="19a4e-167">TRUE se um ou ambos os termos forem verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="19a4e-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="19a4e-168">Xor</span><span class="sxs-lookup"><span data-stu-id="19a4e-168">Xor</span></span>      | <span data-ttu-id="19a4e-169">TRUE se nenhum dos dois termos for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="19a4e-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="19a4e-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="19a4e-170">Eqv</span></span>      | <span data-ttu-id="19a4e-171">TRUE se ambos os termos forem verdadeiros ou ambos os termos forem falsos.</span><span class="sxs-lookup"><span data-stu-id="19a4e-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="19a4e-172">IMP</span><span class="sxs-lookup"><span data-stu-id="19a4e-172">Imp</span></span>      | <span data-ttu-id="19a4e-173">TRUE se o termo esquerdo for FALSE ou o termo direito for TRUE.</span><span class="sxs-lookup"><span data-stu-id="19a4e-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="19a4e-174">Operadores comparativaes</span><span class="sxs-lookup"><span data-stu-id="19a4e-174">Comparative Operators</span></span>

<span data-ttu-id="19a4e-175">A tabela a seguir mostra os operadores de comparação usados em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="19a4e-176">Esses operadores de comparação só podem ocorrer entre dois valores.</span><span class="sxs-lookup"><span data-stu-id="19a4e-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="19a4e-177">Operador</span><span class="sxs-lookup"><span data-stu-id="19a4e-177">Operator</span></span> | <span data-ttu-id="19a4e-178">Significado</span><span class="sxs-lookup"><span data-stu-id="19a4e-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="19a4e-179">VERDADEIRO se o valor esquerdo for igual ao valor correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="19a4e-180">VERDADEIRO se o valor esquerdo não for igual ao valor correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="19a4e-181">VERDADEIRO se o valor esquerdo for maior que o valor correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="19a4e-182">VERDADEIRO se o valor esquerdo for maior ou igual ao valor correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="19a4e-183">TRUE se o valor Left for menor que o valor Right.</span><span class="sxs-lookup"><span data-stu-id="19a4e-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="19a4e-184">VERDADEIRO se o valor esquerdo for menor ou igual ao valor correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="19a4e-185">Operadores de subcadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="19a4e-185">Substring Operators</span></span>

<span data-ttu-id="19a4e-186">A tabela a seguir mostra os operadores de subcadeia de caracteres usados em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="19a4e-187">Operadores de subcadeia de caracteres podem ocorrer entre dois valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="19a4e-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="19a4e-188">Operador</span><span class="sxs-lookup"><span data-stu-id="19a4e-188">Operator</span></span> | <span data-ttu-id="19a4e-189">Significado</span><span class="sxs-lookup"><span data-stu-id="19a4e-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="19a4e-190">TRUE se a cadeia de caracteres esquerda contiver a cadeia de caracteres correta.</span><span class="sxs-lookup"><span data-stu-id="19a4e-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="19a4e-191">TRUE se a cadeia de caracteres esquerda começar com a cadeia de caracteres correta.</span><span class="sxs-lookup"><span data-stu-id="19a4e-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="19a4e-192">TRUE se a cadeia de caracteres esquerda terminar com a cadeia de caracteres correta.</span><span class="sxs-lookup"><span data-stu-id="19a4e-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="19a4e-193">Operadores numéricos bits</span><span class="sxs-lookup"><span data-stu-id="19a4e-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="19a4e-194">A tabela a seguir mostra os operadores numéricos de bits em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="19a4e-195">Esses operadores podem ocorrer entre dois valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="19a4e-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="19a4e-196">Operador</span><span class="sxs-lookup"><span data-stu-id="19a4e-196">Operator</span></span> | <span data-ttu-id="19a4e-197">Significado</span><span class="sxs-lookup"><span data-stu-id="19a4e-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="19a4e-198">AND bit e, TRUE se os inteiros esquerdo e direito tiverem quaisquer bits em comum.</span><span class="sxs-lookup"><span data-stu-id="19a4e-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="19a4e-199">True se os 16 bits altos do inteiro esquerdo forem iguais ao inteiro correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="19a4e-200">True se os 16 bits baixos do inteiro esquerdo forem iguais ao inteiro correto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="19a4e-201">Valores de estado de componente e recurso</span><span class="sxs-lookup"><span data-stu-id="19a4e-201">Feature and Component State Values</span></span>

<span data-ttu-id="19a4e-202">A tabela a seguir mostra onde é válido usar os símbolos de operador de componente e recurso.</span><span class="sxs-lookup"><span data-stu-id="19a4e-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="19a4e-203">Operador <state></span><span class="sxs-lookup"><span data-stu-id="19a4e-203">Operator <state></span></span> | <span data-ttu-id="19a4e-204">Onde essa sintaxe é válida</span><span class="sxs-lookup"><span data-stu-id="19a4e-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a4e-205">ação de $component</span><span class="sxs-lookup"><span data-stu-id="19a4e-205">$component-action</span></span>      | <span data-ttu-id="19a4e-206">Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="19a4e-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="19a4e-207">Recurso de &-ação</span><span class="sxs-lookup"><span data-stu-id="19a4e-207">&feature-action</span></span>        | <span data-ttu-id="19a4e-208">Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="19a4e-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="19a4e-209">! recurso-estado</span><span class="sxs-lookup"><span data-stu-id="19a4e-209">!feature-state</span></span>         | <span data-ttu-id="19a4e-210">Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="19a4e-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="19a4e-211">? Estado do componente</span><span class="sxs-lookup"><span data-stu-id="19a4e-211">?component-state</span></span>       | <span data-ttu-id="19a4e-212">Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="19a4e-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="19a4e-213">A tabela a seguir mostra os valores de estado do componente e do recurso usados em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="19a4e-214">Esses Estados não são definidos até que [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) seja chamado, seja diretamente ou pela ação [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="19a4e-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="19a4e-215">Estado</span><span class="sxs-lookup"><span data-stu-id="19a4e-215">State</span></span>                    | <span data-ttu-id="19a4e-216">Valor</span><span class="sxs-lookup"><span data-stu-id="19a4e-216">Value</span></span> | <span data-ttu-id="19a4e-217">Significado</span><span class="sxs-lookup"><span data-stu-id="19a4e-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="19a4e-218">INSTALLstate \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="19a4e-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="19a4e-219">-1</span><span class="sxs-lookup"><span data-stu-id="19a4e-219">-1</span></span>    | <span data-ttu-id="19a4e-220">Nenhuma ação a ser executada no recurso ou componente.</span><span class="sxs-lookup"><span data-stu-id="19a4e-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="19a4e-221">INSTALLstate \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="19a4e-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="19a4e-222">1</span><span class="sxs-lookup"><span data-stu-id="19a4e-222">1</span></span>     | <span data-ttu-id="19a4e-223">Recurso anunciado.</span><span class="sxs-lookup"><span data-stu-id="19a4e-223">Advertised feature.</span></span> <span data-ttu-id="19a4e-224">Esse estado não está disponível para os componentes do.</span><span class="sxs-lookup"><span data-stu-id="19a4e-224">This state is not available for components.</span></span> |
| <span data-ttu-id="19a4e-225">INSTALLstate \_ ausente</span><span class="sxs-lookup"><span data-stu-id="19a4e-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="19a4e-226">2</span><span class="sxs-lookup"><span data-stu-id="19a4e-226">2</span></span>     | <span data-ttu-id="19a4e-227">O recurso ou componente não está presente.</span><span class="sxs-lookup"><span data-stu-id="19a4e-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="19a4e-228">INSTALAR \_ local</span><span class="sxs-lookup"><span data-stu-id="19a4e-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="19a4e-229">3</span><span class="sxs-lookup"><span data-stu-id="19a4e-229">3</span></span>     | <span data-ttu-id="19a4e-230">Recurso ou componente no computador local.</span><span class="sxs-lookup"><span data-stu-id="19a4e-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="19a4e-231">origem de INSTALLstate \_</span><span class="sxs-lookup"><span data-stu-id="19a4e-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="19a4e-232">4</span><span class="sxs-lookup"><span data-stu-id="19a4e-232">4</span></span>     | <span data-ttu-id="19a4e-233">Execução de recurso ou componente da origem.</span><span class="sxs-lookup"><span data-stu-id="19a4e-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="19a4e-234">Por exemplo, a expressão condicional "&MyFeature = 3" será avaliada como true somente se MyFeature estiver mudando de seu estado atual para o estado de ser instalado no computador local, INSTALLstate \_ local.</span><span class="sxs-lookup"><span data-stu-id="19a4e-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="19a4e-235">Observe que você não deve depender da condição $Component 1 = 3 para verificar se o Component1 está instalado localmente no computador.</span><span class="sxs-lookup"><span data-stu-id="19a4e-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="19a4e-236">Isso poderá falhar se o Component1 for instalado por mais de um produto.</span><span class="sxs-lookup"><span data-stu-id="19a4e-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="19a4e-237">Depois que o Component1 tiver sido instalado localmente pelo Product1, o instalador avaliará a condição $Component 1 = 3 como false durante a instalação do Product2.</span><span class="sxs-lookup"><span data-stu-id="19a4e-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="19a4e-238">Isso ocorre porque o instalador determina a versão do componente usando o caminho de chave do componente e marca o componente para instalação se sua versão for maior ou igual ao componente instalado.</span><span class="sxs-lookup"><span data-stu-id="19a4e-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="19a4e-239">Observe que o instalador não fará comparações diretas do tipo de dados [version](version.md) em instruções condicionais.</span><span class="sxs-lookup"><span data-stu-id="19a4e-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="19a4e-240">Por exemplo, você não pode usar operadores comparativa para comparar versões como "1,10" e "1, 10" em uma instrução condicional.</span><span class="sxs-lookup"><span data-stu-id="19a4e-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="19a4e-241">Em vez disso, use um método válido para pesquisar uma versão, como descrito em [pesquisando aplicativos existentes, arquivos, entradas de registro ou entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)e, em seguida, defina uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="19a4e-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19a4e-242">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19a4e-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a4e-243">Usando propriedades em instruções condicionais</span><span class="sxs-lookup"><span data-stu-id="19a4e-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



