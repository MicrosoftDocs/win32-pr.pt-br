---
description: Publicação de um evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publicação de um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782627"
---
# <a name="publishing-an-event"></a><span data-ttu-id="51d63-103">Publicação de um evento</span><span class="sxs-lookup"><span data-stu-id="51d63-103">Publishing an Event</span></span>

<span data-ttu-id="51d63-104">Para publicar um evento, basta criar uma instância de um objeto de evento chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou o método **CreateObject** do Microsoft Visual Basic usando EventClassID ou EventClassName como um argumento.</span><span class="sxs-lookup"><span data-stu-id="51d63-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="51d63-105">O Publicador chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto de evento para obter as interfaces suportadas pelo objeto de classe de evento e invoca um método no objeto Event por meio da interface para publicar o evento.</span><span class="sxs-lookup"><span data-stu-id="51d63-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="51d63-106">Em seguida, o sistema de eventos publica eventos na classe de evento CLSID \_ EventObjectChange com a ID de interface IID \_ IEventObjectChange.</span><span class="sxs-lookup"><span data-stu-id="51d63-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="51d63-107">Para dar suporte à entrega de eventos a vários assinantes, os métodos de classe de evento devem conter apenas em parâmetros.</span><span class="sxs-lookup"><span data-stu-id="51d63-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="51d63-108">Usando a Propriedade FireInParallel do objeto de [classe de evento](the-com--event-class-object.md) , os editores podem solicitar que o sistema de eventos use vários threads para entregar um evento a mais de um assinante.</span><span class="sxs-lookup"><span data-stu-id="51d63-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="51d63-109">A seleção de um mecanismo de entrega em paralelo não garante a entrega simultânea do evento a vários assinantes, mas instrui o serviço de eventos COM+ a permitir que isso aconteça.</span><span class="sxs-lookup"><span data-stu-id="51d63-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51d63-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51d63-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51d63-111">Publicando e fornecendo eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="51d63-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
