---
title: Usando métodos
description: Quando um cliente é registrado com o Gerenciador de tabela de roteamento, ele pode exportar um conjunto de métodos. Esses métodos são usados por outros clientes para obter informações específicas do cliente. Os métodos permitem a comunicação privada entre clientes do Gerenciador de tabela de roteamento.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916353"
---
# <a name="using-methods"></a><span data-ttu-id="66ea5-105">Usando métodos</span><span class="sxs-lookup"><span data-stu-id="66ea5-105">Using Methods</span></span>

<span data-ttu-id="66ea5-106">Quando um cliente é registrado com o Gerenciador de tabela de roteamento, ele pode exportar um conjunto de métodos.</span><span class="sxs-lookup"><span data-stu-id="66ea5-106">When a client registers with the routing table manager, it can export a set of methods.</span></span> <span data-ttu-id="66ea5-107">Esses métodos são usados por outros clientes para obter informações específicas do cliente.</span><span class="sxs-lookup"><span data-stu-id="66ea5-107">These methods are used by other clients to obtain client-specific information.</span></span> <span data-ttu-id="66ea5-108">Os métodos permitem a comunicação privada entre clientes do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="66ea5-108">Methods enable private communication between clients of the routing table manager.</span></span>

<span data-ttu-id="66ea5-109">Um cliente pode obter a lista de métodos exportados por outro cliente.</span><span class="sxs-lookup"><span data-stu-id="66ea5-109">A client can obtain the list of methods exported by another client.</span></span> <span data-ttu-id="66ea5-110">O cliente chama a função [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , fornecendo o identificador do cliente de destino.</span><span class="sxs-lookup"><span data-stu-id="66ea5-110">The client calls the [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) function, supplying the target client's handle.</span></span>

<span data-ttu-id="66ea5-111">Cada método exportado por um cliente é identificado exclusivamente por seu identificador de método.</span><span class="sxs-lookup"><span data-stu-id="66ea5-111">Each method exported by a client is uniquely identified by its method identifier.</span></span> <span data-ttu-id="66ea5-112">Cada cliente pode exportar até 32 métodos.</span><span class="sxs-lookup"><span data-stu-id="66ea5-112">Each client can export up to 32 methods.</span></span> <span data-ttu-id="66ea5-113">Cada método corresponde a um conjunto de bits no membro **MethodType** da estrutura [**do \_ \_ \_ método de exportação da entidade RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) .</span><span class="sxs-lookup"><span data-stu-id="66ea5-113">Each method corresponds to a bit set in the **MethodType** member of the [**RTM\_ENTITY\_EXPORT\_METHOD**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) structure.</span></span> <span data-ttu-id="66ea5-114">Para invocar vários métodos, o cliente deve executar uma lógica ou dos identificadores para esses métodos.</span><span class="sxs-lookup"><span data-stu-id="66ea5-114">To invoke multiple methods, the client should perform a logical OR of the identifiers for those methods.</span></span> <span data-ttu-id="66ea5-115">A sintaxe e a semântica de estruturas de entrada e saída para cada protocolo devem ser especificadas quando o protocolo é implementado.</span><span class="sxs-lookup"><span data-stu-id="66ea5-115">The syntax and semantics of input and output structures for each protocol must be specified when the protocol is implemented.</span></span>

> [!Note]  
> <span data-ttu-id="66ea5-116">Os valores de identificador de método que correspondem a um conjunto de bits na metade inferior do membro **MethodType** (os 16 bits inferiores) são reservados pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="66ea5-116">Method identifier values that correspond to a bit set in the lower half of the **MethodType** member (the lower 16 bits) are reserved by Microsoft.</span></span>

 

<span data-ttu-id="66ea5-117">Para invocar um segundo método de cliente, um cliente chama a função [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) .</span><span class="sxs-lookup"><span data-stu-id="66ea5-117">To invoke a second client's method, a client calls the [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) function.</span></span> <span data-ttu-id="66ea5-118">O Gerenciador de tabela de roteamento arbitra todas as solicitações para invocar os métodos de um cliente.</span><span class="sxs-lookup"><span data-stu-id="66ea5-118">The routing table manager arbitrates all requests to invoke a client's methods.</span></span> <span data-ttu-id="66ea5-119">O Gerenciador de tabela de roteamento executa duas funções quando arbitra entre clientes:</span><span class="sxs-lookup"><span data-stu-id="66ea5-119">The routing table manager performs two functions when it arbitrates between clients:</span></span>

-   <span data-ttu-id="66ea5-120">Impedir que o segundo cliente invoque um método para um cliente que está cancelando o registro.</span><span class="sxs-lookup"><span data-stu-id="66ea5-120">Preventing the second client from invoking a method for a client that is unregistering.</span></span>
-   <span data-ttu-id="66ea5-121">Manter uma solicitação "Invoke" quando os métodos são bloqueados e permitir que a solicitação continue quando os métodos são desbloqueados.</span><span class="sxs-lookup"><span data-stu-id="66ea5-121">Holding an "invoke" request when methods are blocked, and allowing the request to continue when the methods are unblocked.</span></span>

<span data-ttu-id="66ea5-122">Se um cliente precisar impedir que outros clientes executem seus métodos, o cliente poderá chamar [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span><span class="sxs-lookup"><span data-stu-id="66ea5-122">If a client must prevent other clients from executing its methods, the client can call [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods).</span></span> <span data-ttu-id="66ea5-123">O Gerenciador de tabela de roteamento não permitirá que uma chamada para [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) seja processada até que o cliente desbloqueie seus métodos novamente.</span><span class="sxs-lookup"><span data-stu-id="66ea5-123">The routing table manager will not allow a call to [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) to be processed until the client unblocks its methods again.</span></span>

<span data-ttu-id="66ea5-124">Os clientes normalmente bloqueiam métodos ao fazer alterações nos dados privados trocados entre clientes.</span><span class="sxs-lookup"><span data-stu-id="66ea5-124">Clients typically block methods when making changes to the private data that is exchanged between clients.</span></span> <span data-ttu-id="66ea5-125">Os métodos de bloqueio são uma ação opcional.</span><span class="sxs-lookup"><span data-stu-id="66ea5-125">Blocking methods is an optional action.</span></span> <span data-ttu-id="66ea5-126">Um cliente também pode usar bloqueios internos para impedir que outros clientes invoquem métodos.</span><span class="sxs-lookup"><span data-stu-id="66ea5-126">A client can also use internal locks to prevent other clients from invoking methods.</span></span>

<span data-ttu-id="66ea5-127">Para obter um exemplo de código que mostra como usar essas funções, consulte [obter e chamar os métodos exportados para um cliente](obtain-and-call-the-exported-methods-for-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="66ea5-127">For sample code that shows how to use these functions, see [Obtain and Call the Exported Methods for a Client](obtain-and-call-the-exported-methods-for-a-client.md).</span></span>

 

 




