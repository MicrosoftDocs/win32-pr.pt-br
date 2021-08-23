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
ms.openlocfilehash: b0b7e7b1d1e79e64fb1eb83f17f3aa2d118a9eb53b23c19cbdfd624e2c501a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992776"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Monitorando e respondendo a eventos com consumidores padrão

Você pode usar as [classes de consumidor padrão](standard-consumer-classes.md) instaladas para executar ações com base em eventos em um sistema operacional. Os consumidores padrão são classes simples que já estão registradas e definem classes de consumo permanentes. Cada consumidor padrão executa uma ação específica depois de receber uma notificação de eventos. Por exemplo, você pode definir uma instância de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para executar um script quando o espaço livre em disco em um computador for diferente de um tamanho especificado.

O WMI compila os consumidores padrão em namespaces padrão que dependem do sistema operacional, por exemplo:

-   no Windows Server 2003, todos os consumidores padrão são compilados por padrão no \\ namespace "assinatura raiz".

> [!Note]  
> Para os namespaces e sistemas operacionais padrão específicos para cada classe WMI, consulte as seções comentários e requisitos de cada tópico de classe.

 

A tabela a seguir lista e descreve os consumidores padrão do WMI.



| Consumidor padrão                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | Executa um script quando recebe uma notificação de evento. Para obter mais informações, consulte [executando um script com base em um evento](running-a-script-based-on-an-event.md).                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | Grava cadeias de caracteres personalizadas em um arquivo de log de texto quando recebe uma notificação de eventos. Para obter mais informações, consulte [gravando em um arquivo de log com base em um evento](writing-to-a-log-file-based-on-an-event.md).                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | Registra uma mensagem específica no log de eventos do aplicativo. Para obter mais informações, consulte [registrando em log o log de eventos NT com base em um evento](logging-to-nt-event-log-based-on-an-event.md).                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | Envia uma mensagem de email usando SMTP cada vez que um evento é entregue a ele. Para obter mais informações, consulte [enviando email com base em um evento](sending-e-mail-based-on-an-event.md).                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | Inicia um processo quando um evento é entregue a um sistema local. O arquivo executável deve estar em um local seguro ou protegido com uma ACL (lista de controle de acesso) forte para impedir que um usuário não autorizado substitua seu executável por um executável diferente. Para obter mais informações, consulte [executando um programa da linha de comando com base em um evento](running-a-program-from-the-command-line-based-on-an-event.md). |



 

O procedimento a seguir descreve como monitorar e responder a eventos usando um consumidor padrão. Observe que o procedimento é o mesmo para um arquivo, script ou aplicativo formato MOF (MOF).

**Para monitorar e responder a eventos com um consumidor padrão**

1.  Especifique o namespace em um arquivo MOF usando o [ \# namespace de pragma](pragma-namespace.md)do comando de pré-processador MOF. Em um script ou aplicativo, especifique o namespace no código que se conecta ao WMI.

    O exemplo de código MOF a seguir mostra como especificar o \\ namespace de assinatura raiz.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    A maioria dos [*eventos intrínsecos*](gloss-i.md) está associada às alterações em instâncias de classe no \\ namespace raiz cimv2. No entanto, eventos de registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) são acionados no \\ namespace raiz padrão pelo [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

    Um consumidor pode incluir classes de evento localizadas em outros namespaces, especificando o namespace na propriedade **EventNamespace** na consulta [**\_ \_ EventFilter**](--eventfilter.md) para eventos. As classes de [*eventos intrínsecos*](gloss-i.md) , como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , estão disponíveis em todos os namespaces.

2.  Crie e popule uma instância de uma classe de consumidor padrão.

    Essa instância pode ter um valor exclusivo na propriedade **Name** . Você pode atualizar um consumidor existente reutilizando o mesmo nome.

    **InsertionStringTemplates** contém o texto a ser inserido em um evento que você especifica no **EventType**. Você pode usar cadeias de caracteres literais ou fazer referência diretamente a uma propriedade. Para obter mais informações, consulte [usando modelos de cadeia de caracteres padrão](using-standard-string-templates.md) e [instrução SELECT para consultas de evento](select-statement-for-event-queries.md).

    Use uma fonte existente para o log de eventos que ofereça suporte a uma cadeia de caracteres de inserção sem texto associado.

    O exemplo de código MOF a seguir mostra como usar uma fonte existente do WSH e um valor de **EventID** de 8.

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

3.  Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e defina uma consulta para eventos.

    No exemplo a seguir, o filtro monitora a chave do registro onde os programas de inicialização são registrados. O monitoramento dessa chave do registro pode ser importante porque um programa não autorizado pode se registrar na chave, o que faz com que ela seja iniciada quando o computador é inicializado.

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

4.  Identifique um evento para monitorar e criar uma consulta de evento.

    Você pode verificar se há um evento intrínseco ou extrínsecos que usa. Por exemplo, use a classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) do provedor de registro para monitorar alterações no registro do sistema.

    Se não existir uma classe que descreva um evento que você precisa monitorar, você deverá criar seu próprio provedor de eventos e definir novas classes de evento extrínsecos. Para obter mais informações, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md).

    Em um arquivo MOF, você pode definir um [*alias*](gloss-a.md) para o filtro e o consumidor, que fornece uma maneira fácil de descrever os caminhos de instância.

    O exemplo a seguir mostra como definir um [*alias*](gloss-a.md) para o filtro e o consumidor.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar as classes de filtro e de consumidor. Essa instância determina que quando ocorrer um evento que corresponda ao filtro especificado, a ação especificada pelo consumidor deverá ocorrer. [**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e **\_ \_ FilterToConsumerBinding** devem ter o mesmo SID (identificador de segurança individual) na propriedade **CreatorSID** . Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

    O exemplo a seguir mostra como identificar uma instância pelo caminho do objeto ou usar um alias como uma expressão abreviada para o caminho do objeto.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    O exemplo a seguir associa o filtro ao consumidor usando aliases.

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    Você pode associar um filtro a vários consumidores, o que indica que quando ocorrem eventos correspondentes, várias ações devem ser executadas; ou você pode associar um consumidor a vários filtros, o que indica que a ação deve ser executada quando os eventos que correspondem a um dos filtros ocorrerem.

    As seguintes ações são executadas com base na condição de consumidores e eventos:

    -   Se um dos consumidores permanentes falhar, outros consumidores que solicitarem a notificação de recebimento de eventos.
    -   Se um evento for descartado, o WMI será acionado [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).
    -   Se você assinar esse evento, ele retornará o evento que será descartado e uma referência ao [**\_ \_ EventConsumer**](--eventconsumer.md) representará o consumidor com falha.
    -   Se um consumidor falhar, o WMI aciona [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), que pode conter mais informações nas propriedades **ErrorCode**, **ErrorDescription** e **ErrorObject** .

    Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

## <a name="example"></a>Exemplo

O exemplo a seguir mostra o MOF para uma instância de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). depois de compilar esse MOF, qualquer tentativa de criar, excluir ou modificar um valor no caminho do registro **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ execute** registra uma entrada no log de eventos do aplicativo, sob a origem "WSH".


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recebendo eventos com segurança](receiving-events-securely.md)
</dt> </dl>

 

 
