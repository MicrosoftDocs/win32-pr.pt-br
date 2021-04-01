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
# <a name="monitoring-events"></a>Monitorando eventos

Os administradores do sistema podem usar o WMI para monitorar eventos em uma rede. Por exemplo:

-   Um serviço é interrompido inesperadamente.
-   Um servidor fica indisponível.
-   Uma unidade de disco preenche a capacidade de 80%.
-   Os eventos de segurança são relatados para um log de eventos do NT.

O WMI dá suporte à detecção e entrega de eventos para consumidores de eventos porque alguns provedores WMI são provedores de eventos. Para obter mais informações, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).

Os [*consumidores de eventos*](gloss-e.md) são aplicativos ou scripts que solicitam notificação de eventos e executam tarefas quando eventos específicos ocorrem. Você pode criar scripts de monitoramento de eventos ou aplicativos que monitoram temporariamente quando ocorrem eventos. O WMI também fornece um conjunto de provedores de eventos permanentes pré-instalados e as classes de consumo permanentes que permitem que você monitore eventos permanentemente. Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

As seções a seguir são discutidas neste tópico:

-   [Usando consumidores de eventos temporários](#using-temporary-event-consumers)
-   [Usando consumidores de eventos permanentes](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Usando consumidores de eventos temporários

Os consumidores de eventos temporários são scripts ou aplicativos que retornam os eventos que correspondem a uma consulta de evento ou filtro. As consultas de evento temporárias geralmente usam [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) em aplicativos C++ ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) em scripts e Visual Basic.

Uma consulta de evento solicita instâncias de uma classe de evento que especifica um determinado tipo de evento, como [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

O exemplo de código VBScript a seguir solicita notificação quando uma instância do [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) é criada. Uma instância dessa classe é gerada quando um processo é iniciado ou interrompido.

Para executar o script, copie-o para um arquivo chamado event.vbs e use a seguinte linha de comando: **cscript event.vbs**. Você pode ver a saída do script iniciando Notepad.exe ou qualquer outro processo. O script é interrompido após cinco processos serem iniciados ou interrompidos.

Esse script chama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), que é a versão [*semisynchronous*](gloss-s.md) do método. Consulte o próximo script para obter um exemplo de como configurar uma assinatura de evento temporário assíncrono chamando [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obter mais informações, consulte [chamando um método](calling-a-method.md). O script chama [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para obter e processar cada evento conforme ele chega. Salve o script em um arquivo com uma extensão. vbs e execute o script em uma linha de comando usando CScript: **cscript file.vbs**.


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



Os consumidores de eventos temporários devem ser iniciados manualmente e não devem persistir nas reinicializações do WMI ou nas reinicializações do sistema operacional. Um consumidor de evento temporário pode processar eventos somente enquanto está em execução.

O procedimento a seguir descreve como criar um consumidor de evento temporário.

**Para criar um consumidor de evento temporário**

1.  Decida qual linguagem de programação usar.

    A linguagem de programação determina a API a ser usada.

    -   Para a linguagem de programação C++, use a [API com para o WMI](com-api-for-wmi.md).
    -   Para Visual Basic ou linguagens de script, use a [API de script para o WMI](scripting-api-for-wmi.md).

2.  Comece a codificar um aplicativo de consumidor de evento temporário da mesma maneira que você inicia um aplicativo WMI.

    As primeiras etapas de codificação dependem da linguagem de programação. Normalmente, você faz logon no WMI e define as configurações de segurança. Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).

3.  Defina a consulta de evento que você deseja usar.

    Para obter alguns tipos de dados de desempenho, talvez seja necessário usar classes fornecidas por provedores de alto desempenho. Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md), [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)e [consultando com WQL](querying-with-wql.md).

4.  Decida fazer uma chamada assíncrona ou uma chamada semisynchronous e escolher o método de API.

    As chamadas assíncronas permitem evitar a sobrecarga de sondagem de dados. No entanto, as chamadas semisynchronous fornecem um desempenho semelhante com maior segurança. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

5.  Faça a chamada do método assíncrona ou semisynchronous e inclua uma consulta de evento como o parâmetro *strQuery* .

    Para aplicativos C++, chame os seguintes métodos:

    -   [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Para scripts, chame os seguintes métodos:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Escreva o código para processar o objeto de evento retornado.

    Para consultas de evento assíncrono, coloque o código nos vários métodos ou eventos do coletor de objeto. Para consultas de eventos semisynchronous, cada objeto é retornado à medida que o WMI o Obtém, portanto, o código deve estar no loop que manipula cada objeto.

O exemplo de código de script a seguir é uma versão assíncrona do script [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) . Como as operações assíncronas retornam imediatamente, uma caixa de diálogo mantém o script ativo enquanto está aguardando eventos.

Em vez de chamar [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para receber cada evento, o script tem um manipulador de eventos para o evento [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) .


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
> Um retorno de chamada assíncrono, como um retorno de chamada manipulado pela `SINK_OnObjectReady` sub-rotina, permite que um usuário não autenticado forneça dados para o coletor. Para maior segurança, use a comunicação semisynchronous ou a comunicação síncrona. Para mais informações, consulte os seguintes tópicos:
>
> -   [Fazendo uma chamada Semisynchronous com C++](making-a-semisynchronous-call-with-c--.md)
> -   [Fazendo uma chamada Semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Fazendo uma chamada assíncrona com C++](making-an-asynchronous-call-with-c--.md)
> -   [Fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)
> -   [Protegendo clientes de script](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Usando consumidores de eventos permanentes

Um consumidor de evento permanente é executado até que seu registro seja explicitamente cancelado e, em seguida, iniciado quando o WMI ou o sistema for reiniciado.

Um consumidor de evento permanente é uma combinação de classes, filtros e objetos COM do WMI em um sistema.

A lista a seguir identifica as partes necessárias para criar um consumidor de evento permanente:

-   Um objeto COM que contém o código que implementa o consumidor permanente.
-   Uma nova classe de consumidor permanente.
-   Uma instância da classe de consumidor permanente.
-   Um filtro que contém a consulta de eventos.
-   Um link entre o consumidor e o filtro.

Para obter mais informações, consulte [recebendo eventos em todos os momentos](--filtertoconsumerbinding.md).

O WMI fornece vários consumidores permanentes. As classes de consumidor e o objeto COM que contém o código são pré-instalados. Por exemplo, você pode criar e configurar uma instância da classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para executar um script quando ocorrer um evento. Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md). Para obter um exemplo de como usar **ActiveScriptEventConsumer**, consulte [executando um script com base em um evento](running-a-script-based-on-an-event.md).

O procedimento a seguir descreve como criar um consumidor de evento permanente.

**Para criar um consumidor de evento permanente**

1.  [Registre o provedor de eventos](registering-a-provider.md) com o namespace que você está usando.

    Alguns provedores de eventos só podem usar um namespace específico. Por exemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) é um evento intrínseco que é suportado pelo [provedor do Win32](/windows/desktop/CIMWin32Prov/win32-provider) e é registrado por padrão com o \\ \\ namespace raiz cimv2.

    > [!Note]  
    > Você pode usar a propriedade **EventNamespace** do [**\_ \_ EventFilter**](--eventfilter.md) usado no registro para criar uma assinatura de namespace cruzado. Para obter mais informações, consulte [implementando assinaturas de eventos permanentes de namespace cruzado](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registre o provedor de consumidor de eventos](registering-an-event-consumer-provider.md) com o namespace em que as classes de evento estão localizadas.

    O WMI usa um provedor de consumidor de eventos para encontrar um consumidor de eventos que seja permanente. O consumidor de evento permanente é o aplicativo que o WMI inicia quando um evento é recebido. Para registrar o consumidor de eventos, os provedores criam instâncias de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Crie uma instância da classe que representa o consumidor de evento permanente que você deseja usar.

    As classes de consumidor de eventos são derivadas da classe [**\_ \_ EventConsumer**](--eventconsumer.md). Defina as propriedades que a instância de consumidor de evento requer.

4.  Registre o consumidor com o com usando o utilitário **regsvr32** .
5.  Crie uma instância da classe de filtro de eventos [**\_ \_ EventFilter**](--eventfilter.md).

    Defina os campos obrigatórios para a instância de filtro de eventos. Os campos obrigatórios para [**\_ \_ EventFilter**](--eventfilter.md) são **Name**, **QueryLanguage** e **Query**. A propriedade **Name** pode ser qualquer nome exclusivo para uma instância dessa classe. A propriedade **QueryLanguage** é sempre definida como "WQL". A propriedade de **consulta** é uma cadeia de caracteres que contém uma consulta de evento. Um evento é gerado quando uma consulta do consumidor de evento permanente falha. A origem do evento é WinMgmt, a ID do evento é 10 e o tipo de evento é Error.

6.  Crie uma instância da classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar um consumidor de evento lógico a um filtro de eventos.

    O WMI usa uma associação para localizar o consumidor de eventos associado ao evento que corresponde aos critérios especificados no filtro de eventos. O WMI usa o provedor de consumidor de eventos para encontrar o aplicativo de consumidor de evento permanente a ser iniciado.

 

 
