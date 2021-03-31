---
title: Balanceamento de carga RPC
description: Balanceamento de carga RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004961"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="a7fff-103">Balanceamento de carga RPC</span><span class="sxs-lookup"><span data-stu-id="a7fff-103">RPC Load Balancing</span></span>

<span data-ttu-id="a7fff-104">O balanceamento de carga RPC da Microsoft destina-se a fornecer uma solução escalonável para cenários que exigem uma alta carga de tráfego [RPC sobre http](remote-procedure-calls-using-rpc-over-http.md) .</span><span class="sxs-lookup"><span data-stu-id="a7fff-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="a7fff-105">A principal finalidade do Load Balancer de RPC é garantir que o tráfego RPC/HTTP possa ser atendido por um farm de servidores para melhorar a escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="a7fff-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="a7fff-106">Para conseguir isso, o RPC deve garantir que todas as conexões de um processo de cliente sejam atendidas pelo mesmo ponto de extremidade do servidor no farm de servidores.</span><span class="sxs-lookup"><span data-stu-id="a7fff-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="a7fff-107">A Load Balancer RPC é implementada como um serviço que é executado em conjunto com o serviço RPC sobre proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="a7fff-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="a7fff-108">Para habilitar o balanceamento de carga, o serviço de balanceamento de carga RPC em execução em cada um dos servidores se comunica entre si para determinar o servidor preferencial para a conexão inicial do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7fff-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="a7fff-109">Esse processo é chamado de arbitragem e ocorre no momento da conexão inicial do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7fff-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="a7fff-110">Para reduzir o tráfego entre servidores, o serviço de balanceamento de carga RPC escolhe o ponto de extremidade local para atender à conexão se o cliente ainda não estiver associado a um servidor.</span><span class="sxs-lookup"><span data-stu-id="a7fff-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="a7fff-111">Para uma determinada conexão de cliente, o resultado da arbitragem é uma das duas possibilidades:</span><span class="sxs-lookup"><span data-stu-id="a7fff-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="a7fff-112">Se o cliente já tiver feito uma conexão, o servidor a receber primeiro a conexão tratará as conexões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a7fff-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="a7fff-113">Se essa for a primeira conexão do cliente, a arbitragem resultará no servidor local que manipula a conexão e, portanto, todas as conexões do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7fff-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="a7fff-114">Essas informações, uma vez determinadas, serão confirmadas em outros serviços de Load Balancer de RPC no farm de servidores, informando-os sobre o servidor que lida com todas as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="a7fff-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="a7fff-115">Esta seção fornece uma visão geral do balanceamento de carga RPC nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a7fff-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="a7fff-116">Implantando o balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="a7fff-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="a7fff-117">Configurando o balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="a7fff-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="a7fff-118">Práticas recomendadas de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="a7fff-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="a7fff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7fff-119">Requirements</span></span>

<span data-ttu-id="a7fff-120">O serviço de balanceamento de carga RPC tem suporte em servidores que executam o Windows Server 2008 R2 ou posterior e clientes que executam o Windows 7 ou versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="a7fff-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="a7fff-121">O serviço de proxy RPC, o serviço de balanceamento de carga RPC e os pontos de extremidade do servidor devem estar em execução no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="a7fff-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="a7fff-122">Além disso, todos os servidores no farm de servidores devem ser capazes de atender ao ponto de extremidade solicitado.</span><span class="sxs-lookup"><span data-stu-id="a7fff-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="a7fff-123">Para obter informações sobre como configurar o serviço de proxy RPC e o serviço de balanceamento de carga RPC, consulte [Configurando computadores para RPC sobre http](configuring-computers-for-rpc-over-http.md) e [Configurando o balanceamento de carga](configuring-load-balancing.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a7fff-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="a7fff-124">Limitações</span><span class="sxs-lookup"><span data-stu-id="a7fff-124">Limitations</span></span>

<span data-ttu-id="a7fff-125">Neste momento, o balanceamento de carga RPC dá suporte a apenas um farm de servidores por recurso.</span><span class="sxs-lookup"><span data-stu-id="a7fff-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="a7fff-126">Todos os servidores em todos os farms de servidores também devem ser capazes de atender a todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="a7fff-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




