---
description: Um provedor de consumidor de eventos é um componente da arquitetura de consumidor permanente que determina qual consumidor de evento permanente trata de um determinado evento.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Escrevendo um provedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763069"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="2da15-103">Escrevendo um provedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="2da15-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="2da15-104">Um provedor de consumidor de eventos é um componente da arquitetura de consumidor permanente que determina qual consumidor de evento permanente trata de um determinado evento.</span><span class="sxs-lookup"><span data-stu-id="2da15-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="2da15-105">Você deve criar um provedor de consumidor de eventos junto com seus consumidores de evento permanentes para rotear eventos adequadamente do WMI.</span><span class="sxs-lookup"><span data-stu-id="2da15-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="2da15-106">Um provedor de consumidor de eventos vincula um provedor de eventos a uma lista de classes de consumidor.</span><span class="sxs-lookup"><span data-stu-id="2da15-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="2da15-107">As instâncias dessas classes de consumidor recebem eventos desse provedor.</span><span class="sxs-lookup"><span data-stu-id="2da15-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="2da15-108">O WMI identifica a qual provedor de consumidor os eventos são entregues, com base na instância [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que associa a instância [**\_ \_ Win32Provider**](--win32provider.md) do provedor de consumidor a uma classe de consumidor lógica.</span><span class="sxs-lookup"><span data-stu-id="2da15-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="2da15-109">Os usuários criam instâncias da classe consumidor como parte de uma assinatura permanente.</span><span class="sxs-lookup"><span data-stu-id="2da15-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="2da15-110">Se o provedor de eventos não estiver em execução quando um evento ocorrer, o WMI iniciará o provedor quando precisar entregar eventos.</span><span class="sxs-lookup"><span data-stu-id="2da15-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="2da15-111">O procedimento a seguir descreve como implementar um provedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="2da15-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="2da15-112">**Para implementar um provedor de consumidor de eventos**</span><span class="sxs-lookup"><span data-stu-id="2da15-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="2da15-113">Crie classes de consumidor em formato MOF (MOF) e registre-as com o WMI.</span><span class="sxs-lookup"><span data-stu-id="2da15-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="2da15-114">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="2da15-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="2da15-115">Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="2da15-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="2da15-116">Para obter mais informações, consulte [registrando um provedor de consumidor de eventos](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2da15-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="2da15-117">Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="2da15-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="2da15-118">O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor.</span><span class="sxs-lookup"><span data-stu-id="2da15-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="2da15-119">Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2da15-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="2da15-120">Os provedores de consumidor de eventos são altamente incentivados a usar o modelo de vários threads "both".</span><span class="sxs-lookup"><span data-stu-id="2da15-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="2da15-121">Implemente a interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="2da15-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="2da15-122">A interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) é a interface principal para um provedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="2da15-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="2da15-123">Forneça um ou mais consumidores físicos para receber as mensagens de evento do WMI.</span><span class="sxs-lookup"><span data-stu-id="2da15-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="2da15-124">Um consumidor físico é um objeto COM que representa um consumidor de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="2da15-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="2da15-125">Todos os consumidores físicos devem implementar a interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="2da15-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="2da15-126">Para obter mais informações, consulte [implementando um consumidor físico](implementing-a-physical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="2da15-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



