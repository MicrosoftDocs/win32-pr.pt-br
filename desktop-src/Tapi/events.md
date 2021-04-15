---
description: Os eventos são uma parte crucial do tratamento de chamadas sob a TAPI 3. A manipulação de eventos inclui quatro estágios.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventos (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505867"
---
# <a name="events-telephony-api"></a><span data-ttu-id="5322a-104">Eventos (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="5322a-104">Events (Telephony API)</span></span>

<span data-ttu-id="5322a-105">Os eventos são uma parte crucial do tratamento de chamadas sob a TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="5322a-105">Events are a crucial part of call handling under TAPI 3.</span></span> <span data-ttu-id="5322a-106">A manipulação de eventos inclui quatro estágios.</span><span class="sxs-lookup"><span data-stu-id="5322a-106">Event handling includes four stages.</span></span>

<span data-ttu-id="5322a-107">**Para se registrar e habilitar a recepção de eventos**</span><span class="sxs-lookup"><span data-stu-id="5322a-107">**To register for and enable the reception of events**</span></span>

1.  <span data-ttu-id="5322a-108">Implemente o método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) .</span><span class="sxs-lookup"><span data-stu-id="5322a-108">Implement the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method.</span></span> <span data-ttu-id="5322a-109">(TAPI chama esse método quando ocorre um evento.) Normalmente, essa implementação não tem mais do que **AddRef** o ponteiro da interface **IDispatch** e depois posta para a bomba de mensagens do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5322a-109">(TAPI calls this method when an event occurs.) Typically, this implementation does no more than **AddRef** the **IDispatch** interface pointer, then post to the application's message pump.</span></span>
2.  <span data-ttu-id="5322a-110">Registre a interface de saída do [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) usando as interfaces [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) padrão com e passe o método [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) um ponteiro para [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span><span class="sxs-lookup"><span data-stu-id="5322a-110">Register the [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) outgoing interface using the COM standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) and [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interfaces, and pass the [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) method a pointer to [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span></span>
3.  <span data-ttu-id="5322a-111">Chame o método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) para informar à TAPI quais eventos o aplicativo manipulará.</span><span class="sxs-lookup"><span data-stu-id="5322a-111">Call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method to tell TAPI which events the application will handle.</span></span> <span data-ttu-id="5322a-112">O filtro de eventos consiste em **ou** Ed membros da enumeração de [**\_ eventos TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .</span><span class="sxs-lookup"><span data-stu-id="5322a-112">The event filter consists of **OR** ed members of the [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) enumeration.</span></span>
    > [!Note]  
    > <span data-ttu-id="5322a-113">Você deve chamar o método **ITTAPI::p UT \_ EventFilter** para definir a máscara de filtro de eventos e habilitar a recepção de eventos.</span><span class="sxs-lookup"><span data-stu-id="5322a-113">You must call the **ITTAPI::put\_EventFilter** method to set the event filter mask and enable reception of events.</span></span> <span data-ttu-id="5322a-114">Se você não chamar **ITTAPI::p UT \_ EventFilter**, seu aplicativo não receberá nenhum evento.</span><span class="sxs-lookup"><span data-stu-id="5322a-114">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span>

     

<span data-ttu-id="5322a-115">Você também deve chamar o método [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) para cada objeto de endereço no qual o aplicativo tratará chamadas.</span><span class="sxs-lookup"><span data-stu-id="5322a-115">You must also call the [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) method for each address object on which the application will handle calls.</span></span>

<span data-ttu-id="5322a-116">Consulte [interfaces de evento](./event-interfaces.md) para obter uma lista de todas as interfaces de evento.</span><span class="sxs-lookup"><span data-stu-id="5322a-116">See [Event Interfaces](./event-interfaces.md) for a list of all event interfaces.</span></span> <span data-ttu-id="5322a-117">Consulte [registrar eventos](register-events.md) para obter exemplos de código que ilustram o processo de registro e [recebem uma chamada](receive-a-call.md) para um exemplo de código que mostra um uso de eventos.</span><span class="sxs-lookup"><span data-stu-id="5322a-117">See [Register Events](register-events.md) for code examples that illustrate the registration process and [Receive a Call](receive-a-call.md) for a code example that shows one use of events.</span></span>

 

 
