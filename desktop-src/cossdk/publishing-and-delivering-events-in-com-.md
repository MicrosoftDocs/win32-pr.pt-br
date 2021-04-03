---
description: Para publicar um evento, basta criar uma instância de um objeto de classe de evento e invocar o método desejado; para obter instruções detalhadas sobre como fazer isso no código, consulte publicando um evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publicando e fornecendo eventos no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646488"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="e5517-103">Publicando e fornecendo eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="e5517-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="e5517-104">Para publicar um evento, basta criar uma instância de um objeto de [classe de evento](the-com--event-class-object.md) e invocar o método desejado; para obter instruções detalhadas sobre como fazer isso no código, consulte [publicando um evento](publishing-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="e5517-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="e5517-105">Quando um Publicador dispara um evento, o serviço de eventos COM+ pesquisa o banco de dados de assinatura para localizar todos os assinantes que registraram assinaturas na classe de evento instanciado.</span><span class="sxs-lookup"><span data-stu-id="e5517-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="e5517-106">Ele se conecta a esses assinantes (por criação direta, monikers ou componentes enfileirados) e chama o método.</span><span class="sxs-lookup"><span data-stu-id="e5517-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="e5517-107">Para dar suporte a mais de uma notificação de assinante para um evento, os métodos podem conter apenas em parâmetros e devem retornar apenas valores de êxito ou falha de **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5517-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="e5517-108">Esta versão dos eventos COM+ não dá suporte a um repositório de eventos distribuído.</span><span class="sxs-lookup"><span data-stu-id="e5517-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="e5517-109">Um Assinante deve assinar um evento em cada computador do qual deseja receber a notificação.</span><span class="sxs-lookup"><span data-stu-id="e5517-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="e5517-110">Como alternativa, você pode registrar o objeto de classe de evento e as assinaturas em um computador central e instanciar esse objeto de classe de evento a partir dos computadores remotos nos quais você publica eventos.</span><span class="sxs-lookup"><span data-stu-id="e5517-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="e5517-111">A entrega de eventos é fornecida pelo DCOM ou pelo serviço de componentes em fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="e5517-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="e5517-112">Para obter mais informações sobre como usar o serviço de componentes na fila COM+, consulte [usando eventos com+ com componentes em fila do com+](using-com--events-with-com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="e5517-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="e5517-113">Por padrão, o serviço de eventos COM+ dispara eventos um de cada vez, em nenhuma ordem determinada ou repetitiva.</span><span class="sxs-lookup"><span data-stu-id="e5517-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="e5517-114">Os Publicadores que precisam controlar a ordem em que os assinantes recebem um evento podem implementar um filtro de editor.</span><span class="sxs-lookup"><span data-stu-id="e5517-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="e5517-115">(Para obter mais informações, consulte [Filtering Events in com+](filtering-events-in-com-.md).)</span><span class="sxs-lookup"><span data-stu-id="e5517-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5517-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5517-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5517-117">Filtrando eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="e5517-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="e5517-118">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="e5517-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="e5517-119">O objeto de classe de evento COM+</span><span class="sxs-lookup"><span data-stu-id="e5517-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="e5517-120">Usando eventos COM+ com componentes em fila COM+</span><span class="sxs-lookup"><span data-stu-id="e5517-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



