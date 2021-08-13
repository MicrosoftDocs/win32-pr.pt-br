---
description: Saiba mais sobre como escrever eventos MOF em uma sessão de rastreamento. Comece registrando seu provedor para que ele esteja pronto para gravar eventos em uma sessão de rastreamento.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Escrevendo eventos MOF (clássico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c29b5d753c40bb2fca5313340638a63d2a5e55c5eaf6dcef14e8388906cb190a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393655"
---
# <a name="writing-mof-classic-events"></a>Escrevendo eventos MOF (clássico)

Antes de gravar eventos em uma sessão de rastreamento, você deve registrar seu provedor. Registrar um provedor informa ao ETW que seu provedor está pronto para gravar eventos em uma sessão de rastreamento. Um processo pode registrar até 1.024 GUIDs de provedor; No entanto, você deve limitar o número de provedores que seu processo registra a um ou dois.

**Antes do Windows Vista:** Não há nenhum limite para o número de provedores que um processo pode registrar.

Para registrar um provedor clássico, chame a [**função RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) A função registra o GUID do provedor, GUIDs da classe de rastreamento de eventos e identifica o retorno de chamada que o ETW chama quando um controlador habilita ou desabilita o provedor.

Se o provedor chamar a [**função TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos, você não precisará incluir a matriz de GUIDs de classe (pode ser **NULL**) ao chamar a [**função RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) Você só precisará incluir a matriz se o provedor chamar a [**função TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para registrar eventos.

**Windows XP e Windows 2000:** Você sempre precisa incluir a matriz de GUIDs de classe (não pode ser **NULL).**

Depois que um provedor se registra e é habilitado pelo controlador, o provedor pode registrar eventos na sessão de rastreamento do controlador.

Antes de o provedor sair, chame a [**função UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) para remover o registro do provedor do ETW. A [**função RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) retorna o alça de registro que você passa para a **função UnregisterTraceGuids.**

Se o provedor registrar eventos somente na sessão do Global Logger, você não precisa registrar seu provedor com o ETW porque o controlador do Global Logger não habilita nem desabilita provedores. Para obter detalhes, [consulte Configurando e iniciando a sessão do global logger](configuring-and-starting-the-global-logger-session.md).

Todos [os provedores](about-event-tracing.md) clássicos (exceto aqueles que rastreiam eventos para a sessão do Global Logger) devem implementar a [**função ControlCallback.**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) O provedor usa as informações no retorno de chamada para determinar se ele está habilitado ou desabilitado e quais eventos ele deve gravar.

O provedor especifica o nome da função de retorno de chamada quando chama a [**função RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para se registrar. ETW chama a função de retorno de chamada quando o controlador chama [**a função EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar ou desabilitar o provedor.

Na implementação [**de ControlCallback,**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) você deve chamar a [**função GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) para recuperar o handle de sessão; você usa o alça de sessão ao chamar a [**função TraceEvent.**](/windows/win32/api/evntrace/nf-evntrace-traceevent) Você só precisará chamar a [**função GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) ou a função [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) na implementação **de ControlCallback** se o provedor usar o nível de habilitar ou habilitar sinalizadores.

Um provedor pode registrar eventos de rastreamento em apenas uma sessão, mas não há nada para impedir que vários controladores habilitam um único provedor. Para impedir que outro controlador redirecione seus eventos de rastreamento para sua sessão, talvez você queira adicionar lógica à implementação [**de ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) para comparar os alças de sessão e ignorar as solicitações de habilitar de outros controladores.

Para registrar eventos, [os provedores](about-event-tracing.md) clássicos chamam a [**função TraceEvent.**](/windows/win32/api/evntrace/nf-evntrace-traceevent) Um evento consiste na estrutura [**EVENT \_ TRACE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e todos os dados específicos do evento que são anexados ao header.

O header deve conter as seguintes informações:

-   O **membro** Size deve conter o número total de bytes a serem registrados para o evento (incluindo o tamanho da estrutura [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e de quaisquer dados específicos de evento que são anexados ao header).
-   O **membro** Guid deve conter o GUID da classe do evento (ou o membro **GuidPtr** deve conter um ponteiro para o GUID da classe).

    **Windows XP e Windows 2000:** O GUID de classe deve ter sido registrado anteriormente usando [**a função RegisterTraceGuids.**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

-   O **membro Flags** deve conter o sinalizador GUID **\_ \_ TRACED \_ do SINALIZADOR WNODE.** Se você especificar o GUID da classe usando **o membro GuidPtr,** adicione também o sinalizador USE GUID **\_ \_ \_ \_ PTR** do SINALIZADOR WNODE.
-   O **membro Class.Type** deverá conter o tipo de evento se você usar o MOF para publicar o layout dos dados do evento.
-   O **membro Class.Version** deverá conter a versão do evento se você usar o MOF para publicar o layout dos dados do evento. A versão é usada para distinguir entre revisões para os dados do evento. De definir o número de versão inicial como 0.

Se você escrever o provedor e o consumidor, poderá usar uma estrutura para preencher os dados específicos do evento que são anexados ao header. No entanto, se você usar o MOF para publicar os dados específicos do evento para que qualquer consumidor possa processar o evento, não deverá usar uma estrutura para anexar os dados específicos do evento ao header. Isso ocorre porque o compilador pode adicionar bytes extras aos dados específicos do evento para fins de alinhamento de bytes. Como a definição de MOF não conta para os bytes extras, o consumidor pode recuperar dados que não são válidos.

Você deve alocar um bloco de memória para o evento e copiar cada item de dados de evento para a memória ou criar uma estrutura que inclua uma matriz de estruturas [**FIELD MOF; \_**](/windows/win32/api/evntrace/ns-evntrace-mof_field) a maioria dos aplicativos criará uma estrutura que inclui uma matriz de estruturas **MOF \_ FIELD.** Certifique-se de **que Header.Size** reflita o número real de estruturas **MOF \_ FIELD** que são realmente definidas antes de registrar o evento. Por exemplo, se o evento contiver três campos de dados, deverão ser definidos **Header.Size** como sizeof(EVENT \_ TRACE \_ HEADER) + (sizeof(MOF \_ FIELD) \* 3).

Para obter informações sobre como rastrear eventos relacionados, consulte [Escrevendo eventos relacionados em um cenário de ponta a ponta.](writing-related-events-in-an-end-to-end-scenario.md)

O exemplo a seguir mostra como chamar a [**função TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos. O exemplo faz referência aos eventos definidos [em Publicando seu esquema de evento para um provedor clássico.](publishing-your-event-schema-for-a-classic-provider.md)


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



 

 
