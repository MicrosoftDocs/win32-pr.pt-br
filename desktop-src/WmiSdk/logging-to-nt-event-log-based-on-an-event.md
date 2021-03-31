---
description: A classe NTEventLogEventConsumer grava uma mensagem no log de eventos do Windows quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Registrando no log de eventos NT com base em um evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829266"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a><span data-ttu-id="2ed50-104">Registrando no log de eventos NT com base em um evento</span><span class="sxs-lookup"><span data-stu-id="2ed50-104">Logging to NT Event Log Based on an Event</span></span>

<span data-ttu-id="2ed50-105">A classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) grava uma mensagem no log de eventos do Windows quando ocorre um evento especificado.</span><span class="sxs-lookup"><span data-stu-id="2ed50-105">The [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class writes a message to the Windows Event log when a specified event occurs.</span></span> <span data-ttu-id="2ed50-106">Essa classe é um consumidor de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="2ed50-106">This class is a standard event consumer that WMI provides.</span></span>

> [!Note]  
> <span data-ttu-id="2ed50-107">Os usuários autenticados não podem, por padrão, registrar eventos no log do aplicativo em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="2ed50-107">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="2ed50-108">Como resultado, o exemplo descrito neste tópico falhará se você usar a propriedade **UNCServerName** da classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) e especificar um computador remoto como seu valor.</span><span class="sxs-lookup"><span data-stu-id="2ed50-108">As a result, the example described in this topic will fail if you use the **UNCServerName** property of the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class and specify a remote computer as its value.</span></span> <span data-ttu-id="2ed50-109">Para saber como alterar a segurança do log de eventos, consulte este [artigo da base de conhecimento](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="2ed50-109">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

 

<span data-ttu-id="2ed50-110">O procedimento básico para usar um consumidor padrão é descrito em [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-110">The basic procedure for using a standard consumer is described in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="2ed50-111">Veja a seguir etapas adicionais além do procedimento básico, necessárias ao usar a classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed50-111">The following are additional steps beyond the basic procedure, required when using the [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) class.</span></span> <span data-ttu-id="2ed50-112">As etapas descrevem como criar um consumidor de eventos que grava no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ed50-112">The steps describe how to create an event consumer that writes to the Application event log.</span></span>

<span data-ttu-id="2ed50-113">O procedimento a seguir descreve como criar um consumidor de eventos que grava no log de eventos do NT.</span><span class="sxs-lookup"><span data-stu-id="2ed50-113">The following procedure describes how to create an event consumer that writes to the NT Event Log.</span></span>

<span data-ttu-id="2ed50-114">**Para criar um consumidor de eventos que grava no log de eventos do Windows**</span><span class="sxs-lookup"><span data-stu-id="2ed50-114">**To create an event consumer that writes to the Windows Event Log**</span></span>

1.  <span data-ttu-id="2ed50-115">Em um arquivo formato MOF (MOF), crie uma instância de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) para receber os eventos solicitados na consulta.</span><span class="sxs-lookup"><span data-stu-id="2ed50-115">In a Managed Object Format (MOF) file, create an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="2ed50-116">Para obter mais informações sobre como escrever código MOF, consulte [criando Classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-116">For more information about writing MOF code, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="2ed50-117">Criar e nomear uma instância de [**\_ \_ EventFilter**](--eventfilter.md)e, em seguida, criar uma consulta para especificar o tipo de evento que dispara a gravação no log de eventos do NT.</span><span class="sxs-lookup"><span data-stu-id="2ed50-117">Create, and name, an instance of [**\_\_EventFilter**](--eventfilter.md), and then create a query to specify the type of event which triggers writing to the NT Event Log.</span></span>

    <span data-ttu-id="2ed50-118">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-118">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

3.  <span data-ttu-id="2ed50-119">Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-119">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span>
4.  <span data-ttu-id="2ed50-120">Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-120">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="2ed50-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2ed50-121">Example</span></span>

<span data-ttu-id="2ed50-122">O exemplo nesta seção está no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-122">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="2ed50-123">O exemplo mostra como criar um consumidor para gravar no log de eventos do aplicativo usando [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="2ed50-123">The example shows how to create a consumer to write to the Application event log by using [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="2ed50-124">O MOF cria uma nova classe chamada "NTLogCons \_ example", um filtro de eventos para consultar operações, como a criação, em uma instância dessa nova classe e uma associação entre o filtro e o consumidor.</span><span class="sxs-lookup"><span data-stu-id="2ed50-124">The MOF creates a new class named "NTLogCons\_Example", an event filter to query for operations, such as creation, on an instance of this new class, and a binding between filter and consumer.</span></span> <span data-ttu-id="2ed50-125">Como a última ação no MOF é criar uma instância do \_ exemplo NTLogCons, você pode ver imediatamente o evento no log de eventos do aplicativo executando Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="2ed50-125">Because the last action in the MOF is to create an instance of NTLogCons\_Example, you can immediately see the event in the Application event log by running Eventvwr.exe.</span></span>

<span data-ttu-id="2ed50-126">O `EventID=0x0A for SourceName="WinMgmt"` identifica uma mensagem com o texto a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ed50-126">The `EventID=0x0A for SourceName="WinMgmt"` identifies a message with the following text.</span></span> <span data-ttu-id="2ed50-127">"%1", "%2", "%3" são espaços reservados para cadeias de caracteres correspondentes especificadas na matriz InsertionStringTemplates.</span><span class="sxs-lookup"><span data-stu-id="2ed50-127">The "%1", "%2", "%3" are placeholders for corresponding strings specified in InsertionStringTemplates array.</span></span>

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

<span data-ttu-id="2ed50-128">O procedimento a seguir descreve como usar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="2ed50-128">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="2ed50-129">**Para usar o exemplo**</span><span class="sxs-lookup"><span data-stu-id="2ed50-129">**To use the example**</span></span>

1.  <span data-ttu-id="2ed50-130">Copie a listagem MOF abaixo em um arquivo de texto e salve-a com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="2ed50-130">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="2ed50-131">Em um janela Comando, compile o arquivo MOF usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="2ed50-131">In a Command window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="2ed50-132"> *Nome do arquivo Mofcomp\ *\ * *. mof**</span><span class="sxs-lookup"><span data-stu-id="2ed50-132">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="2ed50-133">Execute Eventvwr.exe.</span><span class="sxs-lookup"><span data-stu-id="2ed50-133">Run Eventvwr.exe.</span></span> <span data-ttu-id="2ed50-134">Examine o log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ed50-134">Look at the Application event log.</span></span> <span data-ttu-id="2ed50-135">Você deverá ver um evento com ID = 10 ( **EventID**), Source = "WMI" e Type = erro.</span><span class="sxs-lookup"><span data-stu-id="2ed50-135">You should see an event with ID = 10 (the **EventID**), Source = "WMI", and Type = Error.</span></span>
4.  <span data-ttu-id="2ed50-136">Clique duas vezes na mensagem **tipo de informação** do WMI com 10 na coluna **evento** .</span><span class="sxs-lookup"><span data-stu-id="2ed50-136">Double-click the **Information type** message from WMI with 10 in the **Event** column.</span></span> <span data-ttu-id="2ed50-137">A descrição a seguir será exibida para o evento.</span><span class="sxs-lookup"><span data-stu-id="2ed50-137">The following description will be displayed for the event.</span></span>

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a><span data-ttu-id="2ed50-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ed50-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed50-139">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="2ed50-139">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



