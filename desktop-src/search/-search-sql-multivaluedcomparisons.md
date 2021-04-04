---
description: As colunas armazenadas no índice de conteúdo podem ter vários valores e as colunas com múltiplos valores podem ser comparadas usando o predicado de comparação de matriz.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparações de vários valores (matriz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646868"
---
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="7cde6-103">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="7cde6-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="7cde6-104">As colunas armazenadas no índice de conteúdo podem ter vários valores e as colunas com múltiplos valores podem ser comparadas usando o predicado de comparação de matriz.</span><span class="sxs-lookup"><span data-stu-id="7cde6-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="7cde6-105">O predicado de comparação de matriz tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="7cde6-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="7cde6-106">Um erro será retornado se a referência de coluna não for uma coluna com valores de multivalor.</span><span class="sxs-lookup"><span data-stu-id="7cde6-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="7cde6-107">O tipo de dados da coluna deve ser compatível com os elementos da lista de comparação.</span><span class="sxs-lookup"><span data-stu-id="7cde6-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="7cde6-108">Se necessário, a referência de coluna pode ser [convertida](-search-sql-castingdatacolumntype.md) como outro tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7cde6-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="7cde6-109">O operador de comparação ( \_ op comp) pode ser qualquer um dos operadores de comparação normais.</span><span class="sxs-lookup"><span data-stu-id="7cde6-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="7cde6-110">Em uma comparação de vários valores, os operadores de comparação têm significados um pouco diferentes dependendo se um quantificador é usado.</span><span class="sxs-lookup"><span data-stu-id="7cde6-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="7cde6-111">Quantificadores identificam se uma comparação deve ser feita em relação a todos ou a alguns dos valores na lista de comparação.</span><span class="sxs-lookup"><span data-stu-id="7cde6-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="7cde6-112">As funções dos operadores de comparação são dadas nas tabelas que descrevem cada quantificador (todos e alguns) posteriormente neste documento.</span><span class="sxs-lookup"><span data-stu-id="7cde6-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="7cde6-113">O valor após o operador especifica um valor literal único que é comparado com todos os elementos da coluna com valores de multivalor.</span><span class="sxs-lookup"><span data-stu-id="7cde6-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="7cde6-114">Se qualquer elemento corresponder ao valor, o predicado será true.</span><span class="sxs-lookup"><span data-stu-id="7cde6-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="7cde6-115">A lista de comparação especifica uma matriz de valores literais que são comparados com a coluna com várias valores.</span><span class="sxs-lookup"><span data-stu-id="7cde6-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="7cde6-116">A sintaxe da lista de comparação é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="7cde6-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="7cde6-117">Lembre-se da sintaxe da lista de comparação.</span><span class="sxs-lookup"><span data-stu-id="7cde6-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="7cde6-118">O grupo de literais que compõem a lista de comparação deve estar entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="7cde6-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="7cde6-119">Não coloque elementos individuais da lista de comparação por colchetes.</span><span class="sxs-lookup"><span data-stu-id="7cde6-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="7cde6-120">Portanto, a matriz 1 \[ \] e a matriz \[ 1, 2, 3 \] são válidas, mas a matriz \[ 1 \[ , 2 \] \[ , 3 \] \] não é.</span><span class="sxs-lookup"><span data-stu-id="7cde6-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="7cde6-121">O método usado para determinar se a comparação de valores multivalor retorna true ou false é especificado pelo quantificador opcional.</span><span class="sxs-lookup"><span data-stu-id="7cde6-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="7cde6-122">As seções a seguir descrevem cada quantificador e como cada operador de comparação funciona quando o quantificador é usado.</span><span class="sxs-lookup"><span data-stu-id="7cde6-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="7cde6-123">Quantificador ausente</span><span class="sxs-lookup"><span data-stu-id="7cde6-123">Absent Quantifier</span></span>

<span data-ttu-id="7cde6-124">Se nenhum quantificador for especificado, cada elemento no lado esquerdo da comparação será comparado ao elemento na mesma posição no lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="7cde6-125">A comparação começa com o primeiro elemento nas matrizes e progride pelo último elemento.</span><span class="sxs-lookup"><span data-stu-id="7cde6-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="7cde6-126">Se todos os elementos no lado esquerdo forem equivalentes aos elementos correspondentes no lado direito, o número de elementos da matriz será usado para determinar qual matriz é maior.</span><span class="sxs-lookup"><span data-stu-id="7cde6-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="7cde6-127">A tabela a seguir mostra a operação dos operadores de comparação quando nenhum quantificador é especificado e fornece uma breve descrição de cada um.</span><span class="sxs-lookup"><span data-stu-id="7cde6-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="7cde6-128">Operador</span><span class="sxs-lookup"><span data-stu-id="7cde6-128">Operator</span></span>       | <span data-ttu-id="7cde6-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cde6-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="7cde6-130">' Equals ' retorna true quando cada elemento do lado esquerdo tem o mesmo valor que o elemento do lado direito correspondente e ambas as matrizes têm o mesmo número de elementos.</span><span class="sxs-lookup"><span data-stu-id="7cde6-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="7cde6-131">! = ou <></span><span class="sxs-lookup"><span data-stu-id="7cde6-131">!= or <></span></span> | <span data-ttu-id="7cde6-132">' Not igual a ' retorna true quando um ou mais elementos do lado esquerdo têm valores que diferem dos elementos correspondentes do lado direito, ou quando as matrizes do lado esquerdo e do lado direito não têm o mesmo número de elementos.</span><span class="sxs-lookup"><span data-stu-id="7cde6-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="7cde6-133">' Maior que ' retorna true quando o valor de cada elemento do lado esquerdo é maior que o valor do elemento do lado direito correspondente.</span><span class="sxs-lookup"><span data-stu-id="7cde6-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="7cde6-134">Se todos os valores de elemento do lado esquerdo corresponderem exatamente aos elementos correspondentes do lado direito e a matriz do lado esquerdo tiver mais elementos do que a matriz do lado direito, ' maior que ' retornará true.</span><span class="sxs-lookup"><span data-stu-id="7cde6-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="7cde6-135">' Maior que ou igual a ' retorna true quando o valor de cada elemento do lado esquerdo é maior ou igual ao valor do elemento do lado direito correspondente.</span><span class="sxs-lookup"><span data-stu-id="7cde6-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="7cde6-136">Se todos os valores de elemento do lado esquerdo forem iguais ou maiores que os elementos correspondentes do lado direito, e a matriz do lado esquerdo tiver os mesmos ou mais elementos do que a matriz do lado direito, ' maior que ' retornará true.</span><span class="sxs-lookup"><span data-stu-id="7cde6-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="7cde6-137">' Less than ' retorna true quando o valor de cada elemento do lado esquerdo é menor que o valor do elemento do lado direito correspondente.</span><span class="sxs-lookup"><span data-stu-id="7cde6-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="7cde6-138">' Menor que ' também retorna true quando o lado esquerdo tem menos elementos do que o lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="7cde6-139">' Menor que ou igual a ' retorna true quando o valor de cada elemento do lado esquerdo é menor ou igual ao valor do elemento do lado direito correspondente.</span><span class="sxs-lookup"><span data-stu-id="7cde6-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="7cde6-140">Se todos os valores de elemento do lado esquerdo forem iguais ou menores que os elementos correspondentes do lado direito e a matriz do lado esquerdo tiver os mesmos elementos ou menos do que a matriz do lado direito, ' maior que ' retornará true.</span><span class="sxs-lookup"><span data-stu-id="7cde6-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="7cde6-141">Todos os quantificadores</span><span class="sxs-lookup"><span data-stu-id="7cde6-141">ALL Quantifier</span></span>

<span data-ttu-id="7cde6-142">O quantificador ALL especifica que cada elemento no lado esquerdo é comparado a todos os elementos do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="7cde6-143">Para retornar true, a comparação deve ser verdadeira para cada elemento no lado esquerdo quando comparado a todos os elementos do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="7cde6-144">O número de elementos nos lados da matriz esquerda e direita não tem nenhum efeito sobre o resultado.</span><span class="sxs-lookup"><span data-stu-id="7cde6-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="7cde6-145">A tabela a seguir mostra como cada operador de comparação funciona com o quantificador ALL.</span><span class="sxs-lookup"><span data-stu-id="7cde6-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="7cde6-146">Operador</span><span class="sxs-lookup"><span data-stu-id="7cde6-146">Operator</span></span>       | <span data-ttu-id="7cde6-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cde6-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="7cde6-148">' Equals ' retorna true quando cada valor de elemento do lado esquerdo é igual a todos os valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="7cde6-149">! = ou <></span><span class="sxs-lookup"><span data-stu-id="7cde6-149">!= or <></span></span> | <span data-ttu-id="7cde6-150">' Diferente de ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é diferente de qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="7cde6-151">' Maior que ' retorna true quando cada valor de elemento do lado esquerdo é maior que cada valor de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="7cde6-152">' Maior que ou igual a ' retorna true quando cada valor de elemento do lado esquerdo é maior ou igual a cada valor de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="7cde6-153">' Less than ' retorna true quando cada valor de elemento do lado esquerdo é menor que todo o valor do elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="7cde6-154">' Menor que ou igual a ' retorna true quando cada valor de elemento do lado esquerdo é menor ou igual a cada valor de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="7cde6-155">ALGUM quantificador (ou qualquer)</span><span class="sxs-lookup"><span data-stu-id="7cde6-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="7cde6-156">O quantificador e o quantificador ANY podem ser usados de forma intercambiável.</span><span class="sxs-lookup"><span data-stu-id="7cde6-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="7cde6-157">Como o quantificador ALL, o quantificador especifica que cada elemento no lado esquerdo é comparado com todos os elementos do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="7cde6-158">Para retornar true, a comparação deve ser verdadeira para pelo menos um dos elementos no lado esquerdo quando comparado a qualquer elemento no lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="7cde6-159">O número de elementos nas matrizes esquerda e direita não tem nenhum efeito sobre o resultado.</span><span class="sxs-lookup"><span data-stu-id="7cde6-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="7cde6-160">A tabela a seguir mostra como cada operador de comparação funciona com um quantificador.</span><span class="sxs-lookup"><span data-stu-id="7cde6-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="7cde6-161">Operador</span><span class="sxs-lookup"><span data-stu-id="7cde6-161">Operator</span></span>       | <span data-ttu-id="7cde6-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cde6-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="7cde6-163">' Equals ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é o mesmo que qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="7cde6-164">! = ou <></span><span class="sxs-lookup"><span data-stu-id="7cde6-164">!= or <></span></span> | <span data-ttu-id="7cde6-165">' Not igual a ' retorna true quando nenhum dos valores de elemento do lado esquerdo é o mesmo que qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="7cde6-166">' Maior que ' retorna true quando pelo menos um dos valores de elementos do lado esquerdo é maior que qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="7cde6-167">' Maior que ou igual a ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é maior ou igual a qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="7cde6-168">' Less than ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é menor que qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="7cde6-169">' Menor que ou igual a ' retorna true quando pelo menos um dos valores de elemento do lado esquerdo é menor ou igual a qualquer um dos valores de elemento do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7cde6-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="7cde6-170">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7cde6-170">Examples</span></span>

<span data-ttu-id="7cde6-171">O exemplo a seguir verifica se os documentos estão nas categorias "Finance" ou "Planning":</span><span class="sxs-lookup"><span data-stu-id="7cde6-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="7cde6-172">Todas as comparações a seguir são avaliadas como true.</span><span class="sxs-lookup"><span data-stu-id="7cde6-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="7cde6-173">Lembre-se de que, em uso real, a sintaxe da consulta de pesquisa exige que o lado esquerdo seja uma propriedade, não um valor literal.</span><span class="sxs-lookup"><span data-stu-id="7cde6-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="7cde6-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cde6-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7cde6-175">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7cde6-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7cde6-176">Predicado LIKE</span><span class="sxs-lookup"><span data-stu-id="7cde6-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="7cde6-177">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="7cde6-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="7cde6-178">Predicado nulo</span><span class="sxs-lookup"><span data-stu-id="7cde6-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="7cde6-179">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7cde6-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7cde6-180">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="7cde6-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="7cde6-181">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="7cde6-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



