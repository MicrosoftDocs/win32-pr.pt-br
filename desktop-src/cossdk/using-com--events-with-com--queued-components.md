---
description: O serviço de eventos COM+ é usado para gerenciar a entrega de eventos de editores para assinantes.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Usando eventos COM+ com componentes em fila COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762185"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="88e95-103">Usando eventos COM+ com componentes em fila COM+</span><span class="sxs-lookup"><span data-stu-id="88e95-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="88e95-104">O serviço de eventos COM+ é usado para gerenciar a entrega de eventos de editores para assinantes.</span><span class="sxs-lookup"><span data-stu-id="88e95-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="88e95-105">O serviço de componentes na fila COM+ pode ser usado para tornar o Publicador e o tempo de processamento do assinante independentes, colocando a mensagem do Publicador em fila e depois repetindo-o no Assinante.</span><span class="sxs-lookup"><span data-stu-id="88e95-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="88e95-106">Se você precisa ou não usar o serviço de componentes na fila depende da lógica de negócios subjacente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88e95-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="88e95-107">Se você precisar ter eventos independentes de tempo, poderá criá-los usando o serviço de eventos COM+ com o serviço de componentes em fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="88e95-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="88e95-108">Para obter informações adicionais sobre como usar o serviço de componentes na fila do COM+, consulte [componentes em fila do com+](com--queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="88e95-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="88e95-109">O serviço de componentes na fila mantém a invocação de ordem de método em uma única mensagem.</span><span class="sxs-lookup"><span data-stu-id="88e95-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="88e95-110">O gravador executa em lotes todas as invocações de método em uma mensagem e, em seguida, o Player invoca esses métodos na ordem em que a mensagem é processada.</span><span class="sxs-lookup"><span data-stu-id="88e95-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="88e95-111">Um gravador e um player de componentes em fila podem ser posicionados em qualquer um dos dois locais a seguir:</span><span class="sxs-lookup"><span data-stu-id="88e95-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="88e95-112">Entre o editor e o objeto de evento</span><span class="sxs-lookup"><span data-stu-id="88e95-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="88e95-113">Entre o objeto de evento e o Assinante</span><span class="sxs-lookup"><span data-stu-id="88e95-113">Between the event object and subscriber</span></span>

<span data-ttu-id="88e95-114">Se você posicionar o gravador e o Player entre o editor e o objeto de evento, estará tornando o componente de [classe de evento](the-com--event-class-object.md) queuable.</span><span class="sxs-lookup"><span data-stu-id="88e95-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="88e95-115">O componente de classe de evento deve ser marcado para enfileiramento e ser ativado pelo Player em um processo separado do Publicador.</span><span class="sxs-lookup"><span data-stu-id="88e95-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="88e95-116">Para entregar eventos de forma assíncrona, redija o gravador e o Player entre o objeto de evento e o Assinante e defina o atributo enfileirado do objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="88e95-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="88e95-117">Isso define SubscriberMoniker da seguinte maneira: "Queue:/New:/ {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="88e95-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="88e95-118">Há uma ordem de implicação de entrega a ser considerada ao usar componentes enfileirados em uma situação de evento.</span><span class="sxs-lookup"><span data-stu-id="88e95-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="88e95-119">Como o serviço de componentes na fila registra e reproduz todas as chamadas dentro do tempo de vida de um único objeto em uma mensagem, todas as chamadas são reproduzidas na ordem em que foram feitas.</span><span class="sxs-lookup"><span data-stu-id="88e95-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="88e95-120">No entanto, se houver mais de uma sessão com mais de um objeto, a ordem não poderá ser garantida.</span><span class="sxs-lookup"><span data-stu-id="88e95-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="88e95-121">Se a ordem for importante, verifique se as chamadas que precisam ser reproduzidas na ordem residem na mesma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="88e95-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e95-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88e95-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e95-123">Filtrando eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="88e95-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="88e95-124">Publicando e fornecendo eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="88e95-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="88e95-125">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="88e95-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="88e95-126">O objeto de classe de evento COM+</span><span class="sxs-lookup"><span data-stu-id="88e95-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



