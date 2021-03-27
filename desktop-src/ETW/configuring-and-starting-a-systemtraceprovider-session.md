---
description: O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurando e iniciando uma sessão SystemTraceProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967440"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="57b59-103">Configurando e iniciando uma sessão SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="57b59-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="57b59-104">O SystemTraceProvider é um provedor de kernel com conjuntos predefinidos de eventos de kernel com suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="57b59-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="57b59-105">No Windows 7 e no Windows Server 2008 R2, o SystemTraceProvider pode ser usado somente para a sessão do agente de log do NT kernel.</span><span class="sxs-lookup"><span data-stu-id="57b59-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="57b59-106">No Windows 8, no Windows Server 2012 e posterior, o SystemTraceProvider pode ser multiplexado em até 8 sessões de agente.</span><span class="sxs-lookup"><span data-stu-id="57b59-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="57b59-107">Os dois primeiros slots para sessões de agente são reservados para o agente de log do kernel NT e para o agente de contexto de kernel circular.</span><span class="sxs-lookup"><span data-stu-id="57b59-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="57b59-108">Para obter mais informações sobre como usar a sessão do agente de log do NT kernel como um provedor de rastreamento, consulte [Configurando e iniciando a sessão do NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="57b59-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="57b59-109">Para habilitar o SystemTraceProvider para iniciar uma sessão que não seja o agente de log de kernel do NT, execute o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="57b59-109">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command.</span></span>

<span data-ttu-id="57b59-110">**tracelog-iniciar MySession-f c: \\ Kernel1. etl-EFLAG proc \_ thread + Loader + CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="57b59-110">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="57b59-111">Para habilitar programaticamente o SystemTraceProvider a iniciar uma sessão diferente do agente de log de kernel do NT, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="57b59-111">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="57b59-112">Defina um nome de agente de log privado.</span><span class="sxs-lookup"><span data-stu-id="57b59-112">Define a private logger name.</span></span>

    <span data-ttu-id="57b59-113">**\#definir o \_ nome do agente de log privado \_ L "alguma sessão de rastreamento particular"**</span><span class="sxs-lookup"><span data-stu-id="57b59-113">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="57b59-114">No controlador, defina os seguintes membros da estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="57b59-114">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="57b59-115">Defina **LOGFILEMODE** para **o \_ \_ modo de \_ agente \_** de log do sistema de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="57b59-115">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="57b59-116">Defina **loggername** para o agente de log privado, em vez do **\_ \_ nome do agente de log do kernel**.</span><span class="sxs-lookup"><span data-stu-id="57b59-116">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="57b59-117">Verifique se o membro **Wnode. GUID** da estrutura [**de \_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) não está definido como **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="57b59-117">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="57b59-118">Você deve atribuir um novo **GUID** a esse membro.</span><span class="sxs-lookup"><span data-stu-id="57b59-118">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="57b59-119">No consumidor, defina o membro **loggername** da estrutura de arquivo de [**\_ \_ log de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) para esse agente particular.</span><span class="sxs-lookup"><span data-stu-id="57b59-119">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="57b59-120">Se você quiser que um processo não-administradores ou não TCB possa iniciar uma sessão de rastreamento de criação de perfil usando o SystemTraceProvider em nome de aplicativos de terceiros, será necessário conceder o privilégio de perfil de usuário e, em seguida, adicionar esse usuário ao **GUID** de sessão (criado para a sessão de agente) e ao **GUID** do provedor de rastreamento do sistema para habilitar o provedor de rastreamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="57b59-120">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="57b59-121">Para obter mais informações, consulte a função [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="57b59-121">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57b59-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57b59-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b59-123">Configurando e iniciando uma sessão de agente de log particular</span><span class="sxs-lookup"><span data-stu-id="57b59-123">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="57b59-124">Configurando e iniciando uma sessão do agente de log</span><span class="sxs-lookup"><span data-stu-id="57b59-124">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="57b59-125">Configurando e iniciando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="57b59-125">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="57b59-126">Configurando e iniciando a sessão do NT kernel logger</span><span class="sxs-lookup"><span data-stu-id="57b59-126">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="57b59-127">Atualizando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="57b59-127">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
