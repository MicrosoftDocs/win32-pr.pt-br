---
description: O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurando e iniciando uma sessão systemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386736"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="9c1a8-103">Configurando e iniciando uma sessão systemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="9c1a8-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="9c1a8-104">O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="9c1a8-105">No Windows 7 e no Windows Server 2008 R2, o SystemTraceProvider só pode ser usado para a sessão do NT Kernel Logger.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="9c1a8-106">No Windows 8, no Windows Server 2012 e posterior, o SystemTraceProvider pode ser multiplexado para até 8 sessões de logger.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="9c1a8-107">Os dois primeiros slots para sessões de logger são reservados para o NT Kernel Logger e o Circular Kernel Context Logger .</span><span class="sxs-lookup"><span data-stu-id="9c1a8-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="9c1a8-108">Para obter mais informações sobre como usar a sessão do NT Kernel Logger como um provedor de rastreamento, consulte Configurando e iniciando a sessão do [NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="9c1a8-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="9c1a8-109">No Windows 10 build do SDK 20348 e posterior, o SystemTraceProvider pode ser configurado por meio de provedores de sistema separados, que podem ser controlados com [EnableTraceEx2,](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) como provedores de eventos Rastreamento de Eventos para Windows padrão.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="9c1a8-110">Para ver uma lista completa de provedores de sistema, palavras-chave e grupos herdados [correspondentes,](system-providers.md) consulte Provedores de sistema</span><span class="sxs-lookup"><span data-stu-id="9c1a8-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="9c1a8-111">Habilitar uma sessão systemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="9c1a8-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="9c1a8-112">Para habilitar o SystemTraceProvider a iniciar uma sessão diferente do NT Kernel Logger, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="9c1a8-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="9c1a8-113">**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="9c1a8-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="9c1a8-114">Para habilitar programaticamente o SystemTraceProvider para iniciar uma sessão diferente do NT Kernel Logger, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="9c1a8-115">Defina um nome de logger privado.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-115">Define a private logger name.</span></span>

    <span data-ttu-id="9c1a8-116">**\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**</span><span class="sxs-lookup"><span data-stu-id="9c1a8-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="9c1a8-117">No controlador, de definir os seguintes membros da estrutura [**EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)</span><span class="sxs-lookup"><span data-stu-id="9c1a8-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="9c1a8-118">De **definir LogFileMode** como **MODO DE \_ \_ LOGGGER DO SISTEMA \_ DE \_** RASTREAMENTO DE EVENTOS .</span><span class="sxs-lookup"><span data-stu-id="9c1a8-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="9c1a8-119">De **configurar LoggerName** como um logger privado, em vez de **KERNEL \_ LOGGER \_ NAME**.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="9c1a8-120">Certifique-se **de que o membro Wnode.Guid** da estrutura EVENT TRACE [**\_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) não está definido **como SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="9c1a8-121">Você deve atribuir um **novo GUID** a esse membro.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="9c1a8-122">No consumidor, de definido o **membro LoggerName** da estrutura [**EVENT TRACE \_ \_ LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) como esse loggger privado.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="9c1a8-123">Se você quiser que um processo não administrador ou não TCB seja capaz de iniciar uma sessão de rastreamento de criação de perfil usando o SystemTraceProvider em nome de aplicativos de terceiros, você precisará conceder o privilégio de perfil do usuário e, em seguida, adicionar esse usuário ao **GUID** de sessão (criado para a sessão do logger) e ao **GUID** do provedor de rastreamento do sistema para habilitar o provedor de rastreamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="9c1a8-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="9c1a8-124">Para obter mais informações, consulte [**a função EventAccessControl.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)</span><span class="sxs-lookup"><span data-stu-id="9c1a8-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9c1a8-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c1a8-125">Related topics</span></span>

[<span data-ttu-id="9c1a8-126">Configurando e iniciando uma sessão de logger privado</span><span class="sxs-lookup"><span data-stu-id="9c1a8-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="9c1a8-127">Configurando e iniciando uma sessão do AutoLogger</span><span class="sxs-lookup"><span data-stu-id="9c1a8-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="9c1a8-128">Configurando e iniciando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9c1a8-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="9c1a8-129">Configurando e iniciando a sessão do NT Kernel Logger</span><span class="sxs-lookup"><span data-stu-id="9c1a8-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="9c1a8-130">Provedores de sistema</span><span class="sxs-lookup"><span data-stu-id="9c1a8-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="9c1a8-131">Atualizando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="9c1a8-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
