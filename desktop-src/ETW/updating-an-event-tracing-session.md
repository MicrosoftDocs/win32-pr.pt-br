---
description: Para atualizar as propriedades de uma sessão de rastreamento de eventos, chame a função ControlTrace usando o código de controle EVENT \_ TRACE \_ CONTROL \_ UPDATE.
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Atualizando uma sessão de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa4f092211d59dda080906f01380f8751fbc099f79dc8f1cd8ea1f7a2ba36fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383336"
---
# <a name="updating-an-event-tracing-session"></a>Atualizando uma sessão de rastreamento de eventos

Para atualizar as propriedades de uma sessão de rastreamento de eventos, chame a [**função ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) usando o **código de controle EVENT TRACE CONTROL \_ \_ \_ UPDATE.** Você pode especificar a sessão a ser atualizada usando um handle de sessão obtido de uma chamada anterior para [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)ou um nome de sessão. As propriedades da sessão de rastreamento de eventos são atualizadas usando os valores especificados na estrutura [**EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Você pode atualizar apenas um subconjunto das propriedades. Para ver uma lista das propriedades que você pode atualizar, consulte o *parâmetro Properties* da **função ControlTrace.**

Se a [**chamada controlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) for bem-sucedida, a estrutura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) será atualizada para refletir os novos valores de propriedade. A estrutura também conterá as novas estatísticas de executar para a sessão de rastreamento de eventos.

O exemplo a seguir mostra como atualizar a sessão de rastreamento de eventos do kernel. O exemplo consulta os valores da propriedade atual e atualiza a estrutura antes de atualizar a sessão.


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
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

[Configurando e iniciando a sessão do NT Kernel Logger](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
