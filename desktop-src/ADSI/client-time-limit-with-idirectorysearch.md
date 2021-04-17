---
title: Limite de tempo do cliente com IDirectorySearch
description: Um cliente pode impor um limite de tempo para um servidor retornar o conjunto de resultados. Quando o servidor não responde a uma consulta dentro do período de tempo especificado, o cliente pode abandonar a pesquisa e tentar novamente mais tarde.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite de tempo do cliente com IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, limite de tempo do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755869"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="60f92-106">Limite de tempo do cliente com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="60f92-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="60f92-107">Um cliente pode impor um limite de tempo para um servidor retornar o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="60f92-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="60f92-108">Quando o servidor não responde a uma consulta dentro do período de tempo especificado, o cliente pode abandonar a pesquisa e tentar novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="60f92-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="60f92-109">A preferência de limite de tempo do cliente é útil quando um cliente solicita uma pesquisa assíncrona.</span><span class="sxs-lookup"><span data-stu-id="60f92-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="60f92-110">Em uma pesquisa assíncrona, o cliente faz uma solicitação e prossegue com outras tarefas enquanto aguarda o servidor retornar os resultados.</span><span class="sxs-lookup"><span data-stu-id="60f92-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="60f92-111">É possível que o servidor possa ficar offline sem notificar o cliente.</span><span class="sxs-lookup"><span data-stu-id="60f92-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="60f92-112">Nesse caso, o cliente não terá nenhuma notificação se o servidor ainda estiver processando a consulta ou se ele não estiver mais ativo.</span><span class="sxs-lookup"><span data-stu-id="60f92-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="60f92-113">A preferência de limite de tempo do cliente fornece ao cliente algum controle de situações como essa.</span><span class="sxs-lookup"><span data-stu-id="60f92-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="60f92-114">O padrão para o limite de tempo do cliente é sem limite.</span><span class="sxs-lookup"><span data-stu-id="60f92-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="60f92-115">Para definir um limite de tempo do cliente, defina uma opção de pesquisa de **\_ \_ tempo limite do ADS SEARCHPREF** com um valor **\_ inteiro ADSTYPE** que contenha o limite de tempo do cliente, em segundos, na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="60f92-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="60f92-116">Um limite de tempo de cliente igual A zero indica que não há limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="60f92-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="60f92-117">O exemplo de código a seguir mostra como definir o limite de tempo do cliente.</span><span class="sxs-lookup"><span data-stu-id="60f92-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




