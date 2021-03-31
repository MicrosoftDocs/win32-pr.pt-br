---
title: Tenha cuidado com outros pontos de extremidade RPC em execução no mesmo processo
description: Quando um aplicativo reside em um processo com outros servidores RPC, todos os aplicativos escutam em todos os protocolos.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636259"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a><span data-ttu-id="a8446-103">Tenha cuidado com outros pontos de extremidade RPC em execução no mesmo processo</span><span class="sxs-lookup"><span data-stu-id="a8446-103">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>

<span data-ttu-id="a8446-104">Quando um aplicativo reside em um processo com outros servidores RPC, todos os aplicativos escutam em todos os protocolos.</span><span class="sxs-lookup"><span data-stu-id="a8446-104">When an application resides in a process with other RPC servers, all applications listen on all protocols.</span></span> <span data-ttu-id="a8446-105">Dessa forma, se um componente chamar [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* apenas para o LRPC, ele não estará necessariamente acessível apenas pelo LRPC.</span><span class="sxs-lookup"><span data-stu-id="a8446-105">As such, if a component calls [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* for LRPC only, it is not necessarily accessible over LRPC only.</span></span> <span data-ttu-id="a8446-106">Ele pode estar acessível em outros protocolos, já que outros servidores RPC no processo podem estar escutando em pipes ou soquetes (por exemplo).</span><span class="sxs-lookup"><span data-stu-id="a8446-106">It may be accessible over other protocols, since other RPC servers in the process may be listening on pipes or sockets (for example).</span></span>

<span data-ttu-id="a8446-107">Semelhante a identificadores estritos de contexto, não colocar outro ponto de extremidade no processo não significa que não exista outro ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a8446-107">Similar to strict context handles, not putting another endpoint in the process does not mean another endpoint does not exist.</span></span> <span data-ttu-id="a8446-108">Independentemente de como você registra seu servidor, não há nenhuma associação especial entre sua interface e seu ponto de extremidade; todas as interfaces podem ser chamadas em todos os pontos de extremidade nesse processo.</span><span class="sxs-lookup"><span data-stu-id="a8446-108">Regardless of how you register your server, there is no special association between your interface and your endpoint; all interfaces are callable on all endpoints in that process.</span></span> <span data-ttu-id="a8446-109">Essa é outra razão pela qual o modelo de segurança do ponto de extremidade é ineficaz; se um descritor de segurança for colocado em um ponto de extremidade, os invasores poderão chamar a interface em outro ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a8446-109">This is another reason why the endpoint security model is ineffective; if a security descriptor is placed on an endpoint, attackers can call the interface on another endpoint.</span></span>

<span data-ttu-id="a8446-110">Para garantir que um processo seja chamado somente em uma sequência de protocolo específica, registre uma função de retorno de chamada de segurança e, nessa função, verifique em qual sequência de protocolo a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="a8446-110">To ensure a process be called only on a specific protocol sequence, register a security callback function, and in that function, check on which protocol sequence the call is made.</span></span>

 

 




