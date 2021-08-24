---
description: a classe NTEventLogEventConsumer grava uma mensagem no log de eventos Windows quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
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
ms.openlocfilehash: c8c070b1a52fe41f32b8610ff0931d33be7feb33f9f5cd6f6067652e963f6824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050704"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Registrando no log de eventos NT com base em um evento

a classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) grava uma mensagem no log de eventos Windows quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.

> [!Note]  
> Os usuários autenticados não podem, por padrão, registrar eventos no log do aplicativo em um computador remoto. Como resultado, o exemplo descrito neste tópico falhará se você usar a propriedade **UNCServerName** da classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) e especificar um computador remoto como seu valor. Para saber como alterar a segurança do log de eventos, consulte este [artigo da base de conhecimento](https://support.microsoft.com/kb/323076).

 

O procedimento básico para usar um consumidor padrão é descrito em [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md). Veja a seguir etapas adicionais além do procedimento básico, necessárias ao usar a classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) . As etapas descrevem como criar um consumidor de eventos que grava no log de eventos do aplicativo.

O procedimento a seguir descreve como criar um consumidor de eventos que grava no log de eventos do NT.

**para criar um consumidor de eventos que grava no Log de eventos do Windows**

1.  Em um arquivo formato MOF (MOF), crie uma instância de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) para receber os eventos solicitados na consulta. Para obter mais informações sobre como escrever código MOF, consulte [criando Classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md).
2.  Criar e nomear uma instância de [**\_ \_ EventFilter**](--eventfilter.md)e, em seguida, criar uma consulta para especificar o tipo de evento que dispara a gravação no log de eventos do NT.

    Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).

3.  Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).
4.  Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Exemplo

O exemplo nesta seção está no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md). O exemplo mostra como criar um consumidor para gravar no log de eventos do aplicativo usando [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). O MOF cria uma nova classe chamada "NTLogCons \_ example", um filtro de eventos para consultar operações, como a criação, em uma instância dessa nova classe e uma associação entre o filtro e o consumidor. Como a última ação no MOF é criar uma instância do \_ exemplo NTLogCons, você pode ver imediatamente o evento no log de eventos do aplicativo executando Eventvwr.exe.

O `EventID=0x0A for SourceName="WinMgmt"` identifica uma mensagem com o texto a seguir. "%1", "%2", "%3" são espaços reservados para cadeias de caracteres correspondentes especificadas na matriz InsertionStringTemplates.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

O procedimento a seguir descreve como usar o exemplo.

**Para usar o exemplo**

1.  Copie a listagem MOF abaixo em um arquivo de texto e salve-a com uma extensão. mof.
2.  Em um janela Comando, compile o arquivo MOF usando o seguinte comando:

     *Nome do arquivo Mofcomp * * *. mof**

3.  Execute Eventvwr.exe. Examine o log de eventos do aplicativo. Você deverá ver um evento com ID = 10 ( **EventID**), Source = "WMI" e Type = erro.
4.  Clique duas vezes na mensagem **tipo de informação** do WMI com 10 na coluna **evento** . A descrição a seguir será exibida para o evento.

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



