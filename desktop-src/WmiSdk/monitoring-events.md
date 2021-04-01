---
description: Os administradores do sistema podem usar o WMI para monitorar eventos em uma rede.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Monitorando eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090993"
---
# <a name="monitoring-events"></a><span data-ttu-id="026f0-103">Monitorando eventos</span><span class="sxs-lookup"><span data-stu-id="026f0-103">Monitoring Events</span></span>

<span data-ttu-id="026f0-104">Os administradores do sistema podem usar o WMI para monitorar eventos em uma rede.</span><span class="sxs-lookup"><span data-stu-id="026f0-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="026f0-105">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="026f0-105">For example:</span></span>

-   <span data-ttu-id="026f0-106">Um serviço é interrompido inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="026f0-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="026f0-107">Um servidor fica indisponível.</span><span class="sxs-lookup"><span data-stu-id="026f0-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="026f0-108">Uma unidade de disco preenche a capacidade de 80%.</span><span class="sxs-lookup"><span data-stu-id="026f0-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="026f0-109">Os eventos de segurança são relatados para um log de eventos do NT.</span><span class="sxs-lookup"><span data-stu-id="026f0-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="026f0-110">O WMI dá suporte à detecção e entrega de eventos para consumidores de eventos porque alguns provedores WMI são provedores de eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="026f0-111">Para obter mais informações, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="026f0-112">Os [*consumidores de eventos*](gloss-e.md) são aplicativos ou scripts que solicitam notificação de eventos e executam tarefas quando eventos específicos ocorrem.</span><span class="sxs-lookup"><span data-stu-id="026f0-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="026f0-113">Você pode criar scripts de monitoramento de eventos ou aplicativos que monitoram temporariamente quando ocorrem eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="026f0-114">O WMI também fornece um conjunto de provedores de eventos permanentes pré-instalados e as classes de consumo permanentes que permitem que você monitore eventos permanentemente.</span><span class="sxs-lookup"><span data-stu-id="026f0-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="026f0-115">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="026f0-116">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="026f0-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="026f0-117">Usando consumidores de eventos temporários</span><span class="sxs-lookup"><span data-stu-id="026f0-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="026f0-118">Usando consumidores de eventos permanentes</span><span class="sxs-lookup"><span data-stu-id="026f0-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="026f0-119">Usando consumidores de eventos temporários</span><span class="sxs-lookup"><span data-stu-id="026f0-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="026f0-120">Os consumidores de eventos temporários são scripts ou aplicativos que retornam os eventos que correspondem a uma consulta de evento ou filtro.</span><span class="sxs-lookup"><span data-stu-id="026f0-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="026f0-121">As consultas de evento temporárias geralmente usam [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) em aplicativos C++ ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) em scripts e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="026f0-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="026f0-122">Uma consulta de evento solicita instâncias de uma classe de evento que especifica um determinado tipo de evento, como [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="026f0-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="026f0-123">O exemplo de código VBScript a seguir solicita notificação quando uma instância do [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) é criada.</span><span class="sxs-lookup"><span data-stu-id="026f0-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="026f0-124">Uma instância dessa classe é gerada quando um processo é iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="026f0-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="026f0-125">Para executar o script, copie-o para um arquivo chamado event.vbs e use a seguinte linha de comando: **cscript event.vbs**.</span><span class="sxs-lookup"><span data-stu-id="026f0-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="026f0-126">Você pode ver a saída do script iniciando Notepad.exe ou qualquer outro processo.</span><span class="sxs-lookup"><span data-stu-id="026f0-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="026f0-127">O script é interrompido após cinco processos serem iniciados ou interrompidos.</span><span class="sxs-lookup"><span data-stu-id="026f0-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="026f0-128">Esse script chama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), que é a versão [*semisynchronous*](gloss-s.md) do método.</span><span class="sxs-lookup"><span data-stu-id="026f0-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="026f0-129">Consulte o próximo script para obter um exemplo de como configurar uma assinatura de evento temporário assíncrono chamando [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="026f0-130">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="026f0-131">O script chama [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para obter e processar cada evento conforme ele chega.</span><span class="sxs-lookup"><span data-stu-id="026f0-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="026f0-132">Salve o script em um arquivo com uma extensão. vbs e execute o script em uma linha de comando usando CScript: **cscript file.vbs**.</span><span class="sxs-lookup"><span data-stu-id="026f0-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Os consumidores de eventos temporários devem ser iniciados manualmente e não devem persistir nas reinicializações do WMI ou nas reinicializações do sistema operacional. <span data-ttu-id="026f0-134">Um consumidor de evento temporário pode processar eventos somente enquanto está em execução.</span><span class="sxs-lookup"><span data-stu-id="026f0-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="026f0-135">O procedimento a seguir descreve como criar um consumidor de evento temporário.</span><span class="sxs-lookup"><span data-stu-id="026f0-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="026f0-136">**Para criar um consumidor de evento temporário**</span><span class="sxs-lookup"><span data-stu-id="026f0-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="026f0-137">Decida qual linguagem de programação usar.</span><span class="sxs-lookup"><span data-stu-id="026f0-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="026f0-138">A linguagem de programação determina a API a ser usada.</span><span class="sxs-lookup"><span data-stu-id="026f0-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="026f0-139">Para a linguagem de programação C++, use a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="026f0-140">Para Visual Basic ou linguagens de script, use a [API de script para o WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="026f0-141">Comece a codificar um aplicativo de consumidor de evento temporário da mesma maneira que você inicia um aplicativo WMI.</span><span class="sxs-lookup"><span data-stu-id="026f0-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="026f0-142">As primeiras etapas de codificação dependem da linguagem de programação.</span><span class="sxs-lookup"><span data-stu-id="026f0-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="026f0-143">Normalmente, você faz logon no WMI e define as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="026f0-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="026f0-144">Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="026f0-145">Defina a consulta de evento que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="026f0-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="026f0-146">Para obter alguns tipos de dados de desempenho, talvez seja necessário usar classes fornecidas por provedores de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="026f0-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="026f0-147">Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md), [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)e [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="026f0-148">Decida fazer uma chamada assíncrona ou uma chamada semisynchronous e escolher o método de API.</span><span class="sxs-lookup"><span data-stu-id="026f0-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="026f0-149">As chamadas assíncronas permitem evitar a sobrecarga de sondagem de dados.</span><span class="sxs-lookup"><span data-stu-id="026f0-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="026f0-150">No entanto, as chamadas semisynchronous fornecem um desempenho semelhante com maior segurança.</span><span class="sxs-lookup"><span data-stu-id="026f0-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="026f0-151">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="026f0-152">Faça a chamada do método assíncrona ou semisynchronous e inclua uma consulta de evento como o parâmetro *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="026f0-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="026f0-153">Para aplicativos C++, chame os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="026f0-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="026f0-154">**IWbemServices:: ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="026f0-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="026f0-155">**IWbemServices:: ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="026f0-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="026f0-156">Para scripts, chame os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="026f0-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="026f0-157">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="026f0-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="026f0-158">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="026f0-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="026f0-159">Escreva o código para processar o objeto de evento retornado.</span><span class="sxs-lookup"><span data-stu-id="026f0-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="026f0-160">Para consultas de evento assíncrono, coloque o código nos vários métodos ou eventos do coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="026f0-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="026f0-161">Para consultas de eventos semisynchronous, cada objeto é retornado à medida que o WMI o Obtém, portanto, o código deve estar no loop que manipula cada objeto.</span><span class="sxs-lookup"><span data-stu-id="026f0-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="026f0-162">O exemplo de código de script a seguir é uma versão assíncrona do script [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="026f0-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="026f0-163">Como as operações assíncronas retornam imediatamente, uma caixa de diálogo mantém o script ativo enquanto está aguardando eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="026f0-164">Em vez de chamar [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para receber cada evento, o script tem um manipulador de eventos para o evento [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="026f0-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> <span data-ttu-id="026f0-165">Um retorno de chamada assíncrono, como um retorno de chamada manipulado pela `SINK_OnObjectReady` sub-rotina, permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="026f0-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="026f0-166">Para maior segurança, use a comunicação semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="026f0-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="026f0-167">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="026f0-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="026f0-168">Fazendo uma chamada Semisynchronous com C++</span><span class="sxs-lookup"><span data-stu-id="026f0-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="026f0-169">Fazendo uma chamada Semisynchronous com o VBScript</span><span class="sxs-lookup"><span data-stu-id="026f0-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="026f0-170">Fazendo uma chamada assíncrona com C++</span><span class="sxs-lookup"><span data-stu-id="026f0-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="026f0-171">Fazendo uma chamada assíncrona com o VBScript</span><span class="sxs-lookup"><span data-stu-id="026f0-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="026f0-172">Definindo a segurança em uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="026f0-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="026f0-173">Protegendo clientes de script</span><span class="sxs-lookup"><span data-stu-id="026f0-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="026f0-174">Usando consumidores de eventos permanentes</span><span class="sxs-lookup"><span data-stu-id="026f0-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="026f0-175">Um consumidor de evento permanente é executado até que seu registro seja explicitamente cancelado e, em seguida, iniciado quando o WMI ou o sistema for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="026f0-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="026f0-176">Um consumidor de evento permanente é uma combinação de classes, filtros e objetos COM do WMI em um sistema.</span><span class="sxs-lookup"><span data-stu-id="026f0-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="026f0-177">A lista a seguir identifica as partes necessárias para criar um consumidor de evento permanente:</span><span class="sxs-lookup"><span data-stu-id="026f0-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="026f0-178">Um objeto COM que contém o código que implementa o consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="026f0-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="026f0-179">Uma nova classe de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="026f0-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="026f0-180">Uma instância da classe de consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="026f0-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="026f0-181">Um filtro que contém a consulta de eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="026f0-182">Um link entre o consumidor e o filtro.</span><span class="sxs-lookup"><span data-stu-id="026f0-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="026f0-183">Para obter mais informações, consulte [recebendo eventos em todos os momentos](--filtertoconsumerbinding.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="026f0-184">O WMI fornece vários consumidores permanentes.</span><span class="sxs-lookup"><span data-stu-id="026f0-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="026f0-185">As classes de consumidor e o objeto COM que contém o código são pré-instalados.</span><span class="sxs-lookup"><span data-stu-id="026f0-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="026f0-186">Por exemplo, você pode criar e configurar uma instância da classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para executar um script quando ocorrer um evento.</span><span class="sxs-lookup"><span data-stu-id="026f0-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="026f0-187">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="026f0-188">Para obter um exemplo de como usar **ActiveScriptEventConsumer**, consulte [executando um script com base em um evento](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="026f0-189">O procedimento a seguir descreve como criar um consumidor de evento permanente.</span><span class="sxs-lookup"><span data-stu-id="026f0-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="026f0-190">**Para criar um consumidor de evento permanente**</span><span class="sxs-lookup"><span data-stu-id="026f0-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="026f0-191">[Registre o provedor de eventos](registering-a-provider.md) com o namespace que você está usando.</span><span class="sxs-lookup"><span data-stu-id="026f0-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="026f0-192">Alguns provedores de eventos só podem usar um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="026f0-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="026f0-193">Por exemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) é um evento intrínseco que é suportado pelo [provedor do Win32](/windows/desktop/CIMWin32Prov/win32-provider) e é registrado por padrão com o \\ \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="026f0-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="026f0-194">Você pode usar a propriedade **EventNamespace** do [**\_ \_ EventFilter**](--eventfilter.md) usado no registro para criar uma assinatura de namespace cruzado.</span><span class="sxs-lookup"><span data-stu-id="026f0-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="026f0-195">Para obter mais informações, consulte [implementando assinaturas de eventos permanentes de namespace cruzado](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="026f0-196">[Registre o provedor de consumidor de eventos](registering-an-event-consumer-provider.md) com o namespace em que as classes de evento estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="026f0-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="026f0-197">O WMI usa um provedor de consumidor de eventos para encontrar um consumidor de eventos que seja permanente.</span><span class="sxs-lookup"><span data-stu-id="026f0-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="026f0-198">O consumidor de evento permanente é o aplicativo que o WMI inicia quando um evento é recebido.</span><span class="sxs-lookup"><span data-stu-id="026f0-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="026f0-199">Para registrar o consumidor de eventos, os provedores criam instâncias de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="026f0-200">Crie uma instância da classe que representa o consumidor de evento permanente que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="026f0-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="026f0-201">As classes de consumidor de eventos são derivadas da classe [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="026f0-202">Defina as propriedades que a instância de consumidor de evento requer.</span><span class="sxs-lookup"><span data-stu-id="026f0-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="026f0-203">Registre o consumidor com o com usando o utilitário **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="026f0-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="026f0-204">Crie uma instância da classe de filtro de eventos [**\_ \_ EventFilter**](--eventfilter.md).</span><span class="sxs-lookup"><span data-stu-id="026f0-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="026f0-205">Defina os campos obrigatórios para a instância de filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="026f0-206">Os campos obrigatórios para [**\_ \_ EventFilter**](--eventfilter.md) são **Name**, **QueryLanguage** e **Query**.</span><span class="sxs-lookup"><span data-stu-id="026f0-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="026f0-207">A propriedade **Name** pode ser qualquer nome exclusivo para uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="026f0-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="026f0-208">A propriedade **QueryLanguage** é sempre definida como "WQL".</span><span class="sxs-lookup"><span data-stu-id="026f0-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="026f0-209">A propriedade de **consulta** é uma cadeia de caracteres que contém uma consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="026f0-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="026f0-210">Um evento é gerado quando uma consulta do consumidor de evento permanente falha.</span><span class="sxs-lookup"><span data-stu-id="026f0-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="026f0-211">A origem do evento é WinMgmt, a ID do evento é 10 e o tipo de evento é Error.</span><span class="sxs-lookup"><span data-stu-id="026f0-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="026f0-212">Crie uma instância da classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar um consumidor de evento lógico a um filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="026f0-213">O WMI usa uma associação para localizar o consumidor de eventos associado ao evento que corresponde aos critérios especificados no filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="026f0-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="026f0-214">O WMI usa o provedor de consumidor de eventos para encontrar o aplicativo de consumidor de evento permanente a ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="026f0-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
