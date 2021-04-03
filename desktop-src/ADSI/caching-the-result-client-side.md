---
title: Armazenando em cache o resultado (lado do cliente)
description: O armazenamento em cache do lado do cliente armazena o conjunto de resultados na memória do cliente, fornecendo aprimoramentos de desempenho para o lado do cliente.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Caching do resultado (lado do cliente) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915911"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="76c27-104">Armazenando em cache o resultado (lado do cliente)</span><span class="sxs-lookup"><span data-stu-id="76c27-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="76c27-105">O armazenamento em cache do lado do cliente armazena o conjunto de resultados na memória do cliente, fornecendo aprimoramentos de desempenho para o lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="76c27-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="76c27-106">Um cliente pode revisitar um objeto repetidamente sem várias viagens para o servidor.</span><span class="sxs-lookup"><span data-stu-id="76c27-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="76c27-107">Por padrão, a ADSI armazena em cache o conjunto de resultados para os clientes.</span><span class="sxs-lookup"><span data-stu-id="76c27-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="76c27-108">Isso permite que a ADSI forneça aos clientes suporte ao cursor do tipo SQL.</span><span class="sxs-lookup"><span data-stu-id="76c27-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="76c27-109">Você pode iterar em um determinado conjunto de resultados várias vezes.</span><span class="sxs-lookup"><span data-stu-id="76c27-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="76c27-110">A ADSI também permite que os clientes desliguem o cache para reduzir os requisitos de memória.</span><span class="sxs-lookup"><span data-stu-id="76c27-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="76c27-111">Se o cache do lado do cliente estiver desabilitado, o cliente não manterá o conjunto de resultados na memória.</span><span class="sxs-lookup"><span data-stu-id="76c27-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="76c27-112">Cada linha é liberada depois que o aplicativo a recupera.</span><span class="sxs-lookup"><span data-stu-id="76c27-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="76c27-113">Desabilitar o armazenamento em cache do lado do cliente pode ser útil para diminuir os requisitos de memória do lado do cliente nesses casos, como quando você pretende fazer uma passagem única do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="76c27-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="76c27-114">No entanto, quando os clientes optam por não armazenar o resultado em cache, eles oferecem suporte ao cursor.</span><span class="sxs-lookup"><span data-stu-id="76c27-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="76c27-115">Para obter mais informações sobre o cache de resultados com uma interface de pesquisa específica, consulte:</span><span class="sxs-lookup"><span data-stu-id="76c27-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="76c27-116">Cache de resultados com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="76c27-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="76c27-117">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="76c27-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="76c27-118">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="76c27-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




