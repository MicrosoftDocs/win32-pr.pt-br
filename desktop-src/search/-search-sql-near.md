---
description: O termo NEAR é usado para especificar que dois termos de pesquisa de conteúdo devem ser relativamente próximos um do outro para serem reconhecidos como correspondência para o predicado CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: CURTO prazo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296240"
---
# <a name="near-term"></a><span data-ttu-id="c92d4-103">CURTO prazo</span><span class="sxs-lookup"><span data-stu-id="c92d4-103">NEAR Term</span></span>

<span data-ttu-id="c92d4-104">O termo NEAR é usado para especificar que dois termos de pesquisa de conteúdo devem ser relativamente próximos um do outro para serem reconhecidos como correspondência para o predicado [Contains](-search-sql-contains.md) .</span><span class="sxs-lookup"><span data-stu-id="c92d4-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="c92d4-105">A sintaxe para o termo NEAR é:</span><span class="sxs-lookup"><span data-stu-id="c92d4-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="c92d4-106">O termo NEAR pode ser representado pela palavra-chave "NEAR" ou por um til (~).</span><span class="sxs-lookup"><span data-stu-id="c92d4-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="c92d4-107">Quando as palavras Unidas perto da consulta são encontradas em aproximadamente 50 palavras umas das outras dentro da coluna que está sendo pesquisada, o próximo termo retorna uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="c92d4-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="c92d4-108">Quanto mais próximas forem as duas palavras, maior será a classificação calculada para o termo próximo.</span><span class="sxs-lookup"><span data-stu-id="c92d4-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="c92d4-109">Quanto mais distante forem as duas palavras, menor será a classificação.</span><span class="sxs-lookup"><span data-stu-id="c92d4-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="c92d4-110">O número de palavras entre os termos de pesquisa encontrados é aproximado e depende da aparência de palavras de ruído, como "a" ou "a", e como separadores o token de texto.</span><span class="sxs-lookup"><span data-stu-id="c92d4-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="c92d4-111">Pode ser menor que 50.</span><span class="sxs-lookup"><span data-stu-id="c92d4-111">It may be less than 50.</span></span>

 


<span data-ttu-id="c92d4-112">A tabela a seguir descreve os tipos de termo de pesquisa de conteúdo que podem ser usados com um termo próximo em um predicado CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="c92d4-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c92d4-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="c92d4-113">Type</span></span></th>
<th><span data-ttu-id="c92d4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c92d4-114">Description</span></span></th>
<th><span data-ttu-id="c92d4-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c92d4-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c92d4-116">Word</span><span class="sxs-lookup"><span data-stu-id="c92d4-116">Word</span></span></td>
<td><span data-ttu-id="c92d4-117">Uma única palavra sem espaços ou outra Pontuação.</span><span class="sxs-lookup"><span data-stu-id="c92d4-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="c92d4-118">Aspas duplas não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="c92d4-118">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c92d4-119">Frase</span><span class="sxs-lookup"><span data-stu-id="c92d4-119">Phrase</span></span></td>
<td><span data-ttu-id="c92d4-120">Várias palavras ou espaços incluídos.</span><span class="sxs-lookup"><span data-stu-id="c92d4-120">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c92d4-121">Curinga</span><span class="sxs-lookup"><span data-stu-id="c92d4-121">Wildcard</span></span></td>
<td><span data-ttu-id="c92d4-122">Palavras ou frases com o asterisco (\*) adicionado ao final.</span><span class="sxs-lookup"><span data-stu-id="c92d4-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="c92d4-123">Para obter mais informações, consulte <a href="-search-sql-wildcards.md">usando curingas no predicado CONTAINS</a>.</span><span class="sxs-lookup"><span data-stu-id="c92d4-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="c92d4-124">Se as palavras de correspondência especificadas com o termo NEAR forem encontradas na coluna que está sendo pesquisada, mas estiverem mais distantes de 50 palavras, o resultado ainda será retornado, mas terá uma [classificação](-search-sql-understandingrelevancevalues.md) de 0.</span><span class="sxs-lookup"><span data-stu-id="c92d4-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="c92d4-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c92d4-125">Example</span></span>

<span data-ttu-id="c92d4-126">O exemplo a seguir mostra o encadeamento de termos próximos, usando as formas curta e longa do termo:</span><span class="sxs-lookup"><span data-stu-id="c92d4-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="c92d4-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c92d4-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c92d4-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c92d4-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c92d4-129">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="c92d4-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="c92d4-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c92d4-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c92d4-131">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="c92d4-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="c92d4-132">Usando curingas no predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="c92d4-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 



