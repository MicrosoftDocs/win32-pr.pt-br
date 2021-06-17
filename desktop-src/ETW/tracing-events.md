---
description: Saiba como gravar eventos MOF em uma sessão de rastreamento. Comece com o registro de seu provedor, para que ele esteja pronto para gravar eventos em uma sessão de rastreamento.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Gravando eventos MOF (clássicos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d081c48567851d2fb570dd7bfa5c75e687b524
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261838"
---
# <a name="writing-mof-classic-events"></a><span data-ttu-id="8c323-104">Gravando eventos MOF (clássicos)</span><span class="sxs-lookup"><span data-stu-id="8c323-104">Writing MOF (Classic) Events</span></span>

<span data-ttu-id="8c323-105">Antes de poder gravar eventos em uma sessão de rastreamento, você deve registrar seu provedor.</span><span class="sxs-lookup"><span data-stu-id="8c323-105">Before you can write events to a trace session, you must register your provider.</span></span> <span data-ttu-id="8c323-106">O registro de um provedor informa ao ETW que seu provedor está pronto para gravar eventos em uma sessão de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="8c323-106">Registering a provider tells ETW that your provider is ready to write events to a trace session.</span></span> <span data-ttu-id="8c323-107">Um processo pode registrar até 1.024 GUIDs do provedor; no entanto, você deve limitar o número de provedores que seu processo registra em um ou dois.</span><span class="sxs-lookup"><span data-stu-id="8c323-107">A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two.</span></span>

<span data-ttu-id="8c323-108">**Antes do Windows Vista:** Não há nenhum limite para o número de provedores que um processo pode registrar.</span><span class="sxs-lookup"><span data-stu-id="8c323-108">**Prior to Windows Vista:** There is no limit to the number of providers that a process can register.</span></span>

<span data-ttu-id="8c323-109">Para registrar um provedor clássico, chame a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="8c323-109">To register a classic provider, call the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="8c323-110">A função registra o GUID do provedor, os GUIDs de classe de rastreamento de eventos e identifica o retorno de chamada que o ETW chama quando um controlador habilita ou desabilita o provedor.</span><span class="sxs-lookup"><span data-stu-id="8c323-110">The function registers the provider's GUID, event trace class GUIDs, and identifies the callback that ETW calls when a controller enables or disables the provider.</span></span>

<span data-ttu-id="8c323-111">Se o provedor chamar a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos, você não precisará incluir a matriz de GUIDs de classe (pode ser **NULL**) ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="8c323-111">If the provider calls the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events, you do not need to include the array of class GUIDs (can be **NULL**) when calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="8c323-112">Você só precisa incluir a matriz se o provedor chamar a função [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="8c323-112">You only need to include the array if the provider calls the [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) function to log events.</span></span>

<span data-ttu-id="8c323-113">**Windows XP e windows 2000:** Você sempre precisa incluir a matriz de GUIDs de classe (não pode ser **NULL**).</span><span class="sxs-lookup"><span data-stu-id="8c323-113">**Windows XP and Windows 2000:** You always need to include the array of class GUIDs (cannot be **NULL**).</span></span>

<span data-ttu-id="8c323-114">Depois que um provedor se registra e é habilitado pelo controlador, o provedor pode registrar eventos na sessão de rastreamento do controlador.</span><span class="sxs-lookup"><span data-stu-id="8c323-114">After a provider registers itself and is enabled by the controller, the provider can log events to the controller's trace session.</span></span>

<span data-ttu-id="8c323-115">Antes de o provedor sair, chame a função [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) para remover o registro do provedor do ETW.</span><span class="sxs-lookup"><span data-stu-id="8c323-115">Before the provider exits, call the [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) function to remove the provider's registration from ETW.</span></span> <span data-ttu-id="8c323-116">A função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) retorna o identificador de registro que você passa para a função **UnregisterTraceGuids** .</span><span class="sxs-lookup"><span data-stu-id="8c323-116">The [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function returns the registration handle that you pass to the **UnregisterTraceGuids** function.</span></span>

<span data-ttu-id="8c323-117">Se seu provedor registrar eventos na sessão global do agente somente, você não precisará registrar seu provedor com o ETW porque o controlador do agente de log global não habilita nem desabilita provedores.</span><span class="sxs-lookup"><span data-stu-id="8c323-117">If your provider logs events to the Global Logger session only, you do not have to register your provider with ETW because the Global Logger controller does not enable or disable providers.</span></span> <span data-ttu-id="8c323-118">Para obter detalhes, consulte [Configurando e iniciando a sessão global de agente](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="8c323-118">For details, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="8c323-119">Todos os provedores [clássicos](about-event-tracing.md) (exceto aqueles que rastreiam eventos para a sessão de agente global) devem implementar a função [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) .</span><span class="sxs-lookup"><span data-stu-id="8c323-119">All [classic](about-event-tracing.md) providers (except those that trace events to the Global Logger session) must implement the [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) function.</span></span> <span data-ttu-id="8c323-120">O provedor usa as informações no retorno de chamada para determinar se ele está habilitado ou desabilitado e quais eventos devem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="8c323-120">The provider uses the information in the callback to determine if it is enabled or disabled and which events it should write.</span></span>

<span data-ttu-id="8c323-121">O provedor especifica o nome da função de retorno de chamada ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para se registrar.</span><span class="sxs-lookup"><span data-stu-id="8c323-121">The provider specifies the name of the callback function when it calls the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register itself.</span></span> <span data-ttu-id="8c323-122">O ETW chama a função de retorno de chamada quando o controlador chama a função [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar ou desabilitar o provedor.</span><span class="sxs-lookup"><span data-stu-id="8c323-122">ETW calls the callback function when the controller calls the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable or disable the provider.</span></span>

<span data-ttu-id="8c323-123">Na implementação do [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) , você deve chamar a função [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) para recuperar o identificador de sessão; Você usa o identificador de sessão ao chamar a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="8c323-123">In your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation, you must call the [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) function to retrieve the session handle; you use the session handle when calling the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="8c323-124">Você só precisa chamar a função [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) ou a função [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) na sua implementação **ControlCallback** se o seu provedor usar o nível de habilitação ou habilitar sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="8c323-124">You only need to call the [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) function or the [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) function in your **ControlCallback** implementation if your provider uses the enable level or enable flags.</span></span>

<span data-ttu-id="8c323-125">Um provedor pode registrar eventos de rastreamento em apenas uma sessão, mas não há nada para impedir que vários controladores habilitem um único provedor.</span><span class="sxs-lookup"><span data-stu-id="8c323-125">A provider can log trace events to only one session, but there is nothing to prevent multiple controllers from enabling a single provider.</span></span> <span data-ttu-id="8c323-126">Para impedir que outro controlador redirecione seus eventos de rastreamento para sua sessão, talvez você queira adicionar lógica à sua implementação do [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) para comparar identificadores de sessão e ignorar as solicitações de habilitação de outros controladores.</span><span class="sxs-lookup"><span data-stu-id="8c323-126">To prevent another controller from redirecting your trace events to its session, you may want to add logic to your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation to compare session handles and ignore enable requests from other controllers.</span></span>

<span data-ttu-id="8c323-127">Para registrar eventos, os provedores [clássicos](about-event-tracing.md) chamam a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="8c323-127">To log events, [classic](about-event-tracing.md) providers call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="8c323-128">Um evento consiste na estrutura [**de \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e em todos os dados específicos de evento que são anexados ao cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8c323-128">An event consists of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and any event-specific data that is appended to the header.</span></span>

<span data-ttu-id="8c323-129">O cabeçalho deve conter as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="8c323-129">The header must contain the following information:</span></span>

-   <span data-ttu-id="8c323-130">O membro de **tamanho** deve conter o número total de bytes a serem registrados para o evento (incluindo o tamanho da estrutura de [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) e de quaisquer dados específicos de evento que são anexados ao cabeçalho).</span><span class="sxs-lookup"><span data-stu-id="8c323-130">The **Size** member must contain the total number of bytes to be recorded for the event (including the size of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and of any event-specific data that is appended to the header).</span></span>
-   <span data-ttu-id="8c323-131">O membro **GUID** deve conter o GUID de classe do evento (ou o membro **GuidPtr** deve conter um ponteiro para o GUID de classe).</span><span class="sxs-lookup"><span data-stu-id="8c323-131">The **Guid** member must contain the class GUID of the event (or the **GuidPtr** member must contain a pointer to the class GUID).</span></span>

    <span data-ttu-id="8c323-132">**Windows XP e windows 2000:** O GUID de classe deve ter sido registrado anteriormente usando a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="8c323-132">**Windows XP and Windows 2000:** The class GUID must have been registered previously using the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span>

-   <span data-ttu-id="8c323-133">O membro **flags** deve conter o **sinalizador \_ \_ \_ GUID rastreado do sinalizador WNODE** .</span><span class="sxs-lookup"><span data-stu-id="8c323-133">The **Flags** member must contain the **WNODE\_FLAG\_TRACED\_GUID** flag.</span></span> <span data-ttu-id="8c323-134">Se você especificar o GUID de classe usando o membro **GuidPtr** , adicione também o sinalizador **WNODE de uso do \_ sinalizador \_ \_ \_ PTR GUID** .</span><span class="sxs-lookup"><span data-stu-id="8c323-134">If you specify the class GUID using the **GuidPtr** member, also add the **WNODE\_FLAG\_USE\_GUID\_PTR** flag.</span></span>
-   <span data-ttu-id="8c323-135">O membro **Class. Type** deve conter o tipo de evento, se você usar o MOF para publicar o layout dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="8c323-135">The **Class.Type** member must contain the event type, if you use MOF to publish the layout of your event data.</span></span>
-   <span data-ttu-id="8c323-136">O membro **Class. Version** deve conter a versão do evento, se você usar o MOF para publicar o layout dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="8c323-136">The **Class.Version** member must contain the event version, if you use MOF to publish the layout of your event data.</span></span> <span data-ttu-id="8c323-137">A versão é usada para distinguir entre revisões para os dados de evento.</span><span class="sxs-lookup"><span data-stu-id="8c323-137">The version is used to distinguish between revisions to the event data.</span></span> <span data-ttu-id="8c323-138">Defina o número de versão inicial como 0.</span><span class="sxs-lookup"><span data-stu-id="8c323-138">Set the initial version number to 0.</span></span>

<span data-ttu-id="8c323-139">Se você escrever o provedor e o consumidor, poderá usar uma estrutura para preencher os dados específicos do evento que são anexados ao cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8c323-139">If you write both the provider and the consumer, you can use a structure to populate the event-specific data that is appended to the header.</span></span> <span data-ttu-id="8c323-140">No entanto, se você usar o MOF para publicar os dados específicos do evento para que qualquer consumidor possa processar o evento, você não deverá usar uma estrutura para acrescentar os dados específicos do evento ao cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8c323-140">However, if you use MOF to publish the event-specific data so that any consumer can process the event, you should not use a structure to append the event-specific data to the header.</span></span> <span data-ttu-id="8c323-141">Isso ocorre porque o compilador pode adicionar bytes extras aos dados específicos do evento para fins de alinhamento de byte.</span><span class="sxs-lookup"><span data-stu-id="8c323-141">This is because the compiler may add extra bytes to the event-specific data for byte alignment purposes.</span></span> <span data-ttu-id="8c323-142">Como a definição de MOF não conta com os bytes extras, o consumidor pode recuperar dados que não são válidos.</span><span class="sxs-lookup"><span data-stu-id="8c323-142">Because the MOF definition does not account for the extra bytes, the consumer may retrieve data that is not valid.</span></span>

<span data-ttu-id="8c323-143">Você deve alocar um bloco de memória para o evento e copiar cada item de dados de evento para a memória ou criar uma estrutura que inclua uma matriz de estruturas de [**\_ campo MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) ; a maioria dos aplicativos criará uma estrutura que inclui uma matriz de estruturas de **\_ campo MOF** .</span><span class="sxs-lookup"><span data-stu-id="8c323-143">You should either allocate a block of memory for the event and copy each event data item to the memory, or create a structure that includes an array of [**MOF\_FIELD**](/windows/win32/api/evntrace/ns-evntrace-mof_field) structures; most applications will create a structure that includes an array of **MOF\_FIELD** structures.</span></span> <span data-ttu-id="8c323-144">Certifique-se de que **header. Size** reflita o número real de estruturas de **\_ campo MOF** definidas na verdade antes de registrar o evento.</span><span class="sxs-lookup"><span data-stu-id="8c323-144">Make sure that **Header.Size** reflects the actual number of **MOF\_FIELD** structures that are actually set before logging the event.</span></span> <span data-ttu-id="8c323-145">Por exemplo, se o evento contiver três campos de dados, defina **header. Size** para sizeof (cabeçalho de rastreamento de eventos \_ \_ ) + (sizeof ( \_ campo MOF) \* 3).</span><span class="sxs-lookup"><span data-stu-id="8c323-145">For example, if the event contains three data fields, set **Header.Size** to sizeof(EVENT\_TRACE\_HEADER) + (sizeof(MOF\_FIELD) \* 3).</span></span>

<span data-ttu-id="8c323-146">Para obter informações sobre rastreamento de eventos relacionados, consulte [escrevendo eventos relacionados em um cenário de ponta a ponta](writing-related-events-in-an-end-to-end-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="8c323-146">For information on tracing related events, see [Writing Related Events in an End-to-End Scenario](writing-related-events-in-an-end-to-end-scenario.md).</span></span>

<span data-ttu-id="8c323-147">O exemplo a seguir mostra como chamar a função [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="8c323-147">The following example shows how to call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events.</span></span> <span data-ttu-id="8c323-148">O exemplo faz referência aos eventos definidos na [publicação do esquema de evento para um provedor clássico](publishing-your-event-schema-for-a-classic-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8c323-148">The example references the events defined in [Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).</span></span>


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



 

 
