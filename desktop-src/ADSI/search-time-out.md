---
title: Tempo limite de pesquisa
description: Um cliente também pode impor um limite de tempo que aguardará que um servidor retorne o conjunto de resultados.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- ADSI de tempo limite de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291779"
---
# <a name="search-time-out"></a><span data-ttu-id="e6ac4-104">Tempo limite de pesquisa</span><span class="sxs-lookup"><span data-stu-id="e6ac4-104">Search Time Out</span></span>

<span data-ttu-id="e6ac4-105">Um cliente também pode impor um limite de tempo que aguardará que um servidor retorne o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="e6ac4-106">O valor da opção "tempo limite de pesquisa" especifica esse limite.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="e6ac4-107">Quando o servidor não responde a uma consulta dentro do período de tempo especificado, o cliente pode interromper a pesquisa e tentar novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="e6ac4-108">A propriedade de tempo limite é útil quando um cliente solicita uma pesquisa assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="e6ac4-109">Em uma pesquisa assíncrona, o cliente faz uma solicitação e prossegue com outras tarefas enquanto aguarda o servidor retornar os resultados.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="e6ac4-110">É possível que o servidor possa ficar offline sem notificar o cliente.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="e6ac4-111">Nesse caso, o cliente não tem como reconhecer que o servidor ainda está processando a consulta, ou se ele parou de ser dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="e6ac4-112">A propriedade de tempo limite fornece ao cliente algum controle nessas instâncias.</span><span class="sxs-lookup"><span data-stu-id="e6ac4-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="e6ac4-113">Para obter mais informações sobre como usar a opção de tempo limite de pesquisa com uma interface de pesquisa específica, consulte:</span><span class="sxs-lookup"><span data-stu-id="e6ac4-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="e6ac4-114">Limite de tempo do cliente com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="e6ac4-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="e6ac4-115">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="e6ac4-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="e6ac4-116">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="e6ac4-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




