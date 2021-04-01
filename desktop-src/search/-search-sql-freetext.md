---
description: O predicado FREETEXT faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicado FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646871"
---
# <a name="freetext-predicate"></a><span data-ttu-id="962db-103">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="962db-103">FREETEXT Predicate</span></span>

<span data-ttu-id="962db-104">O predicado FREETEXT faz parte da cláusula [Where](-search-sql-where.md) e dá suporte à pesquisa de palavras e frases em colunas de texto.</span><span class="sxs-lookup"><span data-stu-id="962db-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="962db-105">Use o predicado FREETEXT para localizar documentos que contenham combinações das palavras de pesquisa espalhadas em todo o conteúdo ou colunas especificadas.</span><span class="sxs-lookup"><span data-stu-id="962db-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="962db-106">Para obter o valor de classificação, inclua System. Search. Rank, que é uma classificação de relevence, como uma coluna na instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="962db-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="962db-107">O predicado FREETEXT tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="962db-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="962db-108">A referência de coluna de texto completo é opcional.</span><span class="sxs-lookup"><span data-stu-id="962db-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="962db-109">Com ele, você pode especificar uma única coluna ou um [alias de agrupamento de colunas](-search-sql-with-as.md) em relação ao qual o predicado FREETEXT é testado.</span><span class="sxs-lookup"><span data-stu-id="962db-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="962db-110">Quando a coluna FULLTEXT é especificada como "ALL" ou " \* ", todas as propriedades de texto indexado são pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="962db-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="962db-111">Embora a coluna não precise ser uma propriedade de texto, os resultados poderão ser insignificantes se a coluna for outro tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="962db-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="962db-112">O nome da coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado, e você deve separá-lo da condição por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="962db-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="962db-113">Se nenhuma condição de texto completo for fornecida, a coluna conteúdo, que é o corpo do documento, será usada.</span><span class="sxs-lookup"><span data-stu-id="962db-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="962db-114">Você pode especificar uma localidade de pesquisa para identificar o separador de palavras apropriado e formulários de inflexão para a consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="962db-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="962db-115">Os valores de localidade válidos são um LCID (identificador de código de idioma padrão) do Windows.</span><span class="sxs-lookup"><span data-stu-id="962db-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="962db-116">Por exemplo, 1033 é o LCID para o Estados Unidos-Inglês.</span><span class="sxs-lookup"><span data-stu-id="962db-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="962db-117">Coloque o LCID como o último item dentro dos parênteses da cláusula FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="962db-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="962db-118">Para obter informações importantes sobre a pesquisa e os idiomas, consulte [usando pesquisas localizadas](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="962db-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="962db-119">A localidade de pesquisa padrão é a localidade padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="962db-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="962db-120">Você deve colocar a parte da condição FREETEXT entre aspas simples e deve consistir em um ou mais termos de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="962db-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="962db-121">O predicado FREETEXT não oferece suporte a operações lógicas.</span><span class="sxs-lookup"><span data-stu-id="962db-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="962db-122">Para procurar uma frase como se fosse uma única palavra, coloque a frase entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="962db-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="962db-123">Quando você usa o predicado FREETEXT, os resultados da consulta de pesquisa retornam documentos que contêm todos os termos de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="962db-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="962db-124">Os termos não precisam aparecer em nenhuma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="962db-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="962db-125">Os documentos que contêm mais termos de pesquisa têm valores de coluna de classificação mais altos.</span><span class="sxs-lookup"><span data-stu-id="962db-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="962db-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="962db-126">Examples</span></span>

<span data-ttu-id="962db-127">O exemplo a seguir procura documentos que contenham "computador", "software", "hardware" ou combinações dessas palavras:</span><span class="sxs-lookup"><span data-stu-id="962db-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="962db-128">Você não pode usar correspondência de palavra única e correspondência de frase no mesmo predicado FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="962db-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="962db-129">Ao executar consultas com contratações, você deve escapar do sinal de aspas na contratação ao usar FREETEXT, mas não ao usar CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="962db-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="962db-130">Por exemplo, a sintaxe a seguir falhará:</span><span class="sxs-lookup"><span data-stu-id="962db-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="962db-131">A sintaxe correta inclui duas aspas simples, não uma aspa dupla.</span><span class="sxs-lookup"><span data-stu-id="962db-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="962db-132">A sintaxe a seguir é realizada com sucesso:</span><span class="sxs-lookup"><span data-stu-id="962db-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="962db-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="962db-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="962db-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="962db-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="962db-135">Predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="962db-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="962db-136">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="962db-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="962db-137">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="962db-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="962db-138">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="962db-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



