---
description: Os administradores do sistema podem usar o WMI para monitorar eventos em uma rede.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Monitorando eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90a0a6eef87f88543e8f2414bc38bdea4f7d89c577471d79d23393f331b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317110"
---
# <a name="monitoring-events"></a>Monitorando eventos

Os administradores do sistema podem usar o WMI para monitorar eventos em uma rede. Por exemplo:

-   Um serviço é interrompido inesperadamente.
-   Um servidor fica indisponível.
-   Uma unidade de disco é preenchida com capacidade de 80%.
-   Eventos de segurança são relatados a um Log de Eventos do NT.

O WMI dá suporte à detecção e à entrega de eventos para consumidores de eventos porque alguns provedores WMI são provedores de eventos. Para obter mais informações, consulte [Recebendo um evento WMI](receiving-a-wmi-event.md).

[*Os consumidores de*](gloss-e.md) eventos são aplicativos ou scripts que solicitam notificação de eventos e, em seguida, executam tarefas quando eventos específicos ocorrem. Você pode criar scripts de monitoramento de eventos ou aplicativos que monitoram temporariamente quando ocorrem eventos. O WMI também fornece um conjunto de provedores de eventos permanentes pré-instalados e as classes de consumidor permanentes que permitem monitorar eventos permanentemente. Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md)

As seções a seguir são discutidas neste tópico:

-   [Usando consumidores de eventos temporários](#using-temporary-event-consumers)
-   [Usando consumidores de eventos permanentes](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Usando consumidores de eventos temporários

Os consumidores de eventos temporários são scripts ou aplicativos que retornam os eventos que corresponderem a uma consulta de evento ou filtro. Consultas de eventos temporários geralmente usam [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) em aplicativos C++ ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) em scripts e Visual Basic.

Uma consulta de evento solicita instâncias de uma classe de evento que especifica um determinado tipo de evento, como [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

O exemplo de código VBScript a seguir solicita notificação quando uma instância do [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) é criada. Uma instância dessa classe é gerada quando um processo é iniciado ou interrompido.

Para executar o script, copie-o para um arquivo chamado event.vbs e use a seguinte linha de comando: **cscript event.vbs**. Você pode ver a saída do script iniciando Notepad.exe ou qualquer outro processo. O script é interrompido depois que cinco processos são iniciados ou interrompidos.

Esse script chama [**SWbemServices.ExecNotificationQuery,**](swbemservices-execnotificationquery.md)que é a [*versão semisíncrona*](gloss-s.md) do método. Consulte o próximo script para ver um exemplo de configuração de uma assinatura de evento temporário assíncrona chamandoSWbemServices.Exe [**cNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obter mais informações, consulte [Chamando um método](calling-a-method.md). O script chama [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) para obter e processar cada evento conforme ele chega. Salve o script em um arquivo com uma extensão .vbs e execute o script em uma linha de comando usando CScript: **cscript file.vbs**.


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



Os consumidores de eventos temporários devem ser iniciados manualmente e não devem persistir entre reinicializações WMI ou reinicializações do sistema operacional. Um consumidor de eventos temporários só pode processar eventos enquanto ele está em execução.

O procedimento a seguir descreve como criar um consumidor de eventos temporários.

**Para criar um consumidor de eventos temporários**

1.  Decida qual linguagem de programação usar.

    A linguagem de programação determina a API a ser usada.

    -   Para a linguagem de programação C++, use a [API COM para WMI](com-api-for-wmi.md).
    -   Para Visual Basic ou linguagens de script, use a [API de Script para WMI](scripting-api-for-wmi.md).

2.  Comece a codificar um aplicativo de consumidor de eventos temporário da mesma maneira que você inicia um aplicativo WMI.

    As primeiras etapas de codificação dependem da linguagem de programação. Normalmente, você faz logoff no WMI e configura as configurações de segurança. Para obter mais informações, consulte [Criando um aplicativo WMI ou script](creating-a-wmi-application-or-script.md).

3.  Defina a consulta de evento que você deseja usar.

    Para obter alguns tipos de dados de desempenho, talvez seja necessário usar classes fornecidas por provedores de alto desempenho. Para obter mais informações, consulte Monitorando dados de [desempenho,](monitoring-performance-data.md) [Determinando](determining-the-type-of-event-to-receive.md)o tipo de evento a ser recebido e [Consultando com o WQL.](querying-with-wql.md)

4.  Decida fazer uma chamada assíncrona ou uma chamada síncrona e escolha o método de API.

    Chamadas assíncronas permitem evitar a sobrecarga de sondagem de dados. No entanto, as chamadas síncronas fornecem um desempenho semelhante com maior segurança. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

5.  Faça a chamada de método assíncrono ou semisíncrono e inclua uma consulta de evento como o *parâmetro strQuery.*

    Para aplicativos C++, chame os seguintes métodos:

    -   [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Para scripts, chame os seguintes métodos:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Escreva o código para processar o objeto de evento retornado.

    Para consultas de evento assíncronas, coloque o código nos vários métodos ou eventos do sink do objeto. Para consultas de eventos semisíncronas, cada objeto é retornado à medida que o WMI o obtém, portanto, o código deve estar no loop que trata cada objeto.

O exemplo de código de script a seguir é uma versão assíncrona do script [**Win32 \_ ProcessTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) Como as operações assíncronas retornam imediatamente, uma caixa de diálogo mantém o script ativo enquanto aguarda eventos.

Em vez de chamar [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) para receber cada evento, o script tem um manipulador de eventos para o evento [**SWbemSink OnObjectReady.**](swbemsink-onobjectready.md)


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
> Um retorno de chamada assíncrono, como um retorno de chamada tratado pela sub-rotina, permite que um usuário não autenticado forneça dados `SINK_OnObjectReady` ao sink. Para maior segurança, use comunicação síncrona ou comunicação síncrona. Para obter mais informações, consulte estes tópicos:
>
> -   [Fazendo uma chamada semisíncrona com C++](making-a-semisynchronous-call-with-c--.md)
> -   [Fazendo uma chamada semisíncrona com VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Fazendo uma chamada assíncrona com C++](making-an-asynchronous-call-with-c--.md)
> -   [Fazendo uma chamada assíncrona com VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)
> -   [Proteger clientes de script](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Usando consumidores de eventos permanentes

Um consumidor de evento permanente é executado até que seu registro seja cancelado explicitamente e, em seguida, inicia quando o WMI ou o sistema é reiniciado.

Um consumidor de eventos permanente é uma combinação de classes WMI, filtros e objetos COM em um sistema.

A lista a seguir identifica as partes necessárias para criar um consumidor de eventos permanente:

-   Um objeto COM que contém o código que implementa o consumidor permanente.
-   Uma nova classe de consumidor permanente.
-   Uma instância da classe de consumidor permanente.
-   Um filtro que contém a consulta para eventos.
-   Um link entre o consumidor e o filtro.

Para obter mais informações, consulte [Recebendo eventos em todos os momentos.](--filtertoconsumerbinding.md)

O WMI fornece vários consumidores permanentes. As classes de consumidor e o objeto COM que contém o código são pré-instalados. Por exemplo, você pode criar e configurar uma instância da [**classe ActiveScriptEventConsumer**](activescripteventconsumer.md) para executar um script quando um evento ocorre. Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md) Para ver um exemplo de **como usar o ActiveScriptEventConsumer,** consulte [Executando um script baseado em um evento](running-a-script-based-on-an-event.md).

O procedimento a seguir descreve como criar um consumidor de eventos permanente.

**Para criar um consumidor de eventos permanente**

1.  [Registre o provedor de](registering-a-provider.md) eventos com o namespace que você está usando.

    Alguns provedores de eventos só podem usar um namespace específico. Por exemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) é um evento intrínseco que tem suporte do provedor [Win32](/windows/desktop/CIMWin32Prov/win32-provider) e é registrado por padrão com o \\ \\ namespace raiz cimv2.

    > [!Note]  
    > Você pode usar a **propriedade EventNamespace** do [**\_ \_ EventFilter**](--eventfilter.md) usada no registro para criar uma assinatura entre namespaces. Para obter mais informações, [consulte Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registre o provedor de consumidor de](registering-an-event-consumer-provider.md) eventos com o namespace em que as classes de evento estão localizadas.

    O WMI usa um provedor de consumidor de eventos para encontrar um consumidor de eventos permanente. O consumidor de evento permanente é o aplicativo que o WMI inicia quando um evento é recebido. Para registrar o consumidor de eventos, os provedores criam instâncias de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Crie uma instância da classe que representa o consumidor de evento permanente que você deseja usar.

    As classes de consumidor de eventos são derivadas da [**\_ \_ classe EventConsumer**](--eventconsumer.md). De acordo com as propriedades que a instância do consumidor do evento requer.

4.  Registre o consumidor com COM usando o **utilitário regsvr32.**
5.  Crie uma instância da classe de filtro de evento [**\_ \_ EventFilter**](--eventfilter.md).

    De definir os campos necessários para a instância de filtro de evento. Os campos necessários para [**\_ \_ EventFilter**](--eventfilter.md) são **Name**, **QueryLanguage** e **Query**. A **propriedade Name** pode ser qualquer nome exclusivo para uma instância dessa classe. A **propriedade QueryLanguage** é sempre definida como "WQL". A **propriedade Consulta é** uma cadeia de caracteres que contém uma consulta de evento. Um evento é gerado quando a consulta de um consumidor de evento permanente falha. A origem do evento é WinMgmt, a ID do evento é 10 e o tipo de evento é Error.

6.  Crie uma instância da classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar um consumidor de eventos lógicos a um filtro de evento.

    O WMI usa uma associação para encontrar o consumidor de eventos associado ao evento que corresponde aos critérios especificados no filtro de evento. O WMI usa o provedor de consumidor de eventos para encontrar o aplicativo de consumidor de eventos permanente para iniciar.

 

 
