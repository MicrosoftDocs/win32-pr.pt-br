---
title: Início Rápido gerenciados TraceLogging
description: A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código gerenciado.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292083"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="b3358-103">Início Rápido gerenciados TraceLogging</span><span class="sxs-lookup"><span data-stu-id="b3358-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="b3358-104">A seção a seguir descreve as etapas básicas necessárias para adicionar o TraceLogging ao código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b3358-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b3358-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b3358-105">Prerequisites</span></span>

-   <span data-ttu-id="b3358-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3358-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="b3358-107">SimpleTraceLoggingExample. cs</span><span class="sxs-lookup"><span data-stu-id="b3358-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="b3358-108">Este exemplo demonstra como registrar em log eventos Tracelogging sem a necessidade de criar manualmente um arquivo XML de manifesto de instrumentação separado.</span><span class="sxs-lookup"><span data-stu-id="b3358-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


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



### <a name="create-the-eventsource"></a><span data-ttu-id="b3358-109">Criar a EventSource</span><span class="sxs-lookup"><span data-stu-id="b3358-109">Create the EventSource</span></span>

<span data-ttu-id="b3358-110">Antes de você poder registrar eventos, você deve criar uma instância da classe EventSource.</span><span class="sxs-lookup"><span data-stu-id="b3358-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="b3358-111">O primeiro parâmetro de construtor identifica o nome desse provedor.</span><span class="sxs-lookup"><span data-stu-id="b3358-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="b3358-112">O provedor é registrado automaticamente para você, conforme ilustrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="b3358-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="b3358-113">A instância é estática porque deve haver apenas uma instância de um provedor específico em seu aplicativo por vez.</span><span class="sxs-lookup"><span data-stu-id="b3358-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="b3358-114">Registrar eventos Tracelogging</span><span class="sxs-lookup"><span data-stu-id="b3358-114">Log Tracelogging events</span></span>

<span data-ttu-id="b3358-115">Depois que o provedor é criado, o código a seguir do exemplo acima registra um evento simples.</span><span class="sxs-lookup"><span data-stu-id="b3358-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="b3358-116">Registrar dados de conteúdo de evento estruturado</span><span class="sxs-lookup"><span data-stu-id="b3358-116">Log structured event payload data</span></span>

<span data-ttu-id="b3358-117">Você pode definir dados de carga estruturados que são registrados com o evento.</span><span class="sxs-lookup"><span data-stu-id="b3358-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="b3358-118">Forneça dados de carga estruturados como um tipo anônimo ou como uma instância de uma classe que tenha sido anotada com o `[EventData]` atributo, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="b3358-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="b3358-119">Você deve adicionar o `[EventData]` atributo às classes de carga de evento que você definir, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="b3358-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="b3358-120">O atributo substitui a necessidade de criar manualmente um arquivo de manifesto para descrever os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="b3358-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="b3358-121">Agora, tudo o que você precisa fazer é passar uma instância da classe para o método EventSource. Write () para registrar o evento e os dados de carga correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b3358-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="b3358-122">Resumo e próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b3358-122">Summary and next steps</span></span>

<span data-ttu-id="b3358-123">Consulte [gravar e exibir eventos do TraceLogging](tracelogging-record-and-display-tracelogging-events.md) para obter informações sobre como capturar e exibir dados do TraceLogging usando as versões internas mais recentes das ferramentas de desempenho do Windows (WPT).</span><span class="sxs-lookup"><span data-stu-id="b3358-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="b3358-124">Consulte [exemplos do .net Tracelogging](tracelogging-net-examples.md) para obter exemplos de Tracelogging mais gerenciados.</span><span class="sxs-lookup"><span data-stu-id="b3358-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




