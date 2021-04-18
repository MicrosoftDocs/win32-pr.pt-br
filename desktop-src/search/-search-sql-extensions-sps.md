---
description: O Microsoft Windows Search, com base nos padrões SQL-92 e SQL-99, melhora as pesquisas baseadas em documentos de texto completo em aplicativos de gerenciamento de documentos ou de gerenciamento de conhecimento.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Extensões do SQL no Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501468"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="78476-103">Extensões do SQL no Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="78476-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="78476-104">O Microsoft Windows Search, com base nos padrões SQL-92 e SQL-99, melhora as pesquisas baseadas em documentos de texto completo em aplicativos de gerenciamento de documentos ou de gerenciamento de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="78476-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="78476-105">Os aprimoramentos da pesquisa do Windows incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="78476-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="78476-106">128-nomes de identificador de caracteres</span><span class="sxs-lookup"><span data-stu-id="78476-106">128-Character Identifier Names</span></span>

<span data-ttu-id="78476-107">Enquanto SQL-92 e SQL-99 restringem colunas e outros identificadores para 18 caracteres, o Windows Search dá suporte a nomes de coluna de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="78476-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="78476-108">Para obter mais informações, consulte [Identificadores](-search-sql-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="78476-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="78476-109">Agrupando resultados por colunas</span><span class="sxs-lookup"><span data-stu-id="78476-109">Grouping Results by Columns</span></span>

<span data-ttu-id="78476-110">As consultas podem especificar como agrupar os resultados.</span><span class="sxs-lookup"><span data-stu-id="78476-110">Queries can specify how to group results.</span></span> <span data-ttu-id="78476-111">Você pode especificar os intervalos pelos quais agrupar e pode especificar mais de uma coluna para Agrupamento.</span><span class="sxs-lookup"><span data-stu-id="78476-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="78476-112">Por exemplo, você pode agrupar os resultados em um intervalo de tamanhos de arquivo (tamanho < 100, 100 <= tamanho < 1000; 1000 <= tamanho) e pode aninhar agrupamentos.</span><span class="sxs-lookup"><span data-stu-id="78476-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="78476-113">Para obter mais informações, consulte [agrupar em... SOBRE... Instrução](-search-sql-group-on-over.md).</span><span class="sxs-lookup"><span data-stu-id="78476-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="78476-114">Pesquisa de Diacritic-Insensitive</span><span class="sxs-lookup"><span data-stu-id="78476-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="78476-115">Além de Pesquisar que não diferencia maiúsculas de minúsculas, a pesquisa do Windows dá suporte à pesquisa que não é sensível a diacríticos (sinais de acentuação).</span><span class="sxs-lookup"><span data-stu-id="78476-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="78476-116">Para obter mais informações, consulte [sensibilidade de diacríticos em pesquisas](-search-sql-accentinsensitivitysearches.md).</span><span class="sxs-lookup"><span data-stu-id="78476-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="78476-117">Peso da coluna</span><span class="sxs-lookup"><span data-stu-id="78476-117">Column Weighting</span></span>

<span data-ttu-id="78476-118">As consultas que pesquisam mais de uma coluna podem especificar a importância de cada coluna.</span><span class="sxs-lookup"><span data-stu-id="78476-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="78476-119">Os predicados [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) dão suporte à ponderação de coluna.</span><span class="sxs-lookup"><span data-stu-id="78476-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="78476-120">Predicado nulo</span><span class="sxs-lookup"><span data-stu-id="78476-120">NULL Predicate</span></span>

<span data-ttu-id="78476-121">Embora a indexação de conteúdo de texto completo não tenha nenhum conjunto definido de colunas, as consultas podem exigir que os membros do conjunto de resultados tenham ou não colunas especificadas.</span><span class="sxs-lookup"><span data-stu-id="78476-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="78476-122">Não é possível diferenciar entre um documento tem uma propriedade especificada com o valor definido como **NULL** e um documento que não tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="78476-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="78476-123">Modificação de classificação</span><span class="sxs-lookup"><span data-stu-id="78476-123">Rank Modification</span></span>

<span data-ttu-id="78476-124">Você pode manipular a classificação de resultados da pesquisa usando [pesos](-search-sql-understandingrelevancevalues.md) em Propriedades e em grupos de propriedades com alias.</span><span class="sxs-lookup"><span data-stu-id="78476-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="78476-125">A coerção de classificação dá suporte à manipulação direta da classificação de relevância com base nos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="78476-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 



