---
description: O predicado CONTAINS faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826907"
---
# <a name="contains-predicate"></a><span data-ttu-id="e5c45-103">Predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="e5c45-103">CONTAINS Predicate</span></span>

<span data-ttu-id="e5c45-104">O predicado CONTAINS faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto.</span><span class="sxs-lookup"><span data-stu-id="e5c45-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="e5c45-105">O predicado CONTAINS tem recursos para palavras correspondentes, correspondência de formas de palavras informativas, pesquisa usando caracteres curinga e pesquisa usando a proximidade.</span><span class="sxs-lookup"><span data-stu-id="e5c45-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="e5c45-106">Você também pode aplicar pesos em um predicado CONTAINS para definir a importância das colunas em que o termo de pesquisa é encontrado.</span><span class="sxs-lookup"><span data-stu-id="e5c45-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="e5c45-107">O predicado CONTAINS é mais adequado para correspondências exatas, em contraste com o predicado [FREETEXT](-search-sql-freetext.md) , que é mais adequado para localizar documentos que contenham combinações das palavras de pesquisa espalhadas por toda a coluna.</span><span class="sxs-lookup"><span data-stu-id="e5c45-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="e5c45-108">As pesquisas não diferenciam letras maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e5c45-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="e5c45-109">Veja a seguir a sintaxe básica do predicado CONTAINS:</span><span class="sxs-lookup"><span data-stu-id="e5c45-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="e5c45-110">A referência de coluna de texto completo \_ é opcional.</span><span class="sxs-lookup"><span data-stu-id="e5c45-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="e5c45-111">Com ele, você pode limitar a pesquisa a uma única coluna ou a um grupo de colunas no qual o predicado CONTAINS é testado.</span><span class="sxs-lookup"><span data-stu-id="e5c45-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="e5c45-112">Quando a coluna FULLTEXT é especificada como "ALL" ou " \* ", todas as propriedades de texto indexado são pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="e5c45-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="e5c45-113">Embora a coluna não precise ser uma propriedade de texto, os resultados poderão ser insignificantes se a coluna for outro tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e5c45-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="e5c45-114">O nome da coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado, e você deve separá-lo da condição por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="e5c45-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="e5c45-115">Se nenhuma coluna de texto completo for especificada, a coluna System. Search. Content, que é o corpo do documento, será usada.</span><span class="sxs-lookup"><span data-stu-id="e5c45-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="e5c45-116">A parte LCID do predicado especifica a localidade de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e5c45-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="e5c45-117">Isso instrui o mecanismo de pesquisa a usar o separador de palavras apropriado e formulários de inflexão para a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e5c45-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="e5c45-118">Para especificar a localidade, forneça o identificador de código do idioma padrão do Windows (LCID).</span><span class="sxs-lookup"><span data-stu-id="e5c45-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="e5c45-119">Por exemplo, 1033 é o LCID para o Estados Unidos-Inglês.</span><span class="sxs-lookup"><span data-stu-id="e5c45-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="e5c45-120">Coloque o LCID como o último item dentro dos parênteses da cláusula CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="e5c45-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="e5c45-121">Para obter informações importantes sobre a pesquisa e os idiomas, consulte [usando pesquisas localizadas](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="e5c45-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="e5c45-122">A localidade de pesquisa padrão é a localidade padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="e5c45-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="e5c45-123">A \_ parte da condição Contains deve ser colocada entre aspas simples por palavras únicas ou aspas duplas para frases e consiste em um ou mais termos de pesquisa de conteúdo que são combinados usando os operadores lógicos  **e** ou.</span><span class="sxs-lookup"><span data-stu-id="e5c45-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="e5c45-124">Você pode usar o operador unário opcional **não** após um operador **and** para negar o valor lógico de um termo de pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e5c45-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="e5c45-125">O operador **not** só pode ocorrer depois **de e**.</span><span class="sxs-lookup"><span data-stu-id="e5c45-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="e5c45-126">Você não poderá usar o operador **not** se houver apenas uma condição de correspondência ou depois do operador **or** .</span><span class="sxs-lookup"><span data-stu-id="e5c45-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="e5c45-127">Você pode usar parênteses para agrupar e aninhar termos de pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e5c45-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="e5c45-128">A tabela a seguir descreve a ordem de precedência para os operadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="e5c45-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="e5c45-129">Ordem (precedência)</span><span class="sxs-lookup"><span data-stu-id="e5c45-129">Order (precedence)</span></span> | <span data-ttu-id="e5c45-130">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="e5c45-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="e5c45-131">Primeiro (mais alto)</span><span class="sxs-lookup"><span data-stu-id="e5c45-131">First (highest)</span></span>    | <span data-ttu-id="e5c45-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="e5c45-132">**NOT**</span></span>          |
| <span data-ttu-id="e5c45-133">Segundo</span><span class="sxs-lookup"><span data-stu-id="e5c45-133">Second</span></span>             | <span data-ttu-id="e5c45-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="e5c45-134">**AND**</span></span>          |
| <span data-ttu-id="e5c45-135">Terceiro (mais baixo)</span><span class="sxs-lookup"><span data-stu-id="e5c45-135">Third (lowest)</span></span>     | <span data-ttu-id="e5c45-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="e5c45-136">**OR**</span></span>           |

<span data-ttu-id="e5c45-137">Os operadores lógicos do mesmo tipo são associativos e não há nenhuma ordem de cálculo especificada.</span><span class="sxs-lookup"><span data-stu-id="e5c45-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="e5c45-138">Por exemplo, (A **e** B) **e** (C **e** d) podem ser calculados (B **e** C) **e** (a **e** d) sem alteração no resultado lógico.</span><span class="sxs-lookup"><span data-stu-id="e5c45-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="e5c45-139">A tabela a seguir descreve os tipos de termos de pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e5c45-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5c45-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5c45-140">Type</span></span></th>
<th><span data-ttu-id="e5c45-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5c45-141">Description</span></span></th>
<th><span data-ttu-id="e5c45-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5c45-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5c45-143">Word</span><span class="sxs-lookup"><span data-stu-id="e5c45-143">Word</span></span></td>
<td><span data-ttu-id="e5c45-144">Uma única palavra sem espaços ou outra Pontuação.</span><span class="sxs-lookup"><span data-stu-id="e5c45-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="e5c45-145">Aspas duplas não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="e5c45-145">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c45-146">Frase</span><span class="sxs-lookup"><span data-stu-id="e5c45-146">Phrase</span></span></td>
<td><span data-ttu-id="e5c45-147">Várias palavras ou espaços incluídos.</span><span class="sxs-lookup"><span data-stu-id="e5c45-147">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c45-148">Curinga</span><span class="sxs-lookup"><span data-stu-id="e5c45-148">Wildcard</span></span></td>
<td><span data-ttu-id="e5c45-149">Palavras ou frases com o asterisco (\*) adicionado ao final.</span><span class="sxs-lookup"><span data-stu-id="e5c45-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="e5c45-150">Para obter mais informações, consulte <a href="-search-sql-wildcards.md">usando curingas no predicado CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="e5c45-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c45-151">Coluna de texto completo</span><span class="sxs-lookup"><span data-stu-id="e5c45-151">Full-text Column</span></span></td>
<td><span data-ttu-id="e5c45-152">Um nome de coluna de propriedade no qual corresponder à consulta restante.</span><span class="sxs-lookup"><span data-stu-id="e5c45-152">A property column name against which to match the remaining query.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c45-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="e5c45-153">Boolean</span></span></td>
<td><span data-ttu-id="e5c45-154">Palavras, frases e cadeias de caracteres curinga combinadas usando os operadores boolianos <strong>and</strong>, <strong>or</strong>ou <strong>not</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5c45-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="e5c45-155">Coloque os termos boolianos entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="e5c45-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c45-156">Near</span><span class="sxs-lookup"><span data-stu-id="e5c45-156">Near</span></span></td>
<td><span data-ttu-id="e5c45-157">Palavras, frases ou caracteres curinga separados pela função perto de.</span><span class="sxs-lookup"><span data-stu-id="e5c45-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="e5c45-158">Para obter mais informações, consulte a <a href="-search-sql-near.md">curto prazo</a>.</span><span class="sxs-lookup"><span data-stu-id="e5c45-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c45-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="e5c45-159">FormsOf</span></span></td>
<td><span data-ttu-id="e5c45-160">Corresponde a uma palavra e as versões de inflexão dessa palavra.</span><span class="sxs-lookup"><span data-stu-id="e5c45-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="e5c45-161">Para obter mais informações, consulte <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span><span class="sxs-lookup"><span data-stu-id="e5c45-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c45-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="e5c45-162">IsAbout</span></span></td>
<td><span data-ttu-id="e5c45-163">Combina os resultados correspondentes em vários termos de pesquisa de palavras, frases ou caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="e5c45-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="e5c45-164">Cada termo de pesquisa pode, opcionalmente, ser ponderado.</span><span class="sxs-lookup"><span data-stu-id="e5c45-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="e5c45-165">Opcionalmente, você pode especificar o método de cálculo de classificação, que combina os pesos e quantos itens o documento corresponde.</span><span class="sxs-lookup"><span data-stu-id="e5c45-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="e5c45-166">Para obter mais informações, consulte o <a href="-search-sql-isabout.md">termo ISABOUT</a>.</span><span class="sxs-lookup"><span data-stu-id="e5c45-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

<span data-ttu-id="e5c45-167">Esta seção inclui os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e5c45-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="e5c45-168">Usando curingas no predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="e5c45-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="e5c45-169">FORMSOF termo</span><span class="sxs-lookup"><span data-stu-id="e5c45-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="e5c45-170">@ SOBRE o termo</span><span class="sxs-lookup"><span data-stu-id="e5c45-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="e5c45-171">CURTO prazo</span><span class="sxs-lookup"><span data-stu-id="e5c45-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="e5c45-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5c45-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="e5c45-173">Referência</span><span class="sxs-lookup"><span data-stu-id="e5c45-173">Reference</span></span>

[<span data-ttu-id="e5c45-174">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="e5c45-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="e5c45-175">Conceitual</span><span class="sxs-lookup"><span data-stu-id="e5c45-175">Conceptual</span></span>

[<span data-ttu-id="e5c45-176">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="e5c45-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="e5c45-177">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="e5c45-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
