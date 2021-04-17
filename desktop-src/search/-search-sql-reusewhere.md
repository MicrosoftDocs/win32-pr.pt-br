---
description: A cláusula WHERE em uma consulta especifica um conjunto de itens aos quais os resultados são correspondidos.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Função ReuseWhere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784596"
---
# <a name="reusewhere-function"></a><span data-ttu-id="3b961-103">Função ReuseWhere</span><span class="sxs-lookup"><span data-stu-id="3b961-103">ReuseWhere Function</span></span>

<span data-ttu-id="3b961-104">A cláusula [Where](-search-sql-where.md) em uma consulta especifica um conjunto de itens aos quais os resultados são correspondidos.</span><span class="sxs-lookup"><span data-stu-id="3b961-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="3b961-105">As consultas subsequentes podem compartilhar o trabalho executado para uma consulta anterior usando a função ReuseWhere em uma nova cláusula WHERE de consulta.</span><span class="sxs-lookup"><span data-stu-id="3b961-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="3b961-106">As consultas que tiram proveito dessa função são executadas mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3b961-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="3b961-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b961-107">Examples</span></span>

<span data-ttu-id="3b961-108">O cenário a seguir mostra como usar a função ReuseWhere:</span><span class="sxs-lookup"><span data-stu-id="3b961-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="3b961-109">Você emite a seguinte consulta:</span><span class="sxs-lookup"><span data-stu-id="3b961-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="3b961-110">No conjunto de linhas retornado, você obtém uma [id where](-search-sql-rowset-properties.md), *Query1WhereID*.</span><span class="sxs-lookup"><span data-stu-id="3b961-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="3b961-111">A ID WHERE é uma propriedade Rowset com PROPset {aa6ee6b0-e828-11D0-B2-3E-00-AA-00-47-FC-01}, PROPID 8 e Type UI4.</span><span class="sxs-lookup"><span data-stu-id="3b961-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="3b961-112">Você emite uma segunda consulta com a função ReuseWhere, passando o *Query1WhereID* da etapa 2:</span><span class="sxs-lookup"><span data-stu-id="3b961-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="3b961-113">A segunda consulta é equivalente à seguinte:</span><span class="sxs-lookup"><span data-stu-id="3b961-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="3b961-114">A função ReuseWhere pode ser usada como na cláusula [Where](-search-sql-where.md) .</span><span class="sxs-lookup"><span data-stu-id="3b961-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b961-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b961-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3b961-116">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3b961-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b961-117">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="3b961-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="3b961-118">Propriedades do conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="3b961-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



