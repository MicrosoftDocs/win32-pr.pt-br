---
description: As condições que determinam se um documento está incluído nos resultados retornados pela consulta são especificadas pela cláusula WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Cláusula WHERE (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779923"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="6b6bc-103">Cláusula WHERE (pesquisa do Windows)</span><span class="sxs-lookup"><span data-stu-id="6b6bc-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="6b6bc-104">As condições que determinam se um documento está incluído nos resultados retornados pela consulta são especificadas pela cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="6b6bc-105">No nível mais alto, há duas partes para a sintaxe da cláusula WHERE:</span><span class="sxs-lookup"><span data-stu-id="6b6bc-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="6b6bc-106">O \_ alias de grupo de <opcional> parte da cláusula simplifica consultas complexas atribuindo um alias a um grupo de uma ou mais colunas.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="6b6bc-107">Isso pode melhorar a legibilidade de consultas complexas que pesquisam as mesmas informações em várias colunas especificadas por URLs.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="6b6bc-108">Para obter mais informações sobre aliases de grupo, consulte [with--como predicado de alias de grupo](-search-sql-with-as.md).</span><span class="sxs-lookup"><span data-stu-id="6b6bc-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="6b6bc-109">A <search condition> parte da cláusula WHERE é um ou mais predicados de pesquisa que especificam critérios de correspondência para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="6b6bc-110">Os predicados de pesquisa são expressões que afirmam algum fato sobre algum valor.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="6b6bc-111">O resultado de um critério de pesquisa é um valor booliano, seja **verdadeiro** se o documento atender aos critérios de pesquisa especificados ou **false** se não tiver.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="6b6bc-112">Se o resultado for **true**, o documento será retornado.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="6b6bc-113">Se o resultado for **false**, o documento não será retornado.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="6b6bc-114">Os documentos retornados em uma consulta do Microsoft Windows Search recebem valores de classificação de acordo com o quão bem eles correspondem às condições de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="6b6bc-115">Cada uma das condições de pesquisa de consulta pode incluir uma cláusula [RANKBY](-search-sql-rankby.md) que dá suporte à modificação dos valores de classificação retornados.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="6b6bc-116">A [função ReuseWhere](-search-sql-reusewhere.md) faz várias consultas que usam algumas das mesmas condições de pesquisa mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="6b6bc-117">A cláusula WHERE em uma consulta especifica o conjunto de itens que correspondem em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="6b6bc-118">As consultas subsequentes podem compartilhar o trabalho executado para o evalution anterior usando a função ReuseWhere na nova cláusula WHERE de consulta.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="6b6bc-119">Predicados de pesquisa</span><span class="sxs-lookup"><span data-stu-id="6b6bc-119">Search Predicates</span></span>

<span data-ttu-id="6b6bc-120">Um critério de pesquisa consiste em um ou mais predicados ou critérios de pesquisa que descrevem o que o usuário está procurando (por exemplo, em que System. DateCreated > ' 2006-04-19 ').</span><span class="sxs-lookup"><span data-stu-id="6b6bc-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="6b6bc-121">Os predicados de pesquisa podem ser combinados usando os operadores lógicos **e** **, ou, ou** **não**.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="6b6bc-122">O operador unário opcional **não** pode ser usado apenas com **and** e somente para negar o valor lógico de um predicado ou critério de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="6b6bc-123">Você pode usar parênteses para agrupar e aninhar termos lógicos.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="6b6bc-124">A tabela a seguir mostra a ordem de precedência para os operadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="6b6bc-125">Ordem (precedência)</span><span class="sxs-lookup"><span data-stu-id="6b6bc-125">Order (precedence)</span></span> | <span data-ttu-id="6b6bc-126">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="6b6bc-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="6b6bc-127">Primeiro (mais alto)</span><span class="sxs-lookup"><span data-stu-id="6b6bc-127">First (highest)</span></span>    | <span data-ttu-id="6b6bc-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-128">**NOT**</span></span>          |
| <span data-ttu-id="6b6bc-129">Segundo</span><span class="sxs-lookup"><span data-stu-id="6b6bc-129">Second</span></span>             | <span data-ttu-id="6b6bc-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-130">**AND**</span></span>          |
| <span data-ttu-id="6b6bc-131">Terceiro (mais baixo)</span><span class="sxs-lookup"><span data-stu-id="6b6bc-131">Third (lowest)</span></span>     | <span data-ttu-id="6b6bc-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-132">**OR**</span></span>           |



 

<span data-ttu-id="6b6bc-133">Os operadores lógicos do mesmo tipo são associativos e não há nenhuma ordem de cálculo especificada.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="6b6bc-134">Por exemplo, (A **e** b) **e** (c **e** D) podem ser calculados (a **e** d) **e** (B **e** C) sem alteração no resultado lógico.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6b6bc-135">Incorreto: onde **não** contém (' computador ')</span><span class="sxs-lookup"><span data-stu-id="6b6bc-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="6b6bc-136">Correto: onde contém (' software ') **e não** contém (' Computer ')</span><span class="sxs-lookup"><span data-stu-id="6b6bc-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="6b6bc-137">Em consultas complexas, talvez você queira posicionar mais ênfase nas correspondências em algumas colunas do que em outras.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="6b6bc-138">Por exemplo, ao pesquisar documentos que abordam "design de software", encontrar o termo de pesquisa no título do documento é mais provável que seja uma boa correspondência do que localizar as palavras individuais no texto do documento.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="6b6bc-139">Para influenciar a classificação de documentos dessa maneira, a linguagem de consulta do Microsoft Windows Search dá suporte à ponderação de critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="6b6bc-140">Para obter mais informações sobre o peso de coluna, consulte contém predicado [Contains](-search-sql-contains.md) e [FREETEXT predicado](-search-sql-freetext.md).</span><span class="sxs-lookup"><span data-stu-id="6b6bc-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="6b6bc-141">Há três grupos de predicados de pesquisa no Windows Search: pesquisas de texto completo, texto não completo e profundidade de pasta.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="6b6bc-142">Os predicados de pesquisa de texto completo normalmente correspondem ao significado do conteúdo, título e outras colunas e dão suporte à correspondência lingüística (por exemplo, formas de palavras alternativas, frases e pesquisa de proximidade).</span><span class="sxs-lookup"><span data-stu-id="6b6bc-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="6b6bc-143">Por outro lado, os predicados de pesquisa de texto não completo correspondem ao valor das colunas especificadas e não incluem nenhum processamento linguístico especial, mas, em vários casos, oferecem correspondência de padrão baseada em caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="6b6bc-144">Os predicados de profundidade de pasta restringem o escopo de pesquisa a um caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="6b6bc-145">Se a consulta retornar um documento porque um predicado de texto não completo é avaliado como **verdadeiro** para esse documento, o valor de classificação é calculado como 1000.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="6b6bc-146">O uso da [função de coerção de classificação](-search-sql-rankby.md) pode modificar o valor de classificação.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="6b6bc-147">As tabelas a seguir descrevem os predicados de pesquisa de texto completo, de texto não completo e de profundidade de pasta.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="6b6bc-148">Predicado de texto completo</span><span class="sxs-lookup"><span data-stu-id="6b6bc-148">Full-text predicate</span></span>                  | <span data-ttu-id="6b6bc-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b6bc-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b6bc-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="6b6bc-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="6b6bc-151">Dá suporte a pesquisas complexas de termos em colunas de texto do documento (por exemplo, título, conteúdo).</span><span class="sxs-lookup"><span data-stu-id="6b6bc-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="6b6bc-152">Pode pesquisar formulários formas flexionadas dos termos de pesquisa, testar a proximidade dos termos e executar comparações lógicas.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="6b6bc-153">Os termos de pesquisa podem incluir caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="6b6bc-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="6b6bc-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="6b6bc-155">Procura documentos que correspondam ao significado da frase de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="6b6bc-156">Palavras relacionadas e frases semelhantes serão correspondentes, com a coluna de classificação calculada com base em quão próximo o documento corresponde à frase de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="6b6bc-157">Os termos de pesquisa não podem incluir caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="6b6bc-158">Predicado de texto não completo</span><span class="sxs-lookup"><span data-stu-id="6b6bc-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="6b6bc-159">Description</span><span class="sxs-lookup"><span data-stu-id="6b6bc-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b6bc-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="6b6bc-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="6b6bc-161">Os valores de coluna são comparados usando a correspondência de padrão simples com caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="6b6bc-162">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="6b6bc-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="6b6bc-163">Os valores de coluna são comparados com valores literais de cadeia de caracteres, data, carimbo de hora, numéricos e outros.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="6b6bc-164">Esse predicado dá suporte a igualdade e desigualdades, como maior que e menor que.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="6b6bc-165">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="6b6bc-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="6b6bc-166">As colunas com valores de multivalor são comparadas com uma matriz de valores literais.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="6b6bc-167">NULL</span><span class="sxs-lookup"><span data-stu-id="6b6bc-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="6b6bc-168">Os valores de coluna que são indefinidos para o documento podem ser detectados usando o predicado **NULL** .</span><span class="sxs-lookup"><span data-stu-id="6b6bc-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="6b6bc-169">Profundidade da pasta</span><span class="sxs-lookup"><span data-stu-id="6b6bc-169">Folder Depth</span></span>                             | <span data-ttu-id="6b6bc-170">Description</span><span class="sxs-lookup"><span data-stu-id="6b6bc-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b6bc-171">COM</span><span class="sxs-lookup"><span data-stu-id="6b6bc-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="6b6bc-172">Executa uma passagem profunda do caminho especificado, incluindo a pasta específica e todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="6b6bc-173">ACTIVE</span><span class="sxs-lookup"><span data-stu-id="6b6bc-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="6b6bc-174">Executa uma passagem superficial do caminho especificado, pesquisando apenas a pasta específica.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="6b6bc-175">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b6bc-175">Examples</span></span>

<span data-ttu-id="6b6bc-176">Para obter exemplos da cláusula WHERE, consulte os tópicos de predicado individuais vinculados na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="6b6bc-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b6bc-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b6bc-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6b6bc-178">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b6bc-179">Função ReuseWhere</span><span class="sxs-lookup"><span data-stu-id="6b6bc-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-180">Propriedades do conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="6b6bc-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-181">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="6b6bc-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-182">Visão geral da sintaxe de pesquisa SQL</span><span class="sxs-lookup"><span data-stu-id="6b6bc-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-183">Como predicado de alias de grupo--AS</span><span class="sxs-lookup"><span data-stu-id="6b6bc-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-184">Predicados de escopo e diretório</span><span class="sxs-lookup"><span data-stu-id="6b6bc-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-185">CLASSIFICAR por cláusula</span><span class="sxs-lookup"><span data-stu-id="6b6bc-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="6b6bc-186">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6b6bc-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b6bc-187">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="6b6bc-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="6b6bc-188">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="6b6bc-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



