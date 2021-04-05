---
description: Em um banco de dados relacional, as linhas retornadas por uma consulta de pesquisa devem atender a todas as condições chamadas para pela consulta. Por outro lado, uma consulta do Windows Search pode retornar documentos que atendam aos critérios de pesquisa a graus variados.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Noções básicas sobre valores de relevância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826905"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="e13f7-104">Noções básicas sobre valores de relevância</span><span class="sxs-lookup"><span data-stu-id="e13f7-104">Understanding Relevance Values</span></span>

<span data-ttu-id="e13f7-105">Em um banco de dados relacional, as linhas retornadas por uma consulta de pesquisa devem atender a todas as condições chamadas para pela consulta.</span><span class="sxs-lookup"><span data-stu-id="e13f7-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="e13f7-106">Por outro lado, uma consulta do Windows Search pode retornar documentos que atendam aos critérios de pesquisa a graus variados.</span><span class="sxs-lookup"><span data-stu-id="e13f7-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="e13f7-107">Por exemplo, uma pesquisa pelo termo "programa" em um banco de dados relacional produz registros que contêm essa grafia específica da palavra.</span><span class="sxs-lookup"><span data-stu-id="e13f7-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="e13f7-108">Se um registro contém uma ou 100 instâncias da palavra não tem impacto sobre os resultados.</span><span class="sxs-lookup"><span data-stu-id="e13f7-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="e13f7-109">Por outro lado, o Windows Search retorna um valor de relevância associado aos documentos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="e13f7-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="e13f7-110">A relevância dos documentos com "programa" no título é maior que aqueles que contêm a palavra somente no último parágrafo.</span><span class="sxs-lookup"><span data-stu-id="e13f7-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="e13f7-111">Da mesma forma, os documentos que contêm variações do termo de pesquisa, por exemplo, "programas" e "programação" também correspondem e são retornados pela consulta.</span><span class="sxs-lookup"><span data-stu-id="e13f7-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="e13f7-112">As consultas do Windows Search retornam valores de relevância de inteiros na coluna chamada "Rank".</span><span class="sxs-lookup"><span data-stu-id="e13f7-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="e13f7-113">Além disso:</span><span class="sxs-lookup"><span data-stu-id="e13f7-113">In addition:</span></span>

-   <span data-ttu-id="e13f7-114">Os valores de classificação retornados pela consulta são inteiros variando de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="e13f7-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="e13f7-115">Valores de classificação mais altos indicam documentos que correspondem melhor às condições de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e13f7-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="e13f7-116">Os valores de classificação se aplicam somente à consulta atual, portanto, eles não podem ser comparados aos resultados entre consultas.</span><span class="sxs-lookup"><span data-stu-id="e13f7-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="e13f7-117">Os valores de classificação são relativos aos outros documentos que correspondem à consulta.</span><span class="sxs-lookup"><span data-stu-id="e13f7-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="e13f7-118">Portanto, o valor de classificação de um documento específico depende dos outros documentos que também correspondem à consulta.</span><span class="sxs-lookup"><span data-stu-id="e13f7-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="e13f7-119">Valores de classificação para itens que correspondem a um predicado puramente relacional são 1000.</span><span class="sxs-lookup"><span data-stu-id="e13f7-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="e13f7-120">Você pode manipular os valores de classificação retornados usando pesos de coluna nos predicados de cláusula [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) Where e a cláusula Rank by.</span><span class="sxs-lookup"><span data-stu-id="e13f7-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



