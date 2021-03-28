---
description: Esta documentação é para aplicativos de modo de usuário que desejam usar o ETW. Para obter informações sobre como instrumentar drivers de dispositivo executados no modo kernel, consulte rastreamento de software do WPP e adicionando o rastreamento de eventos a drivers de Kernel-Mode no WDK (Kit de driver do Windows).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297514"
---
# <a name="event-tracing"></a><span data-ttu-id="9f017-104">Rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9f017-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="9f017-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="9f017-105">Purpose</span></span>

<span data-ttu-id="9f017-106">O ETW (rastreamento de eventos para Windows) fornece aos programadores de aplicativos a capacidade de iniciar e parar sessões de rastreamento de eventos, instrumentar um aplicativo para fornecer eventos de rastreamento e consumir eventos de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="9f017-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="9f017-107">Os eventos de rastreamento contêm um cabeçalho de evento e dados definidos pelo provedor que descrevem o estado atual de um aplicativo ou operação.</span><span class="sxs-lookup"><span data-stu-id="9f017-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="9f017-108">Você pode usar os eventos para depurar um aplicativo e executar a análise de capacidade e desempenho.</span><span class="sxs-lookup"><span data-stu-id="9f017-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="9f017-109">Esta documentação é para aplicativos de modo de usuário que desejam usar o ETW.</span><span class="sxs-lookup"><span data-stu-id="9f017-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="9f017-110">Para obter informações sobre como instrumentar drivers de dispositivo executados no modo kernel, consulte [rastreamento de software do WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) e adicionando o [rastreamento de eventos a drivers de Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="9f017-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9f017-111">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="9f017-111">Where applicable</span></span>

<span data-ttu-id="9f017-112">Use o ETW quando desejar instrumentar seu aplicativo, registrar eventos de usuário ou kernel em um arquivo de log e consumir eventos de um arquivo de log ou em tempo real.</span><span class="sxs-lookup"><span data-stu-id="9f017-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9f017-113">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="9f017-113">Developer audience</span></span>

<span data-ttu-id="9f017-114">O ETW foi projetado para desenvolvedores de C e C++ que escrevem aplicativos de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="9f017-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9f017-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="9f017-115">Run-time requirements</span></span>

<span data-ttu-id="9f017-116">O ETW está incluído no Microsoft Windows 2000 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9f017-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="9f017-117">Para obter informações sobre quais sistemas operacionais são necessários para usar uma função específica, consulte a seção requisitos da documentação da função.</span><span class="sxs-lookup"><span data-stu-id="9f017-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="9f017-118">Processar rastreamentos ETW no código .NET</span><span class="sxs-lookup"><span data-stu-id="9f017-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="9f017-119">Você pode usar a [API do .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analisar rastreamentos ETW para seus aplicativos e outros componentes de software.</span><span class="sxs-lookup"><span data-stu-id="9f017-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="9f017-120">Essa API é usada internamente na Microsoft para analisar dados de ETW produzidos pelo sistema de engenharia do Windows e também é usada para alimentar várias tabelas no [analisador de desempenho do Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="9f017-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="9f017-121">Essa API está disponível como um pacote NuGet.</span><span class="sxs-lookup"><span data-stu-id="9f017-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="9f017-122">Para obter mais informações, consulte [este artigo](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="9f017-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9f017-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9f017-123">In this section</span></span>



| <span data-ttu-id="9f017-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="9f017-124">Topic</span></span>                                                                     | <span data-ttu-id="9f017-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f017-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f017-126">O que há de novo no rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9f017-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="9f017-127">Novos recursos que foram adicionados ao rastreamento de eventos em cada versão.</span><span class="sxs-lookup"><span data-stu-id="9f017-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="9f017-128">Sobre o rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9f017-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="9f017-129">Informações gerais sobre o rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="9f017-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="9f017-130">Usando o rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9f017-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="9f017-131">Tópicos relacionados a tarefas que descrevem como usar a API do ETW.</span><span class="sxs-lookup"><span data-stu-id="9f017-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="9f017-132">Referência de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9f017-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="9f017-133">Descrições detalhadas de funções de ETW e outros elementos de programação.</span><span class="sxs-lookup"><span data-stu-id="9f017-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
