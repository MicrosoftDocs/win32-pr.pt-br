---
description: Membros do CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membros do CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766981"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="60f62-103">Membros do CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="60f62-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="60f62-104">Os blocos de espera armazenam as informações sobre a espera registrada no pool de threads.</span><span class="sxs-lookup"><span data-stu-id="60f62-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="60f62-105">Ele inclui os identificadores de espera retornados pela chamada [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) e um ponteiro para a estrutura de contexto.</span><span class="sxs-lookup"><span data-stu-id="60f62-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="60f62-106">Cada bloco na matriz é para um grafo em um dos objetos Stream.</span><span class="sxs-lookup"><span data-stu-id="60f62-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="60f62-107">O deslocamento de um bloco nessa matriz é o mesmo que o deslocamento do fluxo que possui o grafo.</span><span class="sxs-lookup"><span data-stu-id="60f62-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
