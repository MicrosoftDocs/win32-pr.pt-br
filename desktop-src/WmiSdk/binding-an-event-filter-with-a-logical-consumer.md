---
description: Depois de criar o consumidor de evento lógico e o filtro de eventos, você deve vinculá-los, o que registra o consumidor lógico para receber a notificação sobre os eventos especificados pelo filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Ligando um filtro de eventos a um consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829724"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="1c83e-103">Ligando um filtro de eventos a um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="1c83e-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="1c83e-104">Depois de criar o consumidor de evento lógico e o filtro de eventos, você deve vinculá-los, o que registra o consumidor lógico para receber a notificação sobre os eventos especificados pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="1c83e-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="1c83e-105">O procedimento a seguir descreve como associar um filtro de eventos a um consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="1c83e-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="1c83e-106">**Para associar um filtro de eventos a um consumidor lógico**</span><span class="sxs-lookup"><span data-stu-id="1c83e-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="1c83e-107">Crie uma instância da classe de sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="1c83e-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="1c83e-108">A classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) é uma classe de associação que vincula a instância de filtro de eventos e a instância de consumidor lógica em conjunto pelas propriedades de referência do **filtro** e do **consumidor** .</span><span class="sxs-lookup"><span data-stu-id="1c83e-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="1c83e-109">Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="1c83e-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="1c83e-110">Defina a propriedade de **filtro** para a instância do filtro.</span><span class="sxs-lookup"><span data-stu-id="1c83e-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="1c83e-111">Defina a propriedade **consumidor** como a instância do consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="1c83e-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="1c83e-112">Defina a propriedade **DeliverSynchronously** para determinar o tipo de entrega que você deseja.</span><span class="sxs-lookup"><span data-stu-id="1c83e-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="1c83e-113">A propriedade **DeliverSynchronously** determina quando o WMI fornece notificações de eventos de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1c83e-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="1c83e-114">Definir essa propriedade como **true** solicita uma entrega síncrona.</span><span class="sxs-lookup"><span data-stu-id="1c83e-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="1c83e-115">Use a entrega síncrona somente quando o consumidor permanente puder processar eventos dentro de aproximadamente 100 microssegundos.</span><span class="sxs-lookup"><span data-stu-id="1c83e-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="1c83e-116">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1c83e-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="1c83e-117">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1c83e-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="1c83e-118">Ao cancelar o registro de seu consumidor de evento lógico, certifique-se de excluir a instância [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="1c83e-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="1c83e-119">Cada instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) representa um registro para uma notificação de evento específica.</span><span class="sxs-lookup"><span data-stu-id="1c83e-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="1c83e-120">Quando você exclui uma associação, o WMI desativa o registro.</span><span class="sxs-lookup"><span data-stu-id="1c83e-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="1c83e-121">Talvez seja necessário excluir as instâncias lógicas de consumidor e de filtro de eventos para desativar o registro, dependendo da implementação.</span><span class="sxs-lookup"><span data-stu-id="1c83e-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="1c83e-122">O exemplo de código a seguir mostra uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) que associa uma instância de uma classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a um filtro de eventos específico (a instância do consumidor de eventos foi criada no tópico [criando um consumidor lógico](creating-a-logical-consumer.md) e o filtro de eventos foi criado no tópico [criando um filtro de eventos](creating-an-event-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="1c83e-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="1c83e-123">Dois consumidores, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md), não funcionarão, a menos que seu criador seja membro do grupo local de administradores.</span><span class="sxs-lookup"><span data-stu-id="1c83e-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="1c83e-124">**:** Quando um administrador cria uma assinatura, seu SID não é usado para a propriedade **CreatorSID** , mas o SID do grupo de Administradores local é usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1c83e-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="1c83e-125">Portanto, as instâncias podem ser criadas por administradores diferentes e a assinatura ainda funcionará.</span><span class="sxs-lookup"><span data-stu-id="1c83e-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="1c83e-126">Para obter mais informações, consulte [recebendo eventos com segurança](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="1c83e-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="1c83e-127">Quando um filtro é associado a um consumidor lógico, o evento é registrado pelo ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) para Windows).</span><span class="sxs-lookup"><span data-stu-id="1c83e-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="1c83e-128">Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="1c83e-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c83e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c83e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c83e-130">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="1c83e-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
