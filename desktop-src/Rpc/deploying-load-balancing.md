---
title: Implantando o balanceamento de carga
description: Implantando o balanceamento de carga
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159604"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="5e96a-103">Implantando o balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="5e96a-103">Deploying Load Balancing</span></span>

<span data-ttu-id="5e96a-104">O ambiente de implantação típico e o caso de uso é o que o balanceador de carga RPC é utilizado é mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="5e96a-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![balanceamento de carga RPC](images/rpc-load-balancing.png)

1.  <span data-ttu-id="5e96a-106">O cliente RPC faz uma conexão RPC/HTTP com o farm de servidores.</span><span class="sxs-lookup"><span data-stu-id="5e96a-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="5e96a-107">A conexão é encaminhada pela rede para um balanceador de carga de front-end</span><span class="sxs-lookup"><span data-stu-id="5e96a-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="5e96a-108">O balanceador de carga de front-end escolhe um servidor para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="5e96a-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="5e96a-109">Neste exemplo, o balanceador de carga de front-end encaminha a conexão para o servidor 1.</span><span class="sxs-lookup"><span data-stu-id="5e96a-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="5e96a-110">O serviço de balanceador de carga RPC arbitra a conexão.</span><span class="sxs-lookup"><span data-stu-id="5e96a-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="5e96a-111">Ele determina que essa é a primeira conexão do cliente e associa a conexão ao servidor local, servidor 1.</span><span class="sxs-lookup"><span data-stu-id="5e96a-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="5e96a-112">O cliente faz uma segunda solicitação RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="5e96a-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="5e96a-113">A solicitação é encaminhada pela rede para o balanceador de carga de front-end.</span><span class="sxs-lookup"><span data-stu-id="5e96a-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="5e96a-114">O balanceador de carga de front-end escolhe um servidor para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="5e96a-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="5e96a-115">Nesse caso, o balanceador de carga de front-end escolhe o servidor 2 para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="5e96a-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="5e96a-116">O serviço de Load Balancer RPC arbitra a conexão.</span><span class="sxs-lookup"><span data-stu-id="5e96a-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="5e96a-117">Ele reconhece que as conexões desse cliente estão sendo atendidas pelo servidor 1.</span><span class="sxs-lookup"><span data-stu-id="5e96a-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="5e96a-118">A conexão é encaminhada para o servidor 1.</span><span class="sxs-lookup"><span data-stu-id="5e96a-118">The connection is forwarded to Server 1.</span></span>

 

 




