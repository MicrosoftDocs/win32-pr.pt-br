---
title: Cancelando chamadas de método
description: Com a introdução de aplicativos distribuídos e baseados na Web, algumas chamadas de método podem levar um tempo muito demorado para retornar.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105797997"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="f2d5d-103">Cancelando chamadas de método</span><span class="sxs-lookup"><span data-stu-id="f2d5d-103">Canceling Method Calls</span></span>

<span data-ttu-id="f2d5d-104">Com a introdução de aplicativos distribuídos e baseados na Web, algumas chamadas de método podem levar um tempo muito demorado para retornar.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="f2d5d-105">A latência da conexão de rede pode ser alta, a máquina do servidor pode estar atendendo a vários clientes ou o componente do servidor pode estar passando uma grande quantidade de dados, como um arquivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="f2d5d-106">Os usuários devem ser capazes de cancelar uma solicitação que está demorando muito e o aplicativo deve ser capaz de lidar com solicitações de cancelamento e continuar com seu outro trabalho.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="f2d5d-107">Em COM, você pode usar a interface [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar uma chamada pendente originada de um apartamento single-threaded.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="f2d5d-108">Quando uma chamada é empacotada, o proxy cria um objeto Cancel, que implementa a interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="f2d5d-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="f2d5d-109">O objeto Cancel é associado à chamada e ao thread no qual a chamada está pendente.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="f2d5d-110">Para cancelar a chamada pendente, o cliente passa uma solicitação de cancelamento por meio do objeto Cancel, que manipula os detalhes da notificação do objeto de servidor que a chamada foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="f2d5d-111">Se o método chamado não tiver retornado, o objeto Server, na detecção da solicitação de cancelamento, limpará os recursos do programa que ele alocou e notificará seu cliente, retornando um valor **HRESULT** apropriado, que ele cancelou a execução da chamada.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="f2d5d-112">Se o método chamado já tiver retornado, o objeto Cancel notificará o cliente.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="f2d5d-113">Em ambos os casos, o thread do cliente é desbloqueado e pode continuar o processamento.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="f2d5d-114">A forma como o objeto de servidor responde a uma solicitação de cancelamento é a critério do implementador do servidor, mas o thread de chamada no cliente sempre será desbloqueado e ignorará quaisquer resultados que o servidor tentar passar para ele.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="f2d5d-115">Os objetos Cancel fornecem um meio de solicitar que um método em execução no momento seja cancelado, mas não há nenhuma garantia de que o objeto de servidor pare de processar a chamada.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="f2d5d-116">Por exemplo, a chamada pode já ter sido retornada ou o objeto de servidor pode não dar suporte a objetos Cancel.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="f2d5d-117">O COM fornece automaticamente uma implementação padrão de objetos de cancelamento para objetos de cliente e interfaces que usam marshaling padrão.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="f2d5d-118">Para objetos e interfaces que usam marshaling personalizado, você precisará implementar seu próprio objeto Cancel.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="f2d5d-119">Neste momento, o cancelamento de objetos lida apenas com chamadas síncronas.</span><span class="sxs-lookup"><span data-stu-id="f2d5d-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2d5d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2d5d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2d5d-121">Cancelando uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="f2d5d-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="f2d5d-122">**CoGetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="f2d5d-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="f2d5d-123">**CoSetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="f2d5d-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="f2d5d-124">**CoTestCancel**</span><span class="sxs-lookup"><span data-stu-id="f2d5d-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 