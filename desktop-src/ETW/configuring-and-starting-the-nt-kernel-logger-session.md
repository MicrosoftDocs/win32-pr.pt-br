---
description: A sessão do agente do NT kernel é uma sessão de rastreamento de eventos que registra um conjunto predefinido de eventos de kernel.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Configurando e iniciando a sessão do NT kernel logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968249"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a><span data-ttu-id="2a1a5-103">Configurando e iniciando a sessão do NT kernel logger</span><span class="sxs-lookup"><span data-stu-id="2a1a5-103">Configuring and Starting the NT Kernel Logger Session</span></span>

<span data-ttu-id="2a1a5-104">A sessão do agente do NT kernel é uma sessão de rastreamento de eventos que registra um conjunto predefinido de eventos de kernel.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-104">The NT Kernel Logger session is an event tracing session that records a predefined set of kernel events.</span></span> <span data-ttu-id="2a1a5-105">Você não chama a função [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar os provedores de kernel.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-105">You do not call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable the kernel providers.</span></span> <span data-ttu-id="2a1a5-106">Em vez disso, você usa o membro **EnableFlags** da estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar os eventos de kernel que deseja receber.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-106">Instead, you use the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure to specify the kernel events that you want to receive.</span></span> <span data-ttu-id="2a1a5-107">A função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) usa os sinalizadores de habilitação que você especifica para habilitar os provedores de kernel.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-107">The [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function uses the enable flags that you specify to enable the kernel providers.</span></span>

<span data-ttu-id="2a1a5-108">Há apenas uma sessão de agente de log de kernel NT.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-108">There is only one NT Kernel Logger session.</span></span> <span data-ttu-id="2a1a5-109">Se a sessão já estiver em uso, a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) retornará um erro \_ já \_ existir.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-109">If the session is already in use, the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function returns ERROR\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="2a1a5-110">Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="2a1a5-110">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="2a1a5-111">Para obter detalhes sobre como iniciar uma sessão de agente de log particular, consulte [Configurando e iniciando uma sessão de agente de log particular](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="2a1a5-111">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="2a1a5-112">Para obter detalhes sobre como iniciar uma sessão de agente global, consulte [Configurando e iniciando a sessão global de agente](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="2a1a5-112">For details on starting a Global Logger session, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="2a1a5-113">Para obter detalhes sobre como iniciar uma sessão do agente de log autologger, consulte [Configurando e iniciando uma sessão do agente de log](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="2a1a5-113">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

<span data-ttu-id="2a1a5-114">O exemplo a seguir mostra como configurar e iniciar uma sessão do agente do NT kernel que coleta eventos de kernel TCP/IP de rede e os grava em um arquivo circular de 5 MB.</span><span class="sxs-lookup"><span data-stu-id="2a1a5-114">The following example shows how to configure and start an NT Kernel Logger session that collects network TCP/IP kernel events and writes them to a 5MB circular file.</span></span>


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
}
```



## <a name="related-topics"></a><span data-ttu-id="2a1a5-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a1a5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a1a5-116">Configurando e iniciando uma sessão de agente de log particular</span><span class="sxs-lookup"><span data-stu-id="2a1a5-116">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="2a1a5-117">Configurando e iniciando uma sessão SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="2a1a5-117">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="2a1a5-118">Configurando e iniciando uma sessão do agente de log</span><span class="sxs-lookup"><span data-stu-id="2a1a5-118">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="2a1a5-119">Configurando e iniciando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="2a1a5-119">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="2a1a5-120">Atualizando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="2a1a5-120">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
