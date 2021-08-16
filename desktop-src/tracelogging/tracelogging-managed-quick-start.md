---
title: TraceLogging Managed Início Rápido
description: A seção a seguir descreve as etapas básicas necessárias para adicionar TraceLogging ao código gerenciado.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be29e4a1bd6721b8f53dbe2394be3552ca4845143cf948f130ef55e11881b518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589236"
---
# <a name="tracelogging-managed-quick-start"></a>TraceLogging Managed Início Rápido

A seção a seguir descreve as etapas básicas necessárias para adicionar TraceLogging ao código gerenciado.

## <a name="prerequisites"></a>Pré-requisitos

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample.cs

Este exemplo demonstra como registrar eventos tracelogging sem a necessidade de criar manualmente um arquivo XML de manifesto de instrumentação separado.


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a>Criar o EventSource

Antes de registrar eventos em log, você deve criar uma instância da classe EventSource. O primeiro parâmetro do construtor identifica o nome desse provedor. O provedor é registrado automaticamente para você, conforme ilustrado no exemplo.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



A instância é estática porque deve haver apenas uma instância de um provedor específico em seu aplicativo por vez.

### <a name="log-tracelogging-events"></a>Eventos de Log Tracelogging

Depois que o provedor é criado, o código a seguir do exemplo acima registra um evento simples.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Registrar dados de carga de evento estruturados

Você pode definir dados de carga estruturados que são registrados com o evento . Forneça dados de carga estruturados como um tipo anônimo ou como uma instância de uma classe que foi anotada com o atributo , conforme `[EventData]` mostrado no exemplo a seguir.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



Você deve adicionar o `[EventData]` atributo às classes de carga de evento que você define, conforme mostrado abaixo.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



O atributo substitui a necessidade de criar manualmente um arquivo de manifesto para descrever os dados do evento. Agora tudo o que você precisa fazer é passar uma instância da classe para o método EventSource.Write() para registrar o evento e os dados de carga correspondentes.

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

Consulte Registrar e exibir eventos [traceLogging](tracelogging-record-and-display-tracelogging-events.md) para obter informações sobre como capturar e exibir dados TraceLogging usando as versões internas mais recentes do WPT (Ferramentas de Desempenho Windows).

Consulte [Exemplos de rastreamento do .NET](tracelogging-net-examples.md) para obter exemplos de TraceLogging mais gerenciados.

 

 




