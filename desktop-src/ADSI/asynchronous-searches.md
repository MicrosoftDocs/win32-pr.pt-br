---
title: Pesquisas assíncronas
description: A habilitação da pesquisa assíncrona (Async) resulta em uma chamada para GetFirstRow ou a primeira chamada para blocos GetNextRow até que a primeira entrada seja retornada do servidor.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI de pesquisas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915916"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="d16dd-104">Pesquisas assíncronas</span><span class="sxs-lookup"><span data-stu-id="d16dd-104">Asynchronous Searches</span></span>

<span data-ttu-id="d16dd-105">A habilitação da pesquisa assíncrona (Async) resulta em uma chamada para **GetFirstRow** ou a primeira chamada para blocos **GetNextRow** até que a primeira entrada seja retornada do servidor.</span><span class="sxs-lookup"><span data-stu-id="d16dd-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="d16dd-106">Ou seja, se a pesquisa no servidor exigir muito tempo, os primeiros resultados serão retornados rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d16dd-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="d16dd-107">Isso pode ajudar ao preencher uma caixa de listagem com os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d16dd-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="d16dd-108">Os resultados da pesquisa são exibidos à medida que são retornados.</span><span class="sxs-lookup"><span data-stu-id="d16dd-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="d16dd-109">Se Async estiver desabilitado, a primeira chamada para **GetFirstRow** ou **GetNextRow** será bloqueada até que o servidor Calcule todo o conjunto de resultados e retorna.</span><span class="sxs-lookup"><span data-stu-id="d16dd-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="d16dd-110">Somente a primeira linha é retornada.</span><span class="sxs-lookup"><span data-stu-id="d16dd-110">Only then is the first row returned.</span></span> <span data-ttu-id="d16dd-111">Isso não é recomendado se o conjunto de resultados deve ser grande.</span><span class="sxs-lookup"><span data-stu-id="d16dd-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="d16dd-112">Se a paginação e a Async estiverem habilitadas, a primeira chamada para **GetFirstRow** ou **GetNextRow** será bloqueada até que o servidor gere e envie a primeira página de resultados.</span><span class="sxs-lookup"><span data-stu-id="d16dd-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="d16dd-113">Se um tamanho de página razoável tiver sido definido, os resultados aparecerão imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d16dd-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="d16dd-114">Mais importante, se os resultados da pesquisa forem muito grandes e você pesquisar por uma entrada específica, não será necessário solicitar mais resultados do servidor depois de encontrar as entradas que lhe interessam.</span><span class="sxs-lookup"><span data-stu-id="d16dd-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="d16dd-115">A pesquisa assíncrona paginável fornece um controle fino de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d16dd-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="d16dd-116">Isso será útil se os resultados da pesquisa puderem ser muito grandes e exigirem tempo extensivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="d16dd-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="d16dd-117">Para obter mais informações sobre como usar pesquisas assíncronas com uma interface de pesquisa específica, consulte:</span><span class="sxs-lookup"><span data-stu-id="d16dd-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="d16dd-118">Pesquisas síncronas e assíncronas com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="d16dd-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="d16dd-119">Pesquisando com ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="d16dd-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="d16dd-120">Pesquisando com OLE DB</span><span class="sxs-lookup"><span data-stu-id="d16dd-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




