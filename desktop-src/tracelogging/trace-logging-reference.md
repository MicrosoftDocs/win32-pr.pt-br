---
title: Referência de TraceLogging
description: Os tópicos a seguir fornecem informações sobre a API nativa do TraceLogging. O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366636"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="f3809-103">Referência de TraceLogging</span><span class="sxs-lookup"><span data-stu-id="f3809-103">TraceLogging Reference</span></span>

<span data-ttu-id="f3809-104">Os tópicos a seguir fornecem informações sobre a API nativa do TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="f3809-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="f3809-105">O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.</span><span class="sxs-lookup"><span data-stu-id="f3809-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="f3809-106">O TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.</span><span class="sxs-lookup"><span data-stu-id="f3809-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="f3809-107"><span class="underline">Para desenvolvedores do WinRT</span></span><span class="sxs-lookup"><span data-stu-id="f3809-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="f3809-108">O [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) foi estendido no Windows 10 para registrar eventos de ETW (rastreamento de eventos do Windows) autodescritivos sem a necessidade de um manifesto.</span><span class="sxs-lookup"><span data-stu-id="f3809-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="f3809-109">O [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) foi estendido no Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos de iniciar e parar.</span><span class="sxs-lookup"><span data-stu-id="f3809-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="f3809-110">Além disso, as atividades podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="f3809-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="f3809-111"><span class="underline">Para desenvolvedores de código gerenciado (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="f3809-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="f3809-112">A classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornecida com versões anteriores do .NET Framework já oferece suporte à gravação de eventos ETW sem a necessidade de um manifesto.</span><span class="sxs-lookup"><span data-stu-id="f3809-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="f3809-113">No entanto, os desenvolvedores eram obrigados a usar EventSource como uma classe base e adicionar atributos e métodos à classe derivada que foram transformados em um manifesto ETW automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f3809-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="f3809-114">Agora, os desenvolvedores não precisam derivar de EventSource e, em vez disso, podem usar a EventSource diretamente para registrar eventos autodescritivos que não exigem um manifesto.</span><span class="sxs-lookup"><span data-stu-id="f3809-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="f3809-115"><span class="underline">Para desenvolvedores de C/C++</span></span><span class="sxs-lookup"><span data-stu-id="f3809-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="f3809-116">TraceLoggingProvider. h é a API recomendada para desenvolvedores de C/C++ no modo de usuário ou kernel.</span><span class="sxs-lookup"><span data-stu-id="f3809-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="f3809-117">Essa API não é adequada para uso em cenários dinâmicos (com script), como JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f3809-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="f3809-118">Os links a seguir descrevem a API C/C++.</span><span class="sxs-lookup"><span data-stu-id="f3809-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="f3809-119">Classes</span><span class="sxs-lookup"><span data-stu-id="f3809-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="f3809-120">Funções</span><span class="sxs-lookup"><span data-stu-id="f3809-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="f3809-121">Macros</span><span class="sxs-lookup"><span data-stu-id="f3809-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="f3809-122">Observe que o valor de WINVER afetará a maneira como o TraceLoggingProvider. h se comporta.</span><span class="sxs-lookup"><span data-stu-id="f3809-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="f3809-123">Se WINVER não estiver definido antes de incluir <Windows. h>, <Windows. h> definirá WINVER como um valor padrão correspondente à versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="f3809-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="f3809-124">Usando TraceLoggingProvider. h com WINVER definido como 0x0602 (Windows 8) ou superior, o programa não será executado no Windows Vista ou no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f3809-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="f3809-125">Usando TraceLoggingProvider. h com WINVER definido como 0x0600 (Windows Vista) ou 0x0601 (Windows 7), o programa será configurado para compatibilidade e funcionará nas versões especificadas do Windows.</span><span class="sxs-lookup"><span data-stu-id="f3809-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 