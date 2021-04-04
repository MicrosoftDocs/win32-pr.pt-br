---
description: Você pode usar as classes de consumidor padrão instaladas para executar ações com base em eventos em um sistema operacional.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Monitorando e respondendo a eventos com consumidores padrão
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103837990"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a><span data-ttu-id="a056d-103">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="a056d-103">Monitoring and Responding to Events with Standard Consumers</span></span>

<span data-ttu-id="a056d-104">Você pode usar as [classes de consumidor padrão](standard-consumer-classes.md) instaladas para executar ações com base em eventos em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a056d-104">You can use the installed [standard consumer classes](standard-consumer-classes.md) to perform actions based on events in an operating system.</span></span> <span data-ttu-id="a056d-105">Os consumidores padrão são classes simples que já estão registradas e definem classes de consumo permanentes.</span><span class="sxs-lookup"><span data-stu-id="a056d-105">Standard consumers are simple classes that are already registered, and they define permanent consumer classes.</span></span> <span data-ttu-id="a056d-106">Cada consumidor padrão executa uma ação específica depois de receber uma notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="a056d-106">Each standard consumer takes a specific action after it receives an event notification.</span></span> <span data-ttu-id="a056d-107">Por exemplo, você pode definir uma instância de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para executar um script quando o espaço livre em disco em um computador for diferente de um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="a056d-107">For example, you can define an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to execute a script when free disk space on a computer is different from a specified size.</span></span>

<span data-ttu-id="a056d-108">O WMI compila os consumidores padrão em namespaces padrão que dependem do sistema operacional, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a056d-108">WMI compiles the standard consumers into default namespaces that depend on the operating system, for example:</span></span>

-   <span data-ttu-id="a056d-109">No Windows Server 2003, todos os consumidores padrão são compilados por padrão no \\ namespace "assinatura raiz".</span><span class="sxs-lookup"><span data-stu-id="a056d-109">In Windows Server 2003, all of the standard consumers are compiled by default into the "Root\\Subscription" namespace.</span></span>

> [!Note]  
> <span data-ttu-id="a056d-110">Para os namespaces e sistemas operacionais padrão específicos para cada classe WMI, consulte as seções comentários e requisitos de cada tópico de classe.</span><span class="sxs-lookup"><span data-stu-id="a056d-110">For the default namespaces and operating systems that are specific for each WMI class, see the Remarks and Requirements sections of each class topic.</span></span>

 

<span data-ttu-id="a056d-111">A tabela a seguir lista e descreve os consumidores padrão do WMI.</span><span class="sxs-lookup"><span data-stu-id="a056d-111">The following table lists and describes the WMI standard consumers.</span></span>



| <span data-ttu-id="a056d-112">Consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="a056d-112">Standard consumer</span></span>                                              | <span data-ttu-id="a056d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a056d-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a056d-114">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a056d-114">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md) | <span data-ttu-id="a056d-115">Executa um script quando recebe uma notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="a056d-115">Executes a script when it receives an event notification.</span></span> <span data-ttu-id="a056d-116">Para obter mais informações, consulte [executando um script com base em um evento](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-116">For more information, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="a056d-117">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a056d-117">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)           | <span data-ttu-id="a056d-118">Grava cadeias de caracteres personalizadas em um arquivo de log de texto quando recebe uma notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="a056d-118">Writes customized strings to a text log file when it receives an event notification.</span></span> <span data-ttu-id="a056d-119">Para obter mais informações, consulte [gravando em um arquivo de log com base em um evento](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-119">For more information, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="a056d-120">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a056d-120">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)     | <span data-ttu-id="a056d-121">Registra uma mensagem específica no log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a056d-121">Logs a specific message to the Application event log.</span></span> <span data-ttu-id="a056d-122">Para obter mais informações, consulte [registrando em log o log de eventos NT com base em um evento](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-122">For more information, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="a056d-123">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a056d-123">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                 | <span data-ttu-id="a056d-124">Envia uma mensagem de email usando SMTP cada vez que um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="a056d-124">Sends an email message by using SMTP each time an event is delivered to it.</span></span> <span data-ttu-id="a056d-125">Para obter mais informações, consulte [enviando email com base em um evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-125">For more information, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a056d-126">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="a056d-126">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)   | <span data-ttu-id="a056d-127">Inicia um processo quando um evento é entregue a um sistema local.</span><span class="sxs-lookup"><span data-stu-id="a056d-127">Launches a process when an event is delivered to a local system.</span></span> <span data-ttu-id="a056d-128">O arquivo executável deve estar em um local seguro ou protegido com uma ACL (lista de controle de acesso) forte para impedir que um usuário não autorizado substitua seu executável por um executável diferente.</span><span class="sxs-lookup"><span data-stu-id="a056d-128">The executable file must be in a secure location, or secured with a strong access control list (ACL) to prevent an unauthorized user from replacing your executable with a different executable.</span></span> <span data-ttu-id="a056d-129">Para obter mais informações, consulte [executando um programa da linha de comando com base em um evento](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-129">For more information, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span> |



 

<span data-ttu-id="a056d-130">O procedimento a seguir descreve como monitorar e responder a eventos usando um consumidor padrão.</span><span class="sxs-lookup"><span data-stu-id="a056d-130">The following procedure describes how to monitor and respond to events by using a standard consumer.</span></span> <span data-ttu-id="a056d-131">Observe que o procedimento é o mesmo para um arquivo, script ou aplicativo formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a056d-131">Note that the procedure is the same for a Managed Object Format (MOF) file, script, or application.</span></span>

<span data-ttu-id="a056d-132">**Para monitorar e responder a eventos com um consumidor padrão**</span><span class="sxs-lookup"><span data-stu-id="a056d-132">**To monitor and respond to events with a standard consumer**</span></span>

1.  <span data-ttu-id="a056d-133">Especifique o namespace em um arquivo MOF usando o [ \# namespace de pragma](pragma-namespace.md)do comando de pré-processador MOF.</span><span class="sxs-lookup"><span data-stu-id="a056d-133">Specify the namespace in a MOF file by using the MOF preprocessor command [\#pragma namespace](pragma-namespace.md).</span></span> <span data-ttu-id="a056d-134">Em um script ou aplicativo, especifique o namespace no código que se conecta ao WMI.</span><span class="sxs-lookup"><span data-stu-id="a056d-134">In a script or application, specify the namespace in the code that connects to WMI.</span></span>

    <span data-ttu-id="a056d-135">O exemplo de código MOF a seguir mostra como especificar o \\ namespace de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="a056d-135">The following MOF code example shows how to specify the root\\subscription namespace.</span></span>

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    <span data-ttu-id="a056d-136">A maioria dos [*eventos intrínsecos*](gloss-i.md) está associada às alterações em instâncias de classe no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="a056d-136">Most [*intrinsic events*](gloss-i.md) are associated with changes to class instances in the root\\cimv2 namespace.</span></span> <span data-ttu-id="a056d-137">No entanto, eventos de registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) são acionados no \\ namespace raiz padrão pelo [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).</span><span class="sxs-lookup"><span data-stu-id="a056d-137">However, registry events such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) are fired in the root\\default namespace by the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

    <span data-ttu-id="a056d-138">Um consumidor pode incluir classes de evento localizadas em outros namespaces, especificando o namespace na propriedade **EventNamespace** na consulta [**\_ \_ EventFilter**](--eventfilter.md) para eventos.</span><span class="sxs-lookup"><span data-stu-id="a056d-138">A consumer can include event classes located in other namespaces by specifying the namespace in the **EventNamespace** property in the [**\_\_EventFilter**](--eventfilter.md) query for events.</span></span> <span data-ttu-id="a056d-139">As classes de [*eventos intrínsecos*](gloss-i.md) , como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , estão disponíveis em todos os namespaces.</span><span class="sxs-lookup"><span data-stu-id="a056d-139">The [*intrinsic events*](gloss-i.md) classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

2.  <span data-ttu-id="a056d-140">Crie e popule uma instância de uma classe de consumidor padrão.</span><span class="sxs-lookup"><span data-stu-id="a056d-140">Create and populate an instance of a standard consumer class.</span></span>

    <span data-ttu-id="a056d-141">Essa instância pode ter um valor exclusivo na propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="a056d-141">This instance may have a unique value in the **Name** property.</span></span> <span data-ttu-id="a056d-142">Você pode atualizar um consumidor existente reutilizando o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a056d-142">You can update an existing consumer by reusing the same name.</span></span>

    <span data-ttu-id="a056d-143">**InsertionStringTemplates** contém o texto a ser inserido em um evento que você especifica no **EventType**.</span><span class="sxs-lookup"><span data-stu-id="a056d-143">**InsertionStringTemplates** contains the text to insert in an event that you specify in **EventType**.</span></span> <span data-ttu-id="a056d-144">Você pode usar cadeias de caracteres literais ou fazer referência diretamente a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="a056d-144">You can use literal strings or refer directly to a property.</span></span> <span data-ttu-id="a056d-145">Para obter mais informações, consulte [usando modelos de cadeia de caracteres padrão](using-standard-string-templates.md) e [instrução SELECT para consultas de evento](select-statement-for-event-queries.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-145">For more information, see [Using Standard String Templates](using-standard-string-templates.md) and [SELECT Statement for Event Queries](select-statement-for-event-queries.md).</span></span>

    <span data-ttu-id="a056d-146">Use uma fonte existente para o log de eventos que ofereça suporte a uma cadeia de caracteres de inserção sem texto associado.</span><span class="sxs-lookup"><span data-stu-id="a056d-146">Use an existing source for the event log that supports an insertion string without associated text.</span></span>

    <span data-ttu-id="a056d-147">O exemplo de código MOF a seguir mostra como usar uma fonte existente do WSH e um valor de **EventID** de 8.</span><span class="sxs-lookup"><span data-stu-id="a056d-147">The following MOF code example shows how to use an existing source of WSH and an **EventID** value of 8.</span></span>

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  <span data-ttu-id="a056d-148">Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e defina uma consulta para eventos.</span><span class="sxs-lookup"><span data-stu-id="a056d-148">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query for events.</span></span>

    <span data-ttu-id="a056d-149">No exemplo a seguir, o filtro monitora a chave do registro onde os programas de inicialização são registrados.</span><span class="sxs-lookup"><span data-stu-id="a056d-149">In the following example, the filter monitors the registry key where startup programs are registered.</span></span> <span data-ttu-id="a056d-150">O monitoramento dessa chave do registro pode ser importante porque um programa não autorizado pode se registrar na chave, o que faz com que ela seja iniciada quando o computador é inicializado.</span><span class="sxs-lookup"><span data-stu-id="a056d-150">Monitoring this registry key may be important because an unauthorized program can register itself under the key, which causes it to be launched when the computer boots.</span></span>

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  <span data-ttu-id="a056d-151">Identifique um evento para monitorar e criar uma consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="a056d-151">Identify an event to monitor and create an event query.</span></span>

    <span data-ttu-id="a056d-152">Você pode verificar se há um evento intrínseco ou extrínsecos que usa.</span><span class="sxs-lookup"><span data-stu-id="a056d-152">You can check to see if there is an intrinsic or extrinsic event that use.</span></span> <span data-ttu-id="a056d-153">Por exemplo, use a classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) do provedor de registro para monitorar alterações no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="a056d-153">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="a056d-154">Se não existir uma classe que descreva um evento que você precisa monitorar, você deverá criar seu próprio provedor de eventos e definir novas classes de evento extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="a056d-154">If a class does not exist that describes an event you need to monitor, you must create your own event provider, and define new extrinsic event classes.</span></span> <span data-ttu-id="a056d-155">Para obter mais informações, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-155">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

    <span data-ttu-id="a056d-156">Em um arquivo MOF, você pode definir um [*alias*](gloss-a.md) para o filtro e o consumidor, que fornece uma maneira fácil de descrever os caminhos de instância.</span><span class="sxs-lookup"><span data-stu-id="a056d-156">In a MOF file, you can define an [*alias*](gloss-a.md) for the filter and consumer, which provides an easy way to describe the instance paths.</span></span>

    <span data-ttu-id="a056d-157">O exemplo a seguir mostra como definir um [*alias*](gloss-a.md) para o filtro e o consumidor.</span><span class="sxs-lookup"><span data-stu-id="a056d-157">The following example shows how to define an [*alias*](gloss-a.md) for the filter and consumer.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  <span data-ttu-id="a056d-158">Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar as classes de filtro e de consumidor.</span><span class="sxs-lookup"><span data-stu-id="a056d-158">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer classes.</span></span> <span data-ttu-id="a056d-159">Essa instância determina que quando ocorrer um evento que corresponda ao filtro especificado, a ação especificada pelo consumidor deverá ocorrer.</span><span class="sxs-lookup"><span data-stu-id="a056d-159">This instance determines that when an event occurs that matches the specified filter, the action specified by the consumer must occur.</span></span> <span data-ttu-id="a056d-160">[**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e **\_ \_ FilterToConsumerBinding** devem ter o mesmo SID (identificador de segurança individual) na propriedade **CreatorSID** .</span><span class="sxs-lookup"><span data-stu-id="a056d-160">[**\_\_EventFilter**](--eventfilter.md), [**\_\_EventConsumer**](--eventconsumer.md), and **\_\_FilterToConsumerBinding** must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="a056d-161">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-161">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

    <span data-ttu-id="a056d-162">O exemplo a seguir mostra como identificar uma instância pelo caminho do objeto ou usar um alias como uma expressão abreviada para o caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="a056d-162">The following example shows how to identify an instance by the object path, or use an alias as a shorthand expression for the object path.</span></span>

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    <span data-ttu-id="a056d-163">O exemplo a seguir associa o filtro ao consumidor usando aliases.</span><span class="sxs-lookup"><span data-stu-id="a056d-163">The following example binds the filter to the consumer by using aliases.</span></span>

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    <span data-ttu-id="a056d-164">Você pode associar um filtro a vários consumidores, o que indica que quando ocorrem eventos correspondentes, várias ações devem ser executadas; ou você pode associar um consumidor a vários filtros, o que indica que a ação deve ser executada quando os eventos que correspondem a um dos filtros ocorrerem.</span><span class="sxs-lookup"><span data-stu-id="a056d-164">You can bind one filter to several consumers, which indicates that when matching events occur, several actions must be taken; or you can bind one consumer to several filters, which indicates that the action must be taken when events that match one of the filters occur.</span></span>

    <span data-ttu-id="a056d-165">As seguintes ações são executadas com base na condição de consumidores e eventos:</span><span class="sxs-lookup"><span data-stu-id="a056d-165">The following actions are taken based on the condition of consumers and events:</span></span>

    -   <span data-ttu-id="a056d-166">Se um dos consumidores permanentes falhar, outros consumidores que solicitarem a notificação de recebimento de eventos.</span><span class="sxs-lookup"><span data-stu-id="a056d-166">If one of the permanent consumers fails, other consumers that request the event receive notification.</span></span>
    -   <span data-ttu-id="a056d-167">Se um evento for descartado, o WMI será acionado [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-167">If an event is dropped, WMI fires [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>
    -   <span data-ttu-id="a056d-168">Se você assinar esse evento, ele retornará o evento que será descartado e uma referência ao [**\_ \_ EventConsumer**](--eventconsumer.md) representará o consumidor com falha.</span><span class="sxs-lookup"><span data-stu-id="a056d-168">If you subscribe to this event, it returns the event that is dropped, and a reference to the [**\_\_EventConsumer**](--eventconsumer.md) represents the failed consumer.</span></span>
    -   <span data-ttu-id="a056d-169">Se um consumidor falhar, o WMI aciona [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), que pode conter mais informações nas propriedades **ErrorCode**, **ErrorDescription** e **ErrorObject** .</span><span class="sxs-lookup"><span data-stu-id="a056d-169">If a consumer fails, WMI fires [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md), which may contain more information in the **ErrorCode**, **ErrorDescription** and **ErrorObject** properties.</span></span>

    <span data-ttu-id="a056d-170">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-170">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

## <a name="example"></a><span data-ttu-id="a056d-171">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a056d-171">Example</span></span>

<span data-ttu-id="a056d-172">O exemplo a seguir mostra o MOF para uma instância de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="a056d-172">The following example shows the MOF for an instance of [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).</span></span> <span data-ttu-id="a056d-173">Depois de compilar esse MOF, qualquer tentativa de criar, excluir ou modificar um valor no caminho do registro **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Execute** registra uma entrada no log de eventos do aplicativo, sob a origem "WSH".</span><span class="sxs-lookup"><span data-stu-id="a056d-173">After you compile this MOF, any attempt to create, delete, or modify a value in the Registry path **HKEY\_LOCAL\_MACHINE\\ Software\\Microsoft\\Windows\\CurrentVersion\\Run** logs an entry in the Application eventlog, under the source "WSH".</span></span>


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a><span data-ttu-id="a056d-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a056d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a056d-175">Recebendo eventos com segurança</span><span class="sxs-lookup"><span data-stu-id="a056d-175">Receiving Events Securely</span></span>](receiving-events-securely.md)
</dt> </dl>

 

 
