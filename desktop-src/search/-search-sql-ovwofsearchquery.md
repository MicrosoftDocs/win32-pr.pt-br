---
description: O Windows Search linguagem SQL (SQL) é semelhante a uma consulta SQL padrão.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Visão geral da sintaxe SQL do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010389"
---
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="aba83-103">Visão geral da sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="aba83-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="aba83-104">O Windows Search linguagem SQL (SQL) é semelhante a uma consulta SQL padrão.</span><span class="sxs-lookup"><span data-stu-id="aba83-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="aba83-105">Ele é mostrado nas duas sintaxes a seguir:</span><span class="sxs-lookup"><span data-stu-id="aba83-105">It is shown in the following two syntaxes:</span></span>


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

<span data-ttu-id="aba83-106">No exemplo de consulta a seguir, os valores de contagem de página e data de criação são retornados para todos os documentos que têm mais de 50 páginas, classificados é ordem crescente de contagem de páginas.</span><span class="sxs-lookup"><span data-stu-id="aba83-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="aba83-107">A sintaxe de consulta do Windows Search dá suporte a várias opções, permitindo consultas mais complicadas.</span><span class="sxs-lookup"><span data-stu-id="aba83-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="aba83-108">A tabela a seguir descreve cada cláusula nas instruções SELECT ou GROUP ON e os recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="aba83-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="aba83-109">Cláusula</span><span class="sxs-lookup"><span data-stu-id="aba83-109">Clause</span></span>                                              | <span data-ttu-id="aba83-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="aba83-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aba83-111">AGRUPAR EM... SOBRE...</span><span class="sxs-lookup"><span data-stu-id="aba83-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="aba83-112">Especifica como agrupar os resultados retornados pela consulta.</span><span class="sxs-lookup"><span data-stu-id="aba83-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="aba83-113">Você pode especificar os intervalos pelos quais agrupar e especificar mais de uma coluna para Agrupamento.</span><span class="sxs-lookup"><span data-stu-id="aba83-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="aba83-114">Por exemplo, você pode agrupar os resultados em um intervalo de tamanhos de arquivo (tamanho < 100, 100 <= tamanho < 1000; 1000 <= tamanho) e aninhar agrupamentos.</span><span class="sxs-lookup"><span data-stu-id="aba83-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="aba83-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="aba83-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="aba83-116">Especifica as colunas retornadas pela consulta.</span><span class="sxs-lookup"><span data-stu-id="aba83-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="aba83-117">FROM</span><span class="sxs-lookup"><span data-stu-id="aba83-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="aba83-118">Especifica o computador e o catálogo a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="aba83-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="aba83-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="aba83-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="aba83-120">Especifica o que constitui um documento correspondente.</span><span class="sxs-lookup"><span data-stu-id="aba83-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="aba83-121">Essa cláusula tem muitas opções, permitindo um controle avançado sobre os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="aba83-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="aba83-122">Por exemplo, você pode fazer a correspondência com palavras, frases, formas de palavras informativas, cadeias de caracteres, valores numéricos e de bit-chave e matrizes com vários valores.</span><span class="sxs-lookup"><span data-stu-id="aba83-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="aba83-123">Você também pode aplicar pesos estatísticos às condições de correspondência e combinar condições de correspondência com operadores boolianos.</span><span class="sxs-lookup"><span data-stu-id="aba83-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="aba83-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="aba83-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="aba83-125">Especifica a ordem de classificação dos resultados retornados pela consulta.</span><span class="sxs-lookup"><span data-stu-id="aba83-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="aba83-126">Você pode especificar mais de um campo no qual os resultados são classificados e pode usar ordenação crescente ou decrescente.</span><span class="sxs-lookup"><span data-stu-id="aba83-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="aba83-127">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="aba83-127">Code samples</span></span>

<span data-ttu-id="aba83-128">O exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e o Windows Search por meio do SQL.</span><span class="sxs-lookup"><span data-stu-id="aba83-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="aba83-129">O exemplo de código WSOleDB ilustra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e dois métodos adicionais para recuperar os resultados do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="aba83-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="aba83-130">Ambos os exemplos estão disponíveis no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="aba83-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aba83-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aba83-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="aba83-132">Referência</span><span class="sxs-lookup"><span data-stu-id="aba83-132">Reference</span></span>

[<span data-ttu-id="aba83-133">Literais</span><span class="sxs-lookup"><span data-stu-id="aba83-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="aba83-134">Usando pesquisas localizadas</span><span class="sxs-lookup"><span data-stu-id="aba83-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="aba83-135">Noções básicas sobre valores de relevância</span><span class="sxs-lookup"><span data-stu-id="aba83-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="aba83-136">Mapeamentos de propriedade</span><span class="sxs-lookup"><span data-stu-id="aba83-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="aba83-137">Sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="aba83-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="aba83-138">Conceitual</span><span class="sxs-lookup"><span data-stu-id="aba83-138">Conceptual</span></span>

[<span data-ttu-id="aba83-139">Extensões do SQL no Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="aba83-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="aba83-140">Recursos do SQL não disponíveis no Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="aba83-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="aba83-141">Identificadores</span><span class="sxs-lookup"><span data-stu-id="aba83-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="aba83-142">Distinção de maiúsculas e minúsculas em pesquisas</span><span class="sxs-lookup"><span data-stu-id="aba83-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="aba83-143">Sensibilidade de diacríticos em pesquisas</span><span class="sxs-lookup"><span data-stu-id="aba83-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="aba83-144">Convertendo o tipo de dados de uma coluna</span><span class="sxs-lookup"><span data-stu-id="aba83-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="aba83-145">Mapeamentos de tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aba83-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
