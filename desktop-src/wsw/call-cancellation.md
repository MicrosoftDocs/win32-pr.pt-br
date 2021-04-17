---
title: Cancelamento de chamada
description: A notificação de cancelamento de chamada cancela a operação de operações de serviço no servidor e retornos de chamada de modelo de serviço.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Chamar o cancelamento de serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105764093"
---
# <a name="call-cancellation"></a><span data-ttu-id="21acb-106">Cancelamento de chamada</span><span class="sxs-lookup"><span data-stu-id="21acb-106">Call cancellation</span></span>

<span data-ttu-id="21acb-107">A notificação de cancelamento de chamada cancela a operação de [operações de serviço no servidor](server-side-service-operations.md) e retornos de chamada de modelo de serviço.</span><span class="sxs-lookup"><span data-stu-id="21acb-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="21acb-108">Esse cancelamento pode ser por uma destas duas razões:</span><span class="sxs-lookup"><span data-stu-id="21acb-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="21acb-109">O host de serviço parou as operações devido a uma chamada para a função [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .</span><span class="sxs-lookup"><span data-stu-id="21acb-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="21acb-110">O canal subjacente gerou uma falha.</span><span class="sxs-lookup"><span data-stu-id="21acb-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="21acb-111">Para receber uma notificação de cancelamento, a operação de serviço ou o retorno de chamada de modelo de serviço deve registrar um retorno de chamada de [**\_ \_ cancelamento de \_ retorno de operação do WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) chamando a função [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .</span><span class="sxs-lookup"><span data-stu-id="21acb-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="21acb-112">Opcionalmente, como parte do registro para notificação de cancelamento, a operação de serviço ou o retorno de chamada de modelo de serviço também pode registrar dados de estado específicos do aplicativo e o retorno de chamada do [**\_ \_ \_ \_ estado livre do WS Operation**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .</span><span class="sxs-lookup"><span data-stu-id="21acb-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="21acb-113">Os dados de estado são disponibilizados para o retorno de chamada de [**\_ \_ cancelamento \_ da operação WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) .</span><span class="sxs-lookup"><span data-stu-id="21acb-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="21acb-114">Na conclusão da chamada, o retorno de chamada do [**\_ \_ \_ \_ estado livre do WS Operation**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) é chamado para dar ao aplicativo uma oportunidade de liberar os dados de estado.</span><span class="sxs-lookup"><span data-stu-id="21acb-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="21acb-115">Para obter um exemplo de código, consulte [BlockingServiceExample](blockingserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="21acb-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="21acb-116">O retorno de chamada de cancelamento é chamado apenas uma vez durante o tempo de vida da função de operações ou de retorno de chamada do [serviço do servidor](server-side-service-operations.md) .</span><span class="sxs-lookup"><span data-stu-id="21acb-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="21acb-117">O cancelamento de chamada está disponível em para todos os retornos de chamada do host de serviço que usam o [ \_ \_ contexto de operação do WS](ws-operation-context.md) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="21acb-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="21acb-118">Os elementos da API a seguir estão relacionados ao cancelamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="21acb-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="21acb-119">Callback</span><span class="sxs-lookup"><span data-stu-id="21acb-119">Callback</span></span>                                                                         | <span data-ttu-id="21acb-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="21acb-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21acb-121">**\_retorno de \_ chamada Cancelar operação \_ WS**</span><span class="sxs-lookup"><span data-stu-id="21acb-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="21acb-122">Chamado pelo modelo de serviço para notificar um cancelamento de uma operação de serviço assíncrono como resultado de um desligamento anulado do host de serviço.</span><span class="sxs-lookup"><span data-stu-id="21acb-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="21acb-123">**\_retorno de \_ \_ chamada de estado livre de operação WS \_**</span><span class="sxs-lookup"><span data-stu-id="21acb-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="21acb-124">Chamado pelo modelo de serviço para permitir que um aplicativo Limpe os dados de estado que foram registrados com o retorno de chamada de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="21acb-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="21acb-125">Função</span><span class="sxs-lookup"><span data-stu-id="21acb-125">Function</span></span>                                                             | <span data-ttu-id="21acb-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="21acb-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21acb-127">**WsRegisterOperationForCancel**</span><span class="sxs-lookup"><span data-stu-id="21acb-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="21acb-128">Permite que uma operação de serviço ou um retorno de chamada de modelo de serviço seja registrado para uma notificação de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="21acb-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




