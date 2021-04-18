---
title: Limite de tempo de pesquisa
description: Quando você solicita uma pesquisa em um servidor que está sob uma carga de trabalho pesada, convém instruir o servidor para restringir a pesquisa a um limite de tempo especificado.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- ADSI do limite de tempo de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756315"
---
# <a name="search-time-limit"></a><span data-ttu-id="1ba39-104">Limite de tempo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1ba39-104">Search Time Limit</span></span>

<span data-ttu-id="1ba39-105">Quando você solicita uma pesquisa em um servidor que está sob uma carga de trabalho pesada, convém instruir o servidor para restringir a pesquisa a um limite de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="1ba39-105">When you request a search on a server that is under a heavy workload, you may want to instruct the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="1ba39-106">Por exemplo, para executar um aplicativo para gerar um relatório semanal em um servidor que esteja executando quase a capacidade e para evitar maximizar o tempo de CPU e impedir que outros trabalhos sejam executados, você pode definir o tempo de pesquisa para um valor pequeno e executar novamente o aplicativo mais tarde se ele falhar ao gerar o relatório.</span><span class="sxs-lookup"><span data-stu-id="1ba39-106">For example, to execute an application to generate a weekly report on a server that is running near capacity, and to avoid maximizing the CPU time and preventing other jobs from running, you can set the search time to a small value and rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="1ba39-107">Alguns servidores podem impor seu próprio limite de tempo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1ba39-107">Some servers can impose their own administrative time limit.</span></span> <span data-ttu-id="1ba39-108">Nesses casos, se você especificar um valor de limite de tempo de pesquisa maior que o limite de tempo administrativo, o servidor ignorará sua especificação e usará seu limite de tempo administrativo interno em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1ba39-108">In these cases, if you specify a search time limit value greater than the administrative time limit, the server ignores your specification and use its internal administrative time limit instead.</span></span>

<span data-ttu-id="1ba39-109">Para obter mais informações sobre como usar a opção de limite de tempo de pesquisa com uma interface de pesquisa específica, consulte:</span><span class="sxs-lookup"><span data-stu-id="1ba39-109">For more information about using the search time limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="1ba39-110">Limite de tempo do servidor com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="1ba39-110">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="1ba39-111">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="1ba39-111">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="1ba39-112">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="1ba39-112">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




