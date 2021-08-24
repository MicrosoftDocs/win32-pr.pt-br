---
description: A classe LogFileEventConsumer pode gravar texto predefinido em um arquivo de log quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Escrevendo em um arquivo de log com base em um evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 881435986a1097c2ba97160693ed15e28bae3d86019fb703adf6bf1e8b07f8a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049724"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Escrevendo em um arquivo de log com base em um evento

A [**classe LogFileEventConsumer**](logfileeventconsumer.md) pode gravar texto predefinido em um arquivo de log quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.

O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em Monitoramento e resposta a [eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md)

O procedimento a seguir adiciona ao procedimento básico, é específico à classe [**LogFileEventConsumer**](logfileeventconsumer.md) e descreve como criar um consumidor de eventos que executa um programa.

**Para criar um consumidor de eventos que grava em um arquivo de log**

1.  No arquivo Managed Object Format (MOF), crie uma instância de [**LogFileEventConsumer**](logfileeventconsumer.md) para receber os eventos solicitados na consulta, nomeie a instância na propriedade **Name** e coloque o caminho para o arquivo de log na propriedade **Filename.**

    Para obter mais informações, [consulte Designando classes Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

2.  Forneça o modelo de texto a ser escrito no arquivo de log na propriedade Texto.

    Para obter mais informações, consulte [Usando modelos de cadeia de caracteres padrão](using-standard-string-templates.md).

3.  Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e defina uma consulta para especificar os eventos que ativarão o consumidor.

    Para obter mais informações, [consulte Consultando com WQL](querying-with-wql.md).

4.  Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**LogFileEventConsumer**](logfileeventconsumer.md).
5.  Para controlar quem lê ou grava no arquivo de log, de definir a segurança no diretório em que o log está localizado para o nível necessário.
6.  Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Exemplo

O exemplo nesta seção está no código MOF, mas você pode criar as instâncias programaticamente usando a API de Script para [WMI](scripting-api-for-wmi.md) ou a [API COM para WMI](com-api-for-wmi.md). O exemplo usa o LogFileEventConsumer padrão para criar uma classe de consumidor chamada LogFileEvent que grava uma linha no arquivo c: Logfile.log quando uma instância da classe \\ LogFileEvent é criada.

O procedimento a seguir descreve como usar o exemplo.

**Para usar o exemplo**

1.  Copie a listagem MOF abaixo em um arquivo de texto e salve-a com uma extensão .mof.
2.  Em uma janela de comando, compile o arquivo MOF usando o comando a seguir.

    Nome do arquivo *Mofcomp***.mof* *

3.  Abra Logfile.log para ver a linha especificada por LogFileEvent.Name: "Evento do Consumidor de Eventos do Logfile".

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



