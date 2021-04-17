---
description: Um filtro de eventos é uma classe WMI que descreve quais eventos o WMI fornece a um consumidor físico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Criando um filtro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766530"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="830d0-103">Criando um filtro de eventos</span><span class="sxs-lookup"><span data-stu-id="830d0-103">Creating an Event Filter</span></span>

<span data-ttu-id="830d0-104">Um filtro de eventos é uma classe WMI que descreve quais eventos o WMI fornece a um consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="830d0-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="830d0-105">Por exemplo, um filtro de eventos pode instruir o WMI a fornecer a um consumidor todos os eventos de gerenciamento de energia ou todos os eventos de reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="830d0-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="830d0-106">Um filtro de eventos também descreve as condições sob as quais o WMI fornece os eventos.</span><span class="sxs-lookup"><span data-stu-id="830d0-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="830d0-107">Um filtro de eventos pode especificar um evento intrínseco ou extrínsecos; e o filtro pode se referir a eventos que se originam no namespace, ou seja, que não seja o namespace do filtro.</span><span class="sxs-lookup"><span data-stu-id="830d0-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="830d0-108">O consumidor permanente deve ter o mesmo [**CreatorSID**](--eventconsumer.md) nas instâncias de consumidor, filtro e associação.</span><span class="sxs-lookup"><span data-stu-id="830d0-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="830d0-109">Para obter mais informações, consulte [recebendo eventos com segurança](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="830d0-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="830d0-110">O procedimento a seguir descreve como criar um filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="830d0-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="830d0-111">**Para criar um filtro de eventos**</span><span class="sxs-lookup"><span data-stu-id="830d0-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="830d0-112">Crie uma instância da classe de sistema WMI [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="830d0-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="830d0-113">Crie um identificador exclusivo para o filtro com a propriedade **Name** , de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="830d0-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="830d0-114">Use um esquema privado.</span><span class="sxs-lookup"><span data-stu-id="830d0-114">Use a private scheme.</span></span>

        <span data-ttu-id="830d0-115">Nomear arbitrariamente os filtros de eventos funciona contanto que você não entre em conflito com outros esquemas de nomenclatura de filtro.</span><span class="sxs-lookup"><span data-stu-id="830d0-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="830d0-116">Você deve evitar conflitos de nomenclatura porque adicionar uma instância com um valor de **nome** duplicado substitui a instância antiga.</span><span class="sxs-lookup"><span data-stu-id="830d0-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="830d0-117">Use um GUID (identificador global exclusivo).</span><span class="sxs-lookup"><span data-stu-id="830d0-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="830d0-118">Se você deixar o **nome** vazio, o WMI preencherá o **nome** com um GUID.</span><span class="sxs-lookup"><span data-stu-id="830d0-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="830d0-119">Descreva o tipo de evento que você deseja filtrar com a propriedade de **consulta** .</span><span class="sxs-lookup"><span data-stu-id="830d0-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="830d0-120">A propriedade **Query** contém a consulta linguagem WQL (WQL) que descreve o tipo de evento que você deseja filtrar.</span><span class="sxs-lookup"><span data-stu-id="830d0-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="830d0-121">Você pode obter uma filtragem precisa usando uma variedade de operadores e extensões para WQL.</span><span class="sxs-lookup"><span data-stu-id="830d0-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="830d0-122">Um evento de log do NT é gerado quando uma consulta de um consumidor de evento permanente falha.</span><span class="sxs-lookup"><span data-stu-id="830d0-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="830d0-123">A origem do evento é WinMgmt, a ID do evento é 10 e o tipo de evento é Error.</span><span class="sxs-lookup"><span data-stu-id="830d0-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="830d0-124">O WMI é mais eficiente no processamento de consultas restritivas e específicas do que consultas amplas.</span><span class="sxs-lookup"><span data-stu-id="830d0-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="830d0-125">Ao criar uma consulta específica, você pode evitar a comunicação entre processos e o tráfego de rede desnecessários.</span><span class="sxs-lookup"><span data-stu-id="830d0-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="830d0-126">Em casos de eventos gerados por um provedor, o WMI executa a filtragem em processo para o provedor; Isso garante que apenas os eventos que correspondem ao filtro incorrem no custo de comunicação entre processos.</span><span class="sxs-lookup"><span data-stu-id="830d0-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="830d0-127">Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="830d0-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="830d0-128">Defina a propriedade **QueryLanguage** como o tipo de linguagem de consulta que você usa na propriedade de **consulta** .</span><span class="sxs-lookup"><span data-stu-id="830d0-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="830d0-129">Você quase sempre definirá **QueryLanguage** como "WQL".</span><span class="sxs-lookup"><span data-stu-id="830d0-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="830d0-130">O exemplo de código a seguir descreve um filtro de evento que sinaliza um evento cada vez que o WMI cria uma instância da classe [**\_ \_ TimerEvent**](--timerevent.md) no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="830d0-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="830d0-131">A propriedade **EventNamespace** especifica o namespace do qual os eventos se originam.</span><span class="sxs-lookup"><span data-stu-id="830d0-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="830d0-132">Você não precisa criar uma instância dos filtros no namespace onde os eventos se originam.</span><span class="sxs-lookup"><span data-stu-id="830d0-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="830d0-133">Se você não especificar o namespace, o WMI criará o filtro no namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="830d0-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="830d0-134">As classes de eventos intrínsecos, como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , estão disponíveis em todos os namespaces.</span><span class="sxs-lookup"><span data-stu-id="830d0-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="830d0-135">Para registrar seu consumidor lógico para notificações de eventos, você deve associar os filtros de eventos a um consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="830d0-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="830d0-136">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="830d0-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



