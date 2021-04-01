---
title: Causal ordenação de chamadas assíncronas
description: Em um aplicativo RPC assíncrono, é possível que um thread de cliente faça uma segunda chamada assíncrona em um identificador de associação antes que uma chamada anterior feita nesse identificador seja concluída.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005439"
---
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="61490-103">Causal ordenação de chamadas assíncronas</span><span class="sxs-lookup"><span data-stu-id="61490-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="61490-104">Em um aplicativo RPC assíncrono, é possível que um thread de cliente faça uma segunda chamada assíncrona em um identificador de associação antes que uma chamada anterior feita nesse identificador seja concluída.</span><span class="sxs-lookup"><span data-stu-id="61490-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="61490-105">A biblioteca de tempo de execução RPC trata dessa situação da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="61490-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="61490-106">O mecanismo de RPC assíncrono garante que as chamadas assíncronas feitas no mesmo identificador de ligação, no mesmo thread, no mesmo nível de segurança, sejam expedidas na ordem em que foram feitas.</span><span class="sxs-lookup"><span data-stu-id="61490-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="61490-107">A execução real das chamadas pode ocorrer fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="61490-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="61490-108">Assim como acontece com chamadas síncronas, as chamadas de procedimento remoto assíncronas de diferentes threads de cliente são executadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="61490-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="61490-109">Se uma chamada assíncrona de um aplicativo cliente for seguida por uma ou mais chamadas síncronas, a chamada assíncrona poderá ser executada enquanto as chamadas síncronas estiverem em execução.</span><span class="sxs-lookup"><span data-stu-id="61490-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="61490-110">Independentemente do status da chamada assíncrona, as chamadas síncronas são executadas na ordem em que são recebidas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="61490-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="61490-111">Se um aplicativo cliente selecionar a ordenação noncausal para um identificador de ligação específico, ele desabilitará a serialização para esse identificador.</span><span class="sxs-lookup"><span data-stu-id="61490-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="61490-112">Os aplicativos habilitam a ordenação de noncausal chamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) com o parâmetro *Option* definido como RPC \_ C \_ opt \_ Binding \_ Noncausal e o parâmetro *optionvalue* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="61490-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="61490-113">Para obter detalhes, consulte [constantes de opção de associação](binding-option-constants.md).</span><span class="sxs-lookup"><span data-stu-id="61490-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




