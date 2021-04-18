---
description: Antes de poder gravar eventos em uma sessão de rastreamento, você deve registrar seu provedor.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Gravando eventos MOF (clássicos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3d041e2792540d4a05637bcffdb67e1164a95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968239"
---
# <a name="writing-mof-classic-events"></a>Gravando eventos MOF (clássicos)

Antes de poder gravar eventos em uma sessão de rastreamento, você deve registrar seu provedor. O registro de um provedor informa ao ETW que seu provedor está pronto para gravar eventos em uma sessão de rastreamento. Um processo pode registrar até 1.024 GUIDs do provedor; no entanto, você deve limitar o número de provedores que seu processo registra em um ou dois.

**Antes do Windows Vista:** Não há nenhum limite para o número de provedores que um processo pode registrar.

Para registrar um provedor clássico, chame a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . A função registra o GUID do provedor, os GUIDs de classe de rastreamento de eventos e identifica o retorno de chamada que o ETW chama quando um controlador habilita ou desabilita o provedor.

Se o provedor chamar a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos, você não precisará incluir a matriz de GUIDs de classe (pode ser **NULL**) ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . Você só precisa incluir a matriz se o provedor chamar a função [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para registrar eventos.

**Windows XP e windows 2000:** Você sempre precisa incluir a matriz de GUIDs de classe (não pode ser **NULL**).

Depois que um provedor se registra e é habilitado pelo controlador, o provedor pode registrar eventos na sessão de rastreamento do controlador.

Antes de o provedor sair, chame a função [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) para remover o registro do provedor do ETW. A função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) retorna o identificador de registro que você passa para a função **UnregisterTraceGuids** .

Se seu provedor registrar eventos na sessão global do agente somente, você não precisará registrar seu provedor com o ETW porque o controlador do agente de log global não habilita nem desabilita provedores. Para obter detalhes, consulte [Configurando e iniciando a sessão global de agente](configuring-and-starting-the-global-logger-session.md).

Todos os provedores [clássicos](about-event-tracing.md) (exceto aqueles que rastreiam eventos para a sessão de agente global) devem implementar a função [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) . O provedor usa as informações no retorno de chamada para determinar se ele está habilitado ou desabilitado e quais eventos devem ser gravados.

O provedor especifica o nome da função de retorno de chamada ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para se registrar. O ETW chama a função de retorno de chamada quando o controlador chama a função [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar ou desabilitar o provedor.

Na implementação do [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) , você deve chamar a função [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) para recuperar o identificador de sessão; Você usa o identificador de sessão ao chamar a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) . Você só precisa chamar a função [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) ou a função [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) na sua implementação **ControlCallback** se o seu provedor usar o nível de habilitação ou habilitar sinalizadores.

Um provedor pode registrar eventos de rastreamento em apenas uma sessão, mas não há nada para impedir que vários controladores habilitem um único provedor. Para impedir que outro controlador redirecione seus eventos de rastreamento para sua sessão, talvez você queira adicionar lógica à sua implementação do [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) para comparar identificadores de sessão e ignorar as solicitações de habilitação de outros controladores.

Para registrar eventos, os provedores [clássicos](about-event-tracing.md) chamam a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) . Um evento consiste na estrutura [**de \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e em todos os dados específicos de evento que são anexados ao cabeçalho.

O cabeçalho deve conter as seguintes informações:

-   O membro de **tamanho** deve conter o número total de bytes a serem registrados para o evento (incluindo o tamanho da estrutura de [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e de quaisquer dados específicos de evento que são anexados ao cabeçalho).
-   O membro **GUID** deve conter o GUID de classe do evento (ou o membro **GuidPtr** deve conter um ponteiro para o GUID de classe).

    **Windows XP e windows 2000:** O GUID de classe deve ter sido registrado anteriormente usando a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .

-   O membro **flags** deve conter o **sinalizador \_ \_ \_ GUID rastreado do sinalizador WNODE** . Se você especificar o GUID de classe usando o membro **GuidPtr** , adicione também o sinalizador **WNODE de uso do \_ sinalizador \_ \_ \_ PTR GUID** .
-   O membro **Class. Type** deve conter o tipo de evento, se você usar o MOF para publicar o layout dos dados do evento.
-   O membro **Class. Version** deve conter a versão do evento, se você usar o MOF para publicar o layout dos dados do evento. A versão é usada para distinguir entre revisões para os dados de evento. Defina o número de versão inicial como 0.

Se você escrever o provedor e o consumidor, poderá usar uma estrutura para preencher os dados específicos do evento que são anexados ao cabeçalho. No entanto, se você usar o MOF para publicar os dados específicos do evento para que qualquer consumidor possa processar o evento, você não deverá usar uma estrutura para acrescentar os dados específicos do evento ao cabeçalho. Isso ocorre porque o compilador pode adicionar bytes extras aos dados específicos do evento para fins de alinhamento de byte. Como a definição de MOF não conta com os bytes extras, o consumidor pode recuperar dados que não são válidos.

Você deve alocar um bloco de memória para o evento e copiar cada item de dados de evento para a memória ou criar uma estrutura que inclua uma matriz de estruturas de [**\_ campo MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) ; a maioria dos aplicativos criará uma estrutura que inclui uma matriz de estruturas de **\_ campo MOF** . Certifique-se de que **header. Size** reflita o número real de estruturas de **\_ campo MOF** definidas na verdade antes de registrar o evento. Por exemplo, se o evento contiver três campos de dados, defina **header. Size** para sizeof (cabeçalho de rastreamento de eventos \_ \_ ) + (sizeof ( \_ campo MOF) \* 3).

Para obter informações sobre rastreamento de eventos relacionados, consulte [escrevendo eventos relacionados em um cenário de ponta a ponta](writing-related-events-in-an-end-to-end-scenario.md).

O exemplo a seguir mostra como chamar a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos. O exemplo faz referência aos eventos definidos na [publicação do esquema de evento para um provedor clássico](publishing-your-event-schema-for-a-classic-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 
