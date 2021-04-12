---
title: Comunicação Single-Threaded e multithread
description: Comunicação Single-Threaded e multithread
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292015"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="0b079-103">Comunicação Single-Threaded e multithread</span><span class="sxs-lookup"><span data-stu-id="0b079-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="0b079-104">Um cliente ou servidor que dá suporte a Apartments de thread único e multi-threaded terá um apartamento multi-threaded, contendo todos os threads inicializados como de thread livre e um ou mais Apartments de thread único.</span><span class="sxs-lookup"><span data-stu-id="0b079-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="0b079-105">Os ponteiros de interface devem ser empacotados entre Apartments, mas podem ser usados sem marshaling em um apartamento.</span><span class="sxs-lookup"><span data-stu-id="0b079-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="0b079-106">As chamadas para objetos em um apartamento de thread único serão sincronizadas pelo COM.</span><span class="sxs-lookup"><span data-stu-id="0b079-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="0b079-107">As chamadas para objetos no apartamento multi-threaded não serão sincronizadas pelo COM.</span><span class="sxs-lookup"><span data-stu-id="0b079-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="0b079-108">Todas as informações sobre Apartments de thread único se aplicam aos threads marcados como modelo de apartamento, e todas as informações em Apartments multithread se aplicam a todos os threads marcados como livres de threads.</span><span class="sxs-lookup"><span data-stu-id="0b079-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="0b079-109">As regras de Threading Apartment se aplicam à comunicação entre apartamento, exigindo que os ponteiros de interface sejam empacotados entre Apartments com chamadas para [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) e [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), conforme descrito em [Apartments de thread único](single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="0b079-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="0b079-110">Algumas considerações especiais se aplicam ao lidar com servidores em processo.</span><span class="sxs-lookup"><span data-stu-id="0b079-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="0b079-111">Para obter mais informações, consulte [problemas de thread de servidor em processo](in-process-server-threading-issues.md).</span><span class="sxs-lookup"><span data-stu-id="0b079-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0b079-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b079-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b079-113">Acessando interfaces em Apartments</span><span class="sxs-lookup"><span data-stu-id="0b079-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="0b079-114">Escolhendo o modelo de Threading</span><span class="sxs-lookup"><span data-stu-id="0b079-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="0b079-115">Apartments multithread</span><span class="sxs-lookup"><span data-stu-id="0b079-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="0b079-116">Problemas de Threading do servidor em processo</span><span class="sxs-lookup"><span data-stu-id="0b079-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="0b079-117">Processos, threads e Apartments</span><span class="sxs-lookup"><span data-stu-id="0b079-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="0b079-118">Apartments de thread único</span><span class="sxs-lookup"><span data-stu-id="0b079-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




