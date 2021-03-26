---
description: Lista os elementos usados com o rastreamento de eventos.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Referência de rastreamento de eventos
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968156"
---
# <a name="event-tracing-reference"></a><span data-ttu-id="16ea3-103">Referência de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="16ea3-103">Event Tracing Reference</span></span>

<span data-ttu-id="16ea3-104">Você usa os seguintes elementos de programação para escrever aplicativos que incorporam o rastreamento de eventos:</span><span class="sxs-lookup"><span data-stu-id="16ea3-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="16ea3-105">Enumerações de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="16ea3-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="16ea3-106">Funções de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="16ea3-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="16ea3-107">Interfaces de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="16ea3-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="16ea3-108">Estruturas de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="16ea3-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="16ea3-109">Constantes de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="16ea3-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="16ea3-110">Para obter detalhes sobre exemplos que usam esses elementos de programação, consulte [exemplos de rastreamento de eventos](event-tracing-samples.md).</span><span class="sxs-lookup"><span data-stu-id="16ea3-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="16ea3-111">Esta seção também contém informações sobre:</span><span class="sxs-lookup"><span data-stu-id="16ea3-111">This section also contains information on:</span></span>

-   <span data-ttu-id="16ea3-112">[Ferramentas](event-tracing-tools.md) fornecidas pelo ETW</span><span class="sxs-lookup"><span data-stu-id="16ea3-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="16ea3-113">[Definições de classe MOF](event-tracing-mof-classes.md) para eventos de kernel</span><span class="sxs-lookup"><span data-stu-id="16ea3-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="16ea3-114">[Qualificadores de classe MOF](event-tracing-mof-qualifiers.md) usados ao definir suas classes de evento</span><span class="sxs-lookup"><span data-stu-id="16ea3-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="16ea3-115">Processar rastreamentos ETW no código .NET</span><span class="sxs-lookup"><span data-stu-id="16ea3-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="16ea3-116">Você também pode usar a [API do .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analisar rastreamentos ETW para seus aplicativos e outros componentes de software.</span><span class="sxs-lookup"><span data-stu-id="16ea3-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="16ea3-117">Essa API é usada internamente na Microsoft para analisar dados de ETW produzidos pelo sistema de engenharia do Windows e também é usada para alimentar várias tabelas no [analisador de desempenho do Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="16ea3-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="16ea3-118">Essa API está disponível como um pacote NuGet.</span><span class="sxs-lookup"><span data-stu-id="16ea3-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="16ea3-119">Para obter mais informações, consulte [este artigo](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="16ea3-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
