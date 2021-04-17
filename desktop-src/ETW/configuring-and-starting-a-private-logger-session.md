---
description: Uma sessão de rastreamento de eventos particulares é uma sessão de rastreamento de eventos no modo de usuário que é executada no mesmo processo que seus provedores de rastreamento de eventos&\# 8212; a sessão privada e os provedores que ela habilita devem estar no mesmo processo.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Configurando e iniciando uma sessão de agente de log particular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461199"
---
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="e3a73-103">Configurando e iniciando uma sessão de agente de log particular</span><span class="sxs-lookup"><span data-stu-id="e3a73-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="e3a73-104">Uma sessão de rastreamento de eventos particulares é uma sessão de rastreamento de eventos no modo de usuário que é executada no mesmo processo que seus provedores de rastreamento de eventos – a sessão privada e os provedores que ela habilita devem estar no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="e3a73-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="e3a73-105">O benefício de usar uma sessão privada é que a sessão privada não conta com o máximo de 64 sessões de rastreamento de eventos em execução simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="e3a73-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="e3a73-106">Configurar e iniciar uma sessão privada é semelhante a iniciar uma sessão normal de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="e3a73-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="e3a73-107">A diferença é que o membro **Wnode. GUID** da estrutura de [**\_ \_ Propriedades do rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) deve conter o **GUID** do provedor, e não a sessão, e o provedor já deve ter registrado o GUID.</span><span class="sxs-lookup"><span data-stu-id="e3a73-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="e3a73-108">Observe que, se você também definir o \_ rastreamento de eventos \_ privado \_ no \_ modo de log de proc, poderá usar um **GUID** diferente para a sessão e o provedor.</span><span class="sxs-lookup"><span data-stu-id="e3a73-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="e3a73-109">Para obter detalhes sobre como iniciar uma sessão normal de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="e3a73-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="e3a73-110">Observe que você não pode iniciar, parar ou liberar uma sessão de rastreamento particular de DllMain; Você deve fazer isso nas rotinas de inicialização e finalização da DLL.</span><span class="sxs-lookup"><span data-stu-id="e3a73-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="e3a73-111">De Windows 8.1 para o Windows 10, a versão 1607, a carga do evento, o escopo e os filtros de exame de pilha podem ser usados pela função [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e pelas estruturas [**habilitar \_ \_ parâmetros de rastreamento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descritor de filtro de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar as condições específicas em uma sessão de agente.</span><span class="sxs-lookup"><span data-stu-id="e3a73-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="e3a73-112">Para obter mais informações sobre filtros de carga de evento, consulte as funções [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e as estruturas [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **Enable \_ trace \_**, **\_ \_ descritor de filtro de evento** e conteúdo de filtro de carga.</span><span class="sxs-lookup"><span data-stu-id="e3a73-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="e3a73-113">A partir do Windows 10, versão 1703, os usuários com privilégios baixos agora podem iniciar uma sessão de agente de log particular em processos iniciados.</span><span class="sxs-lookup"><span data-stu-id="e3a73-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="e3a73-114">O provedor não precisa mais ser registrado antes de habilitar ou iniciar a sessão privada, o que significa que o provedor é "habilitado previamente", semelhante a como os provedores de sessão não privados são.</span><span class="sxs-lookup"><span data-stu-id="e3a73-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="e3a73-115">Há um limite de oito agentes particulares do sistema em um processo individual.</span><span class="sxs-lookup"><span data-stu-id="e3a73-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="e3a73-116">Para aumentar o desempenho em cenários de processo cruzado, é recomendável usar a filtragem para APIs de sessão (incluindo [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)e [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) ao iniciar um agente de log particular do sistema.</span><span class="sxs-lookup"><span data-stu-id="e3a73-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="e3a73-117">Observe que os mesmos filtros devem ser passados para todas as APIs de sessão.</span><span class="sxs-lookup"><span data-stu-id="e3a73-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="e3a73-118">Para obter mais informações sobre filtros, [**consulte \_ Propriedades de rastreamento de eventos \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span><span class="sxs-lookup"><span data-stu-id="e3a73-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="e3a73-119">Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="e3a73-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="e3a73-120">Para obter detalhes sobre como iniciar uma sessão do agente do NT kernel, consulte [Configurando e iniciando a sessão do agente de log do NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="e3a73-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="e3a73-121">Para obter detalhes sobre como iniciar uma sessão de agente global, consulte [Configurando e iniciando uma sessão global de agente](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="e3a73-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="e3a73-122">Para obter detalhes sobre como iniciar uma sessão do agente de log autologger, consulte [Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="e3a73-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3a73-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3a73-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a73-124">Configurando e iniciando uma sessão SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="e3a73-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="e3a73-125">Configurando e iniciando uma sessão do agente de log</span><span class="sxs-lookup"><span data-stu-id="e3a73-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="e3a73-126">Configurando e iniciando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="e3a73-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="e3a73-127">Configurando e iniciando a sessão do NT kernel logger</span><span class="sxs-lookup"><span data-stu-id="e3a73-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="e3a73-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="e3a73-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="e3a73-129">**Habilitar \_ parâmetros de rastreamento \_**</span><span class="sxs-lookup"><span data-stu-id="e3a73-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="e3a73-130">**\_Propriedades de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="e3a73-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="e3a73-131">**Propriedades de rastreamento de eventos \_ \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="e3a73-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="e3a73-132">**\_descritor de filtro de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="e3a73-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="e3a73-133">**predicado de filtro de carga \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3a73-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="e3a73-134">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="e3a73-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="e3a73-135">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="e3a73-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="e3a73-136">Atualizando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="e3a73-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
