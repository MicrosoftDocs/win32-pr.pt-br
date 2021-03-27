---
title: Informações de uso de memória do processo
description: A função GetProcessMemoryInfo usa um identificador de processo como entrada e preenche uma \_ estrutura de contadores de memória de processo \_ com informações sobre as estatísticas de memória para o processo.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822863"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="6a555-103">Informações de uso de memória do processo</span><span class="sxs-lookup"><span data-stu-id="6a555-103">Process Memory Usage Information</span></span>

<span data-ttu-id="6a555-104">A função [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) usa um identificador de processo como entrada e preenche uma estrutura de [**\_ \_ contadores de memória de processo**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) com informações sobre as estatísticas de memória para o processo.</span><span class="sxs-lookup"><span data-stu-id="6a555-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="6a555-105">O membro **CB** recebe o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="6a555-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="6a555-106">O membro **PageFaultCount** recebe o número de falhas de página.</span><span class="sxs-lookup"><span data-stu-id="6a555-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="6a555-107">Os membros restantes recebem o uso de memória atual e de pico nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="6a555-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="6a555-108">conjunto de trabalho</span><span class="sxs-lookup"><span data-stu-id="6a555-108">working set</span></span>
-   <span data-ttu-id="6a555-109">Pool Paginável</span><span class="sxs-lookup"><span data-stu-id="6a555-109">paged pool</span></span>
-   <span data-ttu-id="6a555-110">pool não paginável</span><span class="sxs-lookup"><span data-stu-id="6a555-110">nonpaged pool</span></span>
-   <span data-ttu-id="6a555-111">Page</span><span class="sxs-lookup"><span data-stu-id="6a555-111">pagefile</span></span>

<span data-ttu-id="6a555-112">O *conjunto de trabalho* é a quantidade de memória mapeada fisicamente para o contexto do processo em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="6a555-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="6a555-113">A memória no *pool paginável* é a memória do sistema que pode ser transferida para o arquivo de paginação no disco (paginável) quando não está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="6a555-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="6a555-114">A memória no *pool não paginável* é a memória do sistema que não pode ser paginada para o disco, desde que os objetos correspondentes sejam alocados.</span><span class="sxs-lookup"><span data-stu-id="6a555-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="6a555-115">O uso de *arquivo de paginação* representa a quantidade de memória reservada para o processo no arquivo de paginação do sistema.</span><span class="sxs-lookup"><span data-stu-id="6a555-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="6a555-116">Quando a utilização de memória é muito alta, as páginas do Gerenciador de memória virtual selecionam a memória no disco.</span><span class="sxs-lookup"><span data-stu-id="6a555-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="6a555-117">Quando um thread precisa de uma página que não está na memória, o Gerenciador de memória o recarrega a partir do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="6a555-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




