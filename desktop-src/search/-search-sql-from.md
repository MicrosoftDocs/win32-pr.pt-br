---
description: Após a instrução SELECT, você usa a cláusula FROM para especificar onde pesquisar documentos correspondentes.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: Cláusula FROM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782861"
---
# <a name="from-clause"></a><span data-ttu-id="a5126-103">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="a5126-103">FROM Clause</span></span>

<span data-ttu-id="a5126-104">Após a instrução SELECT, você usa a cláusula FROM para especificar onde pesquisar documentos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a5126-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="a5126-105">A seguir está a sintaxe da cláusula FROM para uma consulta local:</span><span class="sxs-lookup"><span data-stu-id="a5126-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="a5126-106">Atualmente, o Windows Search dá suporte a apenas um catálogo, SystemIndex.</span><span class="sxs-lookup"><span data-stu-id="a5126-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="a5126-107">Para consultar o catálogo local de um computador remoto, inclua o nome do computador antes do catálogo e um caminho UNC (Convenção de nomenclatura universal) no computador remoto na cláusula SCOPE ou DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="a5126-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="a5126-108">Especifique um escopo como uma restrição na cláusula WHERE, conforme descrito no tópico [predicados de escopo e diretório](-search-sql-folderdepth.md) .</span><span class="sxs-lookup"><span data-stu-id="a5126-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="a5126-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5126-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="a5126-110">No segundo dos exemplos anteriores, a consulta tem como alvo um computador remoto chamado "zarascomputer".</span><span class="sxs-lookup"><span data-stu-id="a5126-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="a5126-111">Observe que esse nome de computador aparece nas cláusulas de e de escopo.</span><span class="sxs-lookup"><span data-stu-id="a5126-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="a5126-112">No terceiro exemplo, a consulta tem como alvo um nome de compartilhamento "Users" em um servidor chamado "Server" (no qual o caminho UNC seria \\ \\ usuários do servidor \\ ).</span><span class="sxs-lookup"><span data-stu-id="a5126-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5126-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5126-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a5126-114">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a5126-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a5126-115">Visão geral da sintaxe de pesquisa SQL</span><span class="sxs-lookup"><span data-stu-id="a5126-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="a5126-116">Instrução SELECT</span><span class="sxs-lookup"><span data-stu-id="a5126-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="a5126-117">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="a5126-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="a5126-118">Predicados de escopo e diretório</span><span class="sxs-lookup"><span data-stu-id="a5126-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



