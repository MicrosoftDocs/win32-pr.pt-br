---
title: Proxy de serviço e sessões
description: O proxy de serviço tem comportamentos especiais para associações de canal baseadas em sessão e não em sessão.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Serviços Web de sessões e proxy de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008619"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="247f2-106">Proxy de serviço e sessões</span><span class="sxs-lookup"><span data-stu-id="247f2-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="247f2-107">O [proxy de serviço](service-proxy.md) tem comportamentos especiais para associações de canal baseadas em sessão e não em sessão.</span><span class="sxs-lookup"><span data-stu-id="247f2-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="247f2-108">O proxy de serviço fornece semântica baseada em sessão se a associação de canal subjacente for baseada em sessão.</span><span class="sxs-lookup"><span data-stu-id="247f2-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="247f2-109">Nesse caso, um único canal é usado para chamadas de serviço.</span><span class="sxs-lookup"><span data-stu-id="247f2-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="247f2-110">No entanto, se a associação de canal não for baseada em sessão, o proxy de serviço criará um canal separado para cada chamada.</span><span class="sxs-lookup"><span data-stu-id="247f2-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="247f2-111">Observe, no entanto, que os canais não baseados em sessão são agrupados e talvez reutilizados.</span><span class="sxs-lookup"><span data-stu-id="247f2-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="247f2-112">Ao reutilizar um canal, o proxy de serviço mantém o canal aberto se o canal subjacente não tiver falhado ou se a chamada em um canal resultar na falha do proxy de serviço no canal.</span><span class="sxs-lookup"><span data-stu-id="247f2-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="247f2-113">Observe que.</span><span class="sxs-lookup"><span data-stu-id="247f2-113">Note that.</span></span> <span data-ttu-id="247f2-114">exceto no caso de uma falha, quando um canal é aberto, ele é mantido aberto, desde que o proxy de serviço esteja aberto e seja fechado somente quando o proxy de serviço é fechado.</span><span class="sxs-lookup"><span data-stu-id="247f2-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="247f2-115">Se a associação de canal for baseada em sessão e se as falhas de canal subjacentes, a máquina de estado do proxy de serviço passará para o estado de [**falha do estado do \_ proxy de serviço \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="247f2-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="247f2-116">No caso de uma associação de canal baseada em não sessão, uma falha no canal subjacente não faz com que o proxy faça a transição para o estado de **\_ \_ \_ \_ falha de proxy do WS Service** .</span><span class="sxs-lookup"><span data-stu-id="247f2-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="247f2-117">Para obter mais informações sobre o proxy de serviço e sua relação com o estado, consulte o tópico [proxy de serviço](service-proxy.md) .</span><span class="sxs-lookup"><span data-stu-id="247f2-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="247f2-118">Para obter exemplos de associações de canal diferentes, consulte os exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="247f2-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="247f2-119">Associação de canal de não sessão, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="247f2-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="247f2-120">Associação de canal baseada em sessão, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="247f2-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




