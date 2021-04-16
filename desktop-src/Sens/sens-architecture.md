---
description: O serviço de notificação de eventos do sistema funciona com o sistema de eventos COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Arquitetura SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753926"
---
# <a name="sens-architecture"></a><span data-ttu-id="c7311-103">Arquitetura SENS</span><span class="sxs-lookup"><span data-stu-id="c7311-103">SENS Architecture</span></span>

<span data-ttu-id="c7311-104">O serviço de notificação de eventos do sistema funciona com o sistema de eventos COM+.</span><span class="sxs-lookup"><span data-stu-id="c7311-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="c7311-105">O SENS é um editor de eventos para as classes de eventos que ele monitora: eventos de rede, logon e energia/bateria.</span><span class="sxs-lookup"><span data-stu-id="c7311-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="c7311-106">O aplicativo que recebe uma notificação é chamado de assinante de evento.</span><span class="sxs-lookup"><span data-stu-id="c7311-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="c7311-107">Quando um aplicativo assina o recebimento de notificações, ele também pode especificar filtros associados aos eventos assinados.</span><span class="sxs-lookup"><span data-stu-id="c7311-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="c7311-108">Os eventos SENS e COM+ usam os filtros para determinar melhor quando o aplicativo deve ser notificado.</span><span class="sxs-lookup"><span data-stu-id="c7311-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="c7311-109">As notificações são assíncronas, portanto, o aplicativo que está recebendo a notificação não precisa estar ativo quando a notificação é enviada.</span><span class="sxs-lookup"><span data-stu-id="c7311-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="c7311-110">Quando um aplicativo assina o recebimento de notificações, ele pode especificar se ele deve ser ativado quando o evento ocorrer ou notificado posteriormente quando estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="c7311-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="c7311-111">A assinatura pode ser transitória e válida somente até que o aplicativo pare de ser executado, ou pode ser persistente e válido até que o aplicativo seja removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="c7311-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="c7311-112">Um repositório de dados de eventos COM+ contém informações sobre o sensor de evento (SENS), os assinantes de eventos e os filtros.</span><span class="sxs-lookup"><span data-stu-id="c7311-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="c7311-113">O SENS também predefine uma interface de saída para cada classe de evento em uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="c7311-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="c7311-114">Classe de eventos</span><span class="sxs-lookup"><span data-stu-id="c7311-114">Event class</span></span>    | <span data-ttu-id="c7311-115">GUID</span><span class="sxs-lookup"><span data-stu-id="c7311-115">GUID</span></span>                          | <span data-ttu-id="c7311-116">Interface</span><span class="sxs-lookup"><span data-stu-id="c7311-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="c7311-117">Eventos de rede</span><span class="sxs-lookup"><span data-stu-id="c7311-117">Network events</span></span> | <span data-ttu-id="c7311-118">\_rede SENSGUID EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="c7311-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="c7311-119">ISensNetwork</span><span class="sxs-lookup"><span data-stu-id="c7311-119">ISensNetwork</span></span> |
| <span data-ttu-id="c7311-120">Eventos de logon</span><span class="sxs-lookup"><span data-stu-id="c7311-120">Logon events</span></span>   | <span data-ttu-id="c7311-121">LOGON do SENSGUID \_ EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="c7311-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="c7311-122">ISensLogon</span><span class="sxs-lookup"><span data-stu-id="c7311-122">ISensLogon</span></span>   |
| <span data-ttu-id="c7311-123">Eventos de energia</span><span class="sxs-lookup"><span data-stu-id="c7311-123">Power events</span></span>   | <span data-ttu-id="c7311-124">SENSGUID \_ EVENTCLASS \_ ONNOW</span><span class="sxs-lookup"><span data-stu-id="c7311-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="c7311-125">ISensOnNow</span><span class="sxs-lookup"><span data-stu-id="c7311-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="c7311-126">Para receber notificações para qualquer um desses eventos, seu aplicativo deve fazer duas coisas:</span><span class="sxs-lookup"><span data-stu-id="c7311-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="c7311-127">Assine os eventos SENS que lhe interessam.</span><span class="sxs-lookup"><span data-stu-id="c7311-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="c7311-128">Para assinar um evento, use as interfaces **IEventSubscription** e **IEVENTSYSTEM** em eventos com+.</span><span class="sxs-lookup"><span data-stu-id="c7311-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="c7311-129">Você precisa fornecer um identificador para as classes de evento e o identificador do editor do sensor, SENSGUID \_ Publisher.</span><span class="sxs-lookup"><span data-stu-id="c7311-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="c7311-130">As assinaturas estão em um nível por evento, de modo que o aplicativo de assinatura também deve especificar quais eventos dentro da classe são interessantes.</span><span class="sxs-lookup"><span data-stu-id="c7311-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="c7311-131">Cada evento corresponde a um método na interface correspondente à sua classe de evento.</span><span class="sxs-lookup"><span data-stu-id="c7311-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="c7311-132">Crie um objeto de coletor com uma implementação para cada interface que você manipular.</span><span class="sxs-lookup"><span data-stu-id="c7311-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="c7311-133">Consulte [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) para obter mais informações sobre essas interfaces e os eventos com suporte em cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="c7311-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="c7311-134">Quando um dos eventos monitorados ocorre, o SENS processa cada assinatura com qualquer filtro associado e notifica os assinantes por meio do sistema de eventos COM+.</span><span class="sxs-lookup"><span data-stu-id="c7311-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 



