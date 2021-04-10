---
description: O WMI contém uma infraestrutura de eventos que produz notificações sobre alterações nos dados e serviços do WMI. As classes de evento WMI fornecem notificação quando eventos específicos ocorrem.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Recebendo um evento WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091304"
---
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="4e4b0-104">Recebendo um evento WMI</span><span class="sxs-lookup"><span data-stu-id="4e4b0-104">Receiving a WMI Event</span></span>

<span data-ttu-id="4e4b0-105">O WMI contém uma infraestrutura de eventos que produz notificações sobre alterações nos dados e serviços do WMI.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="4e4b0-106">As [*classes de evento*](gloss-e.md) WMI fornecem notificação quando eventos específicos ocorrem.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="4e4b0-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="4e4b0-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="4e4b0-108">Consultas de evento</span><span class="sxs-lookup"><span data-stu-id="4e4b0-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="4e4b0-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4e4b0-109">Example</span></span>](#example)
-   [<span data-ttu-id="4e4b0-110">Consumidores de eventos</span><span class="sxs-lookup"><span data-stu-id="4e4b0-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="4e4b0-111">Fornecendo eventos</span><span class="sxs-lookup"><span data-stu-id="4e4b0-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="4e4b0-112">Cotas de assinatura</span><span class="sxs-lookup"><span data-stu-id="4e4b0-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="4e4b0-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e4b0-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="4e4b0-114">Consultas de evento</span><span class="sxs-lookup"><span data-stu-id="4e4b0-114">Event Queries</span></span>

<span data-ttu-id="4e4b0-115">Você pode criar uma consulta [**assíncrona**](receiving-asynchronous-event-notifications.md) ou [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) para monitorar alterações em logs de eventos, criação de processos, status do serviço, disponibilidade do computador ou espaço livre da unidade de disco e outras entidades ou eventos.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="4e4b0-116">No script, o método [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) é usado para assinar eventos.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="4e4b0-117">Em C++, [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) é usado.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="4e4b0-118">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4e4b0-119">A notificação de uma alteração no modelo de dados padrão do WMI é chamada de [*evento intrínseco*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="4e4b0-120">[**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) ou [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) são exemplos de eventos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="4e4b0-121">A notificação de uma alteração que um provedor faz para definir um evento de provedor é chamada de [*evento extrínsecos*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="4e4b0-122">Por exemplo, o provedor de [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), o provedor de eventos de [Gerenciamento de energia](/windows/desktop/CIMWin32Prov/power-management-event-provider)e o [Provedor Win32](/windows/desktop/CIMWin32Prov/win32-provider) definem seus próprios eventos.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="4e4b0-123">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="4e4b0-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4e4b0-124">Example</span></span>

<span data-ttu-id="4e4b0-125">O exemplo de código de script a seguir é uma consulta para o [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrínseco da classe de evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="4e4b0-126">Você pode executar esse programa em segundo plano e, quando houver um evento, será exibida uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="4e4b0-127">Se você fechar a caixa de diálogo **aguardando eventos** , o programa parará de aguardar eventos.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="4e4b0-128">Lembre-se de que **SeSecurityPrivilege** deve estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





<span data-ttu-id="4e4b0-129">O exemplo de código VBScript a seguir mostra o evento extrínsecos [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) que o provedor do registro define.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="4e4b0-130">O script cria um consumidor temporário usando a chamada para [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)e recebe apenas eventos quando o script está em execução.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="4e4b0-131">O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="4e4b0-132">Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="4e4b0-133">Para interrompê-lo programaticamente, use o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe de processo do Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="4e4b0-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="4e4b0-134">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a><span data-ttu-id="4e4b0-135">Consumidores de evento</span><span class="sxs-lookup"><span data-stu-id="4e4b0-135">Event Consumers</span></span>

<span data-ttu-id="4e4b0-136">Você pode monitorar ou consumir eventos usando os seguintes consumidores enquanto um script ou aplicativo está em execução:</span><span class="sxs-lookup"><span data-stu-id="4e4b0-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="4e4b0-137">Consumidores de eventos temporários</span><span class="sxs-lookup"><span data-stu-id="4e4b0-137">Temporary event consumers</span></span>

    <span data-ttu-id="4e4b0-138">Um [*consumidor temporário*](gloss-t.md) é um aplicativo cliente WMI que recebe um evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="4e4b0-139">O WMI inclui uma interface exclusiva que usa o para especificar os eventos que o WMI deve enviar a um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="4e4b0-140">Um consumidor de evento temporário é considerado temporário porque só funciona quando é especificamente carregado por um usuário.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="4e4b0-141">Para obter mais informações, consulte [recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="4e4b0-142">Consumidores de eventos permanentes</span><span class="sxs-lookup"><span data-stu-id="4e4b0-142">Permanent event consumers</span></span>

    <span data-ttu-id="4e4b0-143">Um [*consumidor permanente*](gloss-p.md) é um objeto com que pode receber um evento WMI em todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="4e4b0-144">Um consumidor de evento permanente usa um conjunto de objetos persistentes e filtros para capturar um evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="4e4b0-145">Como um consumidor de evento temporário, você configura uma série de objetos e filtros do WMI que capturam um evento WMI.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="4e4b0-146">Quando ocorre um evento que corresponde a um filtro, o WMI carrega o consumidor de evento permanente e o notifica sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="4e4b0-147">Como um consumidor permanente é implementado no repositório do WMI e é um arquivo executável registrado no WMI, o consumidor de evento permanente Opera e recebe eventos depois que ele é criado e, mesmo após uma reinicialização do sistema operacional, desde que o WMI esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="4e4b0-148">Para obter mais informações, consulte [recebendo eventos em todos os momentos](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="4e4b0-149">Scripts ou aplicativos que recebem eventos têm considerações de segurança especiais.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="4e4b0-150">Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="4e4b0-151">Um aplicativo ou script pode usar um provedor de eventos interno do WMI que fornece [classes de consumidor padrão](standard-consumer-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="4e4b0-152">Cada classe de consumidor padrão responde a um evento com uma ação diferente, enviando uma mensagem de email ou executando um script.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="4e4b0-153">Você não precisa escrever o código do provedor para usar uma classe de consumidor padrão para criar um consumidor de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="4e4b0-154">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="4e4b0-155">Fornecendo eventos</span><span class="sxs-lookup"><span data-stu-id="4e4b0-155">Providing Events</span></span>

<span data-ttu-id="4e4b0-156">Um provedor de eventos é um componente COM que envia um evento para o WMI.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="4e4b0-157">Você pode criar um provedor de eventos para enviar um evento em um aplicativo C++ ou C#.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="4e4b0-158">A maioria dos provedores de eventos gerencia um objeto para o WMI, por exemplo, um aplicativo ou item de hardware.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="4e4b0-159">Para obter mais informações, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="4e4b0-160">Um evento cronometrado ou repetitivo é um evento que ocorre em um momento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="4e4b0-161">O WMI fornece as seguintes maneiras de criar eventos cronometrados ou repetidos para seus aplicativos:</span><span class="sxs-lookup"><span data-stu-id="4e4b0-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="4e4b0-162">A infra-estrutura de eventos padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="4e4b0-163">Uma classe de temporizador especializada.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-163">A specialized timer class.</span></span>

<span data-ttu-id="4e4b0-164">Para obter mais informações, consulte [recebendo um evento cronometrado ou repetido](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="4e4b0-165">Ao escrever um provedor de eventos, considere as informações de segurança identificadas no [fornecimento de eventos com segurança](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="4e4b0-166">É recomendável que as assinaturas de evento permanentes sejam compiladas \\ no \\ namespace da assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="4e4b0-167">Para obter mais informações, consulte [implementando assinaturas de eventos permanentes de namespace cruzado](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="4e4b0-168">Cotas de assinatura</span><span class="sxs-lookup"><span data-stu-id="4e4b0-168">Subscription Quotas</span></span>

<span data-ttu-id="4e4b0-169">A sondagem de eventos pode prejudicar o desempenho de provedores que dão suporte a consultas em grandes conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="4e4b0-170">Além disso, qualquer usuário que tenha acesso de leitura a um namespace com provedores dinâmicos pode executar um ataque de negação de serviço (DoS).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="4e4b0-171">O WMI mantém cotas para todos os usuários combinados e para cada consumidor de evento na única instância do [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) localizado no \\ namespace raiz.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="4e4b0-172">Essas cotas são globais em vez de para cada namespace.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="4e4b0-173">Você não pode alterar as cotas.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-173">You cannot change the quotas.</span></span>

<span data-ttu-id="4e4b0-174">Atualmente, o WMI impõe cotas usando as propriedades de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="4e4b0-175">Cada cota tem um por usuário e uma versão total que inclui todos os usuários combinados, não por namespace.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="4e4b0-176">A tabela a seguir lista as cotas que se aplicam às propriedades **\_ \_ ArbitratorConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="4e4b0-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="4e4b0-177">Total/Peruser</span><span class="sxs-lookup"><span data-stu-id="4e4b0-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="4e4b0-178">Quota</span><span class="sxs-lookup"><span data-stu-id="4e4b0-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4e4b0-179">TemporarySubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="4e4b0-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="4e4b0-180">TemporarySubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="4e4b0-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="4e4b0-181">10.000</span><span class="sxs-lookup"><span data-stu-id="4e4b0-181">10,000</span></span><br/> <span data-ttu-id="4e4b0-182">1,000</span><span class="sxs-lookup"><span data-stu-id="4e4b0-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="4e4b0-183">PermanentSubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="4e4b0-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="4e4b0-184">PermanentSubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="4e4b0-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="4e4b0-185">10.000</span><span class="sxs-lookup"><span data-stu-id="4e4b0-185">10,000</span></span><br/> <span data-ttu-id="4e4b0-186">1,000</span><span class="sxs-lookup"><span data-stu-id="4e4b0-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="4e4b0-187">PollingInstructionsTotal</span><span class="sxs-lookup"><span data-stu-id="4e4b0-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="4e4b0-188">PollingInstructionsPerUser</span><span class="sxs-lookup"><span data-stu-id="4e4b0-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="4e4b0-189">10.000</span><span class="sxs-lookup"><span data-stu-id="4e4b0-189">10,000</span></span><br/> <span data-ttu-id="4e4b0-190">1,000</span><span class="sxs-lookup"><span data-stu-id="4e4b0-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="4e4b0-191">PollingMemoryTotal</span><span class="sxs-lookup"><span data-stu-id="4e4b0-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="4e4b0-192">PollingMemoryPerUser</span><span class="sxs-lookup"><span data-stu-id="4e4b0-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="4e4b0-193">10 milhões (0x989680) bytes</span><span class="sxs-lookup"><span data-stu-id="4e4b0-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="4e4b0-194">5 milhões (0x4CB40) bytes</span><span class="sxs-lookup"><span data-stu-id="4e4b0-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="4e4b0-195">Um administrador ou um usuário com permissão de **\_ gravação completa** no namespace pode modificar a instância singleton de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4e4b0-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="4e4b0-196">O WMI rastreia a cota por usuário.</span><span class="sxs-lookup"><span data-stu-id="4e4b0-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e4b0-197">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e4b0-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e4b0-198">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="4e4b0-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

