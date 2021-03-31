---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642686"
---
# <a name="tracelogging"></a><span data-ttu-id="de596-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="de596-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="de596-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="de596-104">Purpose</span></span>

<span data-ttu-id="de596-105">TraceLogging é a nova estrutura de rastreamento de eventos do Windows 10 para aplicativos de modo de usuário e drivers de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="de596-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="de596-106">O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.</span><span class="sxs-lookup"><span data-stu-id="de596-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de596-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="de596-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de596-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="de596-108">Topic</span></span></th>
<th><span data-ttu-id="de596-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="de596-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de596-110"><a href="trace-logging-about.md">Sobre o TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="de596-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="de596-111">TraceLogging é o novo rastreamento de eventos do Windows 10 para aplicativos de modo de usuário e drivers de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="de596-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="de596-112">TraceLogging é um formato para o ETW (rastreamento de eventos autodescritivo para Windows).</span><span class="sxs-lookup"><span data-stu-id="de596-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="de596-113">O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.</span><span class="sxs-lookup"><span data-stu-id="de596-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de596-114"><a href="tracelogging-using-tracelogging.md">Usando TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="de596-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="de596-115">Os tópicos a seguir fornecem um início rápido do TraceLogging para código nativo e gerenciado, com exemplos.</span><span class="sxs-lookup"><span data-stu-id="de596-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de596-116"><a href="trace-logging-reference.md">Referência de TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="de596-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="de596-117">Os tópicos a seguir fornecem informações sobre a API nativa do TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="de596-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="de596-118">O TraceLogging se baseia no ETW (rastreamento de eventos para Windows) e fornece uma maneira simplificada de instrumentar o código.</span><span class="sxs-lookup"><span data-stu-id="de596-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="de596-119">O TraceLogging permite incluir dados estruturados com eventos, correlacionar eventos e não requer um arquivo XML de manifesto de instrumentação separado.</span><span class="sxs-lookup"><span data-stu-id="de596-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="de596-120"><span class="underline">Para desenvolvedores do WinRT</span></span><span class="sxs-lookup"><span data-stu-id="de596-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="de596-121">O <a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> foi estendido no Windows 10 para registrar eventos de ETW (rastreamento de eventos do Windows) autodescritivos sem a necessidade de um manifesto.</span><span class="sxs-lookup"><span data-stu-id="de596-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="de596-122">O <a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> foi estendido no Windows 10 para fornecer métodos de início e parada de atividade que fornecem controle sobre o formato e o conteúdo dos eventos de iniciar e parar.</span><span class="sxs-lookup"><span data-stu-id="de596-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="de596-123">Além disso, as atividades podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="de596-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="de596-124">
<span class="underline">Para desenvolvedores de código gerenciado (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="de596-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="de596-125">A classe <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> fornecida com versões anteriores do .NET Framework já oferece suporte à gravação de eventos ETW sem a necessidade de um manifesto.</span><span class="sxs-lookup"><span data-stu-id="de596-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="de596-126">No entanto, os desenvolvedores eram obrigados a usar EventSource como uma classe base e adicionar atributos e métodos à classe derivada que foram transformados em um manifesto ETW automaticamente.</span><span class="sxs-lookup"><span data-stu-id="de596-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="de596-127">Agora, os desenvolvedores não precisam derivar de EventSource e, em vez disso, podem usar a EventSource diretamente para registrar eventos autodescritivos que não exigem um manifesto.</span><span class="sxs-lookup"><span data-stu-id="de596-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="de596-128">
<span class="underline">Para desenvolvedores de C/C++</span></span><span class="sxs-lookup"><span data-stu-id="de596-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="de596-129">TraceLoggingProvider. h é a API recomendada para desenvolvedores de C/C++ no modo de usuário ou kernel.</span><span class="sxs-lookup"><span data-stu-id="de596-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="de596-130">Essa API não é adequada para uso em cenários dinâmicos (com script), como JavaScript.</span><span class="sxs-lookup"><span data-stu-id="de596-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="de596-131">Os links a seguir descrevem a API C/C++.</span><span class="sxs-lookup"><span data-stu-id="de596-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="de596-132">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="de596-132">Developer audience</span></span>

<span data-ttu-id="de596-133">O TraceLogging foi projetado para ser usado por desenvolvedores de aplicativos no modo de usuário e por desenvolvedores de driver de modo kernel que desejam adicionar rastreamento ao seu código.</span><span class="sxs-lookup"><span data-stu-id="de596-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

