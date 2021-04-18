---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793235"
---
# <a name="e-wmi"></a><span data-ttu-id="49c85-103">E (WMI)</span><span class="sxs-lookup"><span data-stu-id="49c85-103">E (WMI)</span></span>

<span data-ttu-id="49c85-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="49c85-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="49c85-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**classe de evento**</span><span class="sxs-lookup"><span data-stu-id="49c85-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-106">Uma classe WMI que os *consumidores de eventos* podem assinar por uma consulta de *evento*.</span><span class="sxs-lookup"><span data-stu-id="49c85-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="49c85-107">A classe relata um tipo específico de ocorrência.</span><span class="sxs-lookup"><span data-stu-id="49c85-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="49c85-108">Por exemplo, a classe [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) relata que um processo específico foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="49c85-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="49c85-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumidor de evento**</span><span class="sxs-lookup"><span data-stu-id="49c85-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-110">Um destinatário de notificações que relatam uma ocorrência de um evento.</span><span class="sxs-lookup"><span data-stu-id="49c85-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="49c85-111">Um consumidor de eventos é [*temporário*](gloss-t.md) ou [*permanente*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="49c85-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c85-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**provedor de consumidor de eventos**</span><span class="sxs-lookup"><span data-stu-id="49c85-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-113">Um provedor que determina qual consumidor de evento permanente manipula um determinado evento.</span><span class="sxs-lookup"><span data-stu-id="49c85-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="49c85-114">Um provedor de consumidor de eventos é registrado com o WMI por uma instância de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), que contém uma lista das classes de [*consumidor lógicas*](gloss-l.md) que o provedor de consumidor de eventos suporta.</span><span class="sxs-lookup"><span data-stu-id="49c85-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="49c85-115">Um provedor de consumidor de eventos é um servidor COM que mapeia [*consumidores físicos*](gloss-p.md) para *consumidores lógicos*.</span><span class="sxs-lookup"><span data-stu-id="49c85-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="49c85-116">Um provedor de consumidor de eventos dá suporte à interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) e é um componente da arquitetura de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="49c85-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="49c85-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro de eventos**</span><span class="sxs-lookup"><span data-stu-id="49c85-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-118">Uma instância da classe de sistema [**\_ \_ EventFilter**](--eventfilter.md) que descreve um tipo de evento e as condições para entregar uma notificação.</span><span class="sxs-lookup"><span data-stu-id="49c85-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="49c85-119">Um consumidor usa um filtro de eventos para se registrar para receber a notificação de um tipo específico de evento.</span><span class="sxs-lookup"><span data-stu-id="49c85-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="49c85-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**provedor de eventos**</span><span class="sxs-lookup"><span data-stu-id="49c85-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-121">Um provedor WMI que monitora uma fonte de eventos e notifica o WMI quando ocorrem eventos.</span><span class="sxs-lookup"><span data-stu-id="49c85-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="49c85-122">Um provedor de eventos implementa as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e, às vezes, [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span><span class="sxs-lookup"><span data-stu-id="49c85-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="49c85-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**consulta de evento**</span><span class="sxs-lookup"><span data-stu-id="49c85-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-124">Uma instrução [*linguagem WQL*](gloss-w.md) que os consumidores de eventos usam para se registrar para receber notificações de eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="49c85-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="49c85-125">Um provedor de eventos usa uma consulta de evento para se registrar para gerar notificações de eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="49c85-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="49c85-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**esquema de extensão**</span><span class="sxs-lookup"><span data-stu-id="49c85-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-127">A terceira camada do [*esquema CIM*](gloss-c.md), que inclui extensões específicas da plataforma do esquema CIM, como Windows, UNIX e Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49c85-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="49c85-128">Consulte também [*modelo comum*](gloss-c.md) e modelo de núcleo.</span><span class="sxs-lookup"><span data-stu-id="49c85-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="49c85-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento extrínsecos**</span><span class="sxs-lookup"><span data-stu-id="49c85-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="49c85-130">Uma notificação de evento de um provedor.</span><span class="sxs-lookup"><span data-stu-id="49c85-130">An event notification from a provider.</span></span> <span data-ttu-id="49c85-131">A maioria dos provedores cria uma instância de uma classe de evento definida nos arquivos MOF do provedor.</span><span class="sxs-lookup"><span data-stu-id="49c85-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="49c85-132">Um evento extrínsecos herda de [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="49c85-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="49c85-133">Por exemplo, o [provedor de log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) define a classe de evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="49c85-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="49c85-134">Consulte também [*evento intrínseco*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="49c85-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
