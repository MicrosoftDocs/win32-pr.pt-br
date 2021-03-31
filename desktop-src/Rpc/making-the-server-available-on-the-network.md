---
title: Disponibilizando o servidor na rede
description: Antes que um aplicativo de servidor possa aceitar chamadas de procedimento remotos, ele deve estar disponível na rede.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- RPC de chamada de procedimento remoto, tarefas, disponibilizando o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005726"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="f742d-104">Disponibilizando o servidor na rede</span><span class="sxs-lookup"><span data-stu-id="f742d-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="f742d-105">Antes que um aplicativo de servidor possa aceitar chamadas de procedimento remotos, ele deve estar disponível na rede.</span><span class="sxs-lookup"><span data-stu-id="f742d-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="f742d-106">Para fazer isso, o servidor indica para o tempo de execução RPC que está disposto a aceitar chamadas em uma ou mais sequências de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f742d-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="f742d-107">Escolhendo as sequências de protocolo que um aplicativo de servidor dá suporte é uma decisão importante; sequências de protocolo diferentes têm recursos muito diferentes.</span><span class="sxs-lookup"><span data-stu-id="f742d-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="f742d-108">Os servidores que esperam que as chamadas sejam recebidas localmente devem usar **Ncalrpc**.</span><span class="sxs-lookup"><span data-stu-id="f742d-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="f742d-109">Os servidores que aceitam chamadas remotas devem usar o **\_ \_ TCP IP ncacn**.</span><span class="sxs-lookup"><span data-stu-id="f742d-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="f742d-110">Os servidores não devem verificar se a sequência de protocolo na qual eles recebem chamadas é a sequência de protocolos na qual eles esperam receber chamadas.</span><span class="sxs-lookup"><span data-stu-id="f742d-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="f742d-111">Confira cuidado com outros pontos de extremidade RPC em execução no mesmo processo nas melhores práticas de programação RPC para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f742d-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="f742d-112">O exemplo a seguir usa **ncacn \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="f742d-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="f742d-113">A maioria dos programas de servidor usa todas as sequências de protocolo disponíveis na rede.</span><span class="sxs-lookup"><span data-stu-id="f742d-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="f742d-114">Para fazer isso, eles invocam a função [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , conforme mostrado no fragmento de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="f742d-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="f742d-115">O primeiro parâmetro para a função [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) é a sequência de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f742d-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="f742d-116">O segundo parâmetro depende da sequência de protocolo.</span><span class="sxs-lookup"><span data-stu-id="f742d-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="f742d-117">Conforme ilustrado no fragmento de código, a maioria dos programas de servidor define esse parâmetro como **RPC \_ C \_ PROTSEQ \_ Max \_ requisitos \_ Default**.</span><span class="sxs-lookup"><span data-stu-id="f742d-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="f742d-118">Esse valor define a Biblioteca RPC para usar o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f742d-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="f742d-119">O terceiro parâmetro é um descritor de segurança e não deve ser usado em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f742d-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="f742d-120">Para obter mais informações, consulte [**segurança**](security.md).</span><span class="sxs-lookup"><span data-stu-id="f742d-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="f742d-121">Você também pode usar as funções [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)ou [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .</span><span class="sxs-lookup"><span data-stu-id="f742d-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="f742d-122">Depois que um aplicativo de servidor seleciona pelo menos uma sequência de protocolo, os servidores que usam pontos de extremidade dinâmicos devem criar informações de associação para cada sequência de protocolo usada por ele.</span><span class="sxs-lookup"><span data-stu-id="f742d-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="f742d-123">O servidor armazena as informações de associação em um vetor de associação que pode então exportar para o serviço mapeador de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f742d-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="f742d-124">Use a função [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obter um vetor de associação para o aplicativo de servidor, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="f742d-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="f742d-125">O único parâmetro passado para a função [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) é um ponteiro para um ponteiro para uma estrutura de [**\_ \_ vetor de associação RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) .</span><span class="sxs-lookup"><span data-stu-id="f742d-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="f742d-126">A biblioteca de tempo de execução RPC aloca dinamicamente uma matriz de vetores de ligação e armazena o endereço da matriz na variável de parâmetro (nesse caso, **rpcBindingVector**).</span><span class="sxs-lookup"><span data-stu-id="f742d-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="f742d-127">Cada aplicativo de servidor é responsável por liberar esse vetor de ligação usando a função [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) depois que ele termina de usá-lo (por exemplo, depois de transmiti-lo para as funções apropriadas).</span><span class="sxs-lookup"><span data-stu-id="f742d-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




