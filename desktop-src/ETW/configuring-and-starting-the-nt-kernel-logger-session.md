---
description: A sessão do NT Kernel Logger é uma sessão de rastreamento de eventos que registra um conjunto predefinido de eventos de kernel.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Configurando e iniciando a sessão do NT Kernel Logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41398c9caac3ecd090af68a18bfb148095632d96b8c75eaaee7f04a551360fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901216"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Configurando e iniciando a sessão do NT Kernel Logger

A sessão do NT Kernel Logger é uma sessão de rastreamento de eventos que registra um conjunto predefinido de eventos de kernel. Você não chama a [**função EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar os provedores de kernel. Em vez disso, você usa **o membro EnableFlags** da estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) para especificar os eventos de kernel que você deseja receber. A [**função StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) usa os sinalizadores de habilitar que você especifica para habilitar os provedores de kernel.

Há apenas uma sessão do NT Kernel Logger. Se a sessão já estiver em uso, a [**função StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) retornará ERROR \_ ALREADY \_ EXISTS.

Para obter detalhes sobre como iniciar uma sessão de rastreamento de eventos, consulte [Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obter detalhes sobre como iniciar uma sessão de logger privado, consulte [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do Global Logger, consulte [Configurando e iniciando a sessão do global logger](configuring-and-starting-the-global-logger-session.md).

Para obter detalhes sobre como iniciar uma sessão do AutoLogger, consulte Configurando e [iniciando uma sessão do AutoLogger.](configuring-and-starting-an-autologger-session.md)

O exemplo a seguir mostra como configurar e iniciar uma sessão do NT Kernel Logger que coleta eventos de kernel TCP/IP de rede e os grava em um arquivo circular de 5 MB.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando e iniciando uma sessão de logger privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão systemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão do AutoLogger](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurando e iniciando uma sessão de rastreamento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Atualizando uma sessão de rastreamento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
