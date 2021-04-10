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
# <a name="receiving-a-wmi-event"></a>Recebendo um evento WMI

O WMI contém uma infraestrutura de eventos que produz notificações sobre alterações nos dados e serviços do WMI. As [*classes de evento*](gloss-e.md) WMI fornecem notificação quando eventos específicos ocorrem.

As seções a seguir são discutidas neste tópico:

-   [Consultas de evento](#event-queries)
-   [Exemplo](#example)
-   [Consumidores de eventos](#event-consumers)
-   [Fornecendo eventos](#providing-events)
-   [Cotas de assinatura](#subscription-quotas)
-   [Tópicos relacionados](#related-topics)

## <a name="event-queries"></a>Consultas de evento

Você pode criar uma consulta [**assíncrona**](receiving-asynchronous-event-notifications.md) ou [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) para monitorar alterações em logs de eventos, criação de processos, status do serviço, disponibilidade do computador ou espaço livre da unidade de disco e outras entidades ou eventos. No script, o método [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) é usado para assinar eventos. Em C++, [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) é usado. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

A notificação de uma alteração no modelo de dados padrão do WMI é chamada de [*evento intrínseco*](gloss-i.md). [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) ou [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) são exemplos de eventos intrínsecos. A notificação de uma alteração que um provedor faz para definir um evento de provedor é chamada de [*evento extrínsecos*](gloss-e.md). Por exemplo, o provedor de [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), o provedor de eventos de [Gerenciamento de energia](/windows/desktop/CIMWin32Prov/power-management-event-provider)e o [Provedor Win32](/windows/desktop/CIMWin32Prov/win32-provider) definem seus próprios eventos. Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

## <a name="example"></a>Exemplo

O exemplo de código de script a seguir é uma consulta para o [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrínseco da classe de evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Você pode executar esse programa em segundo plano e, quando houver um evento, será exibida uma mensagem. Se você fechar a caixa de diálogo **aguardando eventos** , o programa parará de aguardar eventos. Lembre-se de que **SeSecurityPrivilege** deve estar habilitado.


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





O exemplo de código VBScript a seguir mostra o evento extrínsecos [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) que o provedor do registro define. O script cria um consumidor temporário usando a chamada para [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)e recebe apenas eventos quando o script está em execução. O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido. Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo. Para interrompê-lo programaticamente, use o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe de processo do Win32 \_ . Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).


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



## <a name="event-consumers"></a>Consumidores de evento

Você pode monitorar ou consumir eventos usando os seguintes consumidores enquanto um script ou aplicativo está em execução:

-   Consumidores de eventos temporários

    Um [*consumidor temporário*](gloss-t.md) é um aplicativo cliente WMI que recebe um evento WMI. O WMI inclui uma interface exclusiva que usa o para especificar os eventos que o WMI deve enviar a um aplicativo cliente. Um consumidor de evento temporário é considerado temporário porque só funciona quando é especificamente carregado por um usuário. Para obter mais informações, consulte [recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md).

-   Consumidores de eventos permanentes

    Um [*consumidor permanente*](gloss-p.md) é um objeto com que pode receber um evento WMI em todos os momentos. Um consumidor de evento permanente usa um conjunto de objetos persistentes e filtros para capturar um evento WMI. Como um consumidor de evento temporário, você configura uma série de objetos e filtros do WMI que capturam um evento WMI. Quando ocorre um evento que corresponde a um filtro, o WMI carrega o consumidor de evento permanente e o notifica sobre o evento. Como um consumidor permanente é implementado no repositório do WMI e é um arquivo executável registrado no WMI, o consumidor de evento permanente Opera e recebe eventos depois que ele é criado e, mesmo após uma reinicialização do sistema operacional, desde que o WMI esteja em execução. Para obter mais informações, consulte [recebendo eventos em todos os momentos](receiving-events-at-all-times.md).

Scripts ou aplicativos que recebem eventos têm considerações de segurança especiais. Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).

Um aplicativo ou script pode usar um provedor de eventos interno do WMI que fornece [classes de consumidor padrão](standard-consumer-classes.md). Cada classe de consumidor padrão responde a um evento com uma ação diferente, enviando uma mensagem de email ou executando um script. Você não precisa escrever o código do provedor para usar uma classe de consumidor padrão para criar um consumidor de evento permanente. Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="providing-events"></a>Fornecendo eventos

Um provedor de eventos é um componente COM que envia um evento para o WMI. Você pode criar um provedor de eventos para enviar um evento em um aplicativo C++ ou C#. A maioria dos provedores de eventos gerencia um objeto para o WMI, por exemplo, um aplicativo ou item de hardware. Para obter mais informações, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md).

Um evento cronometrado ou repetitivo é um evento que ocorre em um momento predeterminado.

O WMI fornece as seguintes maneiras de criar eventos cronometrados ou repetidos para seus aplicativos:

-   A infra-estrutura de eventos padrão da Microsoft.
-   Uma classe de temporizador especializada.

Para obter mais informações, consulte [recebendo um evento cronometrado ou repetido](receiving-a-timed-or-repeating-event.md). Ao escrever um provedor de eventos, considere as informações de segurança identificadas no [fornecimento de eventos com segurança](providing-events-securely.md).

É recomendável que as assinaturas de evento permanentes sejam compiladas \\ no \\ namespace da assinatura raiz. Para obter mais informações, consulte [implementando assinaturas de eventos permanentes de namespace cruzado](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Cotas de assinatura

A sondagem de eventos pode prejudicar o desempenho de provedores que dão suporte a consultas em grandes conjuntos de dados. Além disso, qualquer usuário que tenha acesso de leitura a um namespace com provedores dinâmicos pode executar um ataque de negação de serviço (DoS). O WMI mantém cotas para todos os usuários combinados e para cada consumidor de evento na única instância do [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) localizado no \\ namespace raiz. Essas cotas são globais em vez de para cada namespace. Você não pode alterar as cotas.

Atualmente, o WMI impõe cotas usando as propriedades de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). Cada cota tem um por usuário e uma versão total que inclui todos os usuários combinados, não por namespace. A tabela a seguir lista as cotas que se aplicam às propriedades **\_ \_ ArbitratorConfiguration** .



| Total/Peruser                                                                   | Quota                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10.000<br/> 1,000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10.000<br/> 1,000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10.000<br/> 1,000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10 milhões (0x989680) bytes<br/> 5 milhões (0x4CB40) bytes<br/> |



 

Um administrador ou um usuário com permissão de **\_ gravação completa** no namespace pode modificar a instância singleton de [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). O WMI rastreia a cota por usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

