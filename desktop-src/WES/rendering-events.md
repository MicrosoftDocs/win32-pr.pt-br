---
title: Renderizando eventos
description: Para exibir um evento, você deve chamar a função EvtRender para renderizá-lo em um formulário que pode ser exibido.
ms.assetid: fc763669-1fbc-4183-a4ff-577a7954d1ca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b1b4e2cbcab564abefb628f9c58f79ade86d8
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104365770"
---
# <a name="rendering-events"></a><span data-ttu-id="c0e87-103">Renderizando eventos</span><span class="sxs-lookup"><span data-stu-id="c0e87-103">Rendering Events</span></span>

<span data-ttu-id="c0e87-104">Para exibir um evento, você deve chamar a função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) para renderizá-lo em um formulário que pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c0e87-104">To display an event, you must call the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render it in a displayable form.</span></span> <span data-ttu-id="c0e87-105">Você pode renderizar o evento como uma cadeia de caracteres XML ou pode renderizar um ou mais valores do evento.</span><span class="sxs-lookup"><span data-stu-id="c0e87-105">You can render the event as an XML string or you can render one or more values from the event.</span></span> <span data-ttu-id="c0e87-106">Um evento também pode conter cadeias de mensagens (por exemplo, a cadeia de caracteres de mensagem do evento, a cadeia de caracteres de mensagem do canal ou a cadeia de caracteres de mensagem do provedor).</span><span class="sxs-lookup"><span data-stu-id="c0e87-106">An event can also contain messages strings (for example, the event's message string, the channel's message string, or the provider's message string).</span></span> <span data-ttu-id="c0e87-107">Para obter uma das cadeias de caracteres de mensagem do evento, chame a função [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) .</span><span class="sxs-lookup"><span data-stu-id="c0e87-107">To get one of the message strings from the event, call the [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) function.</span></span> <span data-ttu-id="c0e87-108">Para obter mais detalhes sobre como obter uma cadeia de caracteres de mensagem do evento, consulte [Formatando mensagens de evento](formatting-event-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c0e87-108">For more details on getting a message string from the event, see [Formatting Event Messages](formatting-event-messages.md).</span></span>

<span data-ttu-id="c0e87-109">Para renderizar o evento como uma cadeia de caracteres XML, chame a função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) .</span><span class="sxs-lookup"><span data-stu-id="c0e87-109">To render the event as an XML string, call the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function.</span></span> <span data-ttu-id="c0e87-110">No entanto, se você quiser renderizar partes específicas do evento, primeiro você deve chamar o [**EvtCreateRenderContext**](/windows/desktop/api/WinEvt/nf-winevt-evtcreaterendercontext) para especificar as partes do evento que deseja renderizar.</span><span class="sxs-lookup"><span data-stu-id="c0e87-110">However, if you want to render specific pieces of the event, you must first call the [**EvtCreateRenderContext**](/windows/desktop/api/WinEvt/nf-winevt-evtcreaterendercontext) to specify the pieces of the event that you want to render.</span></span> <span data-ttu-id="c0e87-111">Você pode renderizar valores específicos do evento, os valores da seção dados do usuário ou dados do evento do evento ou os valores das propriedades relacionadas ao sistema do evento.</span><span class="sxs-lookup"><span data-stu-id="c0e87-111">You can render specific values from the event, the values from the user data or event data section of the event, or the values from the system-related properties of the event.</span></span> <span data-ttu-id="c0e87-112">Para obter detalhes sobre os componentes de um evento, consulte [esquema de evento](eventschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c0e87-112">For details on the components of an event, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="c0e87-113">O exemplo a seguir mostra como renderizar um evento como uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="c0e87-113">The following example shows how to render an event as an XML string.</span></span>


```C++
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    // The EvtRenderEventXml flag tells EvtRender to render the event as an XML string.
    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    wprintf(L"\n\n%s", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



<span data-ttu-id="c0e87-114">O exemplo a seguir mostra como renderizar os valores de propriedades da seção System do evento.</span><span class="sxs-lookup"><span data-stu-id="c0e87-114">The following example shows how to render the properties values from the system section of the event.</span></span> <span data-ttu-id="c0e87-115">Para renderizar os dados de usuário ou as propriedades de dados de evento do evento, substitua o sinalizador EvtRenderContextSystem pelo sinalizador EvtRenderContextUser ao criar o contexto de renderização.</span><span class="sxs-lookup"><span data-stu-id="c0e87-115">To render the user data or event data properties of the event, replace the EvtRenderContextSystem flag with the EvtRenderContextUser flag when creating the rendering context.</span></span>


```C++
DWORD PrintEventSystemData(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hContext = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    PEVT_VARIANT pRenderedValues = NULL;
    WCHAR wsGuid[50];
    LPWSTR pwsSid = NULL;
    ULONGLONG ullTimeStamp = 0;
    ULONGLONG ullNanoseconds = 0;
    SYSTEMTIME st;
    FILETIME ft;

    // Identify the components of the event that you want to render. In this case,
    // render the system section of the event.
    hContext = EvtCreateRenderContext(0, NULL, EvtRenderContextSystem);
    if (NULL == hContext)
    {
        wprintf(L"EvtCreateRenderContext failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    // When you render the user data or system section of the event, you must specify
    // the EvtRenderEventValues flag. The function returns an array of variant values 
    // for each element in the user data or system section of the event. For user data
    // or event data, the values are returned in the same order as the elements are 
    // defined in the event. For system data, the values are returned in the order defined
    // in the EVT_SYSTEM_PROPERTY_ID enumeration.
    if (!EvtRender(hContext, hEvent, EvtRenderEventValues, dwBufferSize, pRenderedValues, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedValues = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pRenderedValues)
            {
                EvtRender(hContext, hEvent, EvtRenderEventValues, dwBufferSize, pRenderedValues, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    // Print the values from the System section of the element.
    wprintf(L"Provider Name: %s\n", pRenderedValues[EvtSystemProviderName].StringVal);
    if (NULL != pRenderedValues[EvtSystemProviderGuid].GuidVal)
    {
        StringFromGUID2(*(pRenderedValues[EvtSystemProviderGuid].GuidVal), wsGuid, sizeof(wsGuid)/sizeof(WCHAR));
        wprintf(L"Provider Guid: %s\n", wsGuid);
    }
    else 
    {
        wprintf(L"Provider Guid: NULL");
    }


    DWORD EventID = pRenderedValues[EvtSystemEventID].UInt16Val;
    if (EvtVarTypeNull != pRenderedValues[EvtSystemQualifiers].Type)
    {
        EventID = MAKELONG(pRenderedValues[EvtSystemEventID].UInt16Val, pRenderedValues[EvtSystemQualifiers].UInt16Val);
    }
    wprintf(L"EventID: %lu\n", EventID);

    wprintf(L"Version: %u\n", (EvtVarTypeNull == pRenderedValues[EvtSystemVersion].Type) ? 0 : pRenderedValues[EvtSystemVersion].ByteVal);
    wprintf(L"Level: %u\n", (EvtVarTypeNull == pRenderedValues[EvtSystemLevel].Type) ? 0 : pRenderedValues[EvtSystemLevel].ByteVal);
    wprintf(L"Task: %hu\n", (EvtVarTypeNull == pRenderedValues[EvtSystemTask].Type) ? 0 : pRenderedValues[EvtSystemTask].UInt16Val);
    wprintf(L"Opcode: %u\n", (EvtVarTypeNull == pRenderedValues[EvtSystemOpcode].Type) ? 0 : pRenderedValues[EvtSystemOpcode].ByteVal);
    wprintf(L"Keywords: 0x%I64x\n", pRenderedValues[EvtSystemKeywords].UInt64Val);

    ullTimeStamp = pRenderedValues[EvtSystemTimeCreated].FileTimeVal;
    ft.dwHighDateTime = (DWORD)((ullTimeStamp >> 32) & 0xFFFFFFFF);
    ft.dwLowDateTime = (DWORD)(ullTimeStamp & 0xFFFFFFFF);

    FileTimeToSystemTime(&ft, &st);
    ullNanoseconds = (ullTimeStamp % 10000000) * 100; // Display nanoseconds instead of milliseconds for higher resolution
    wprintf(L"TimeCreated SystemTime: %02d/%02d/%02d %02d:%02d:%02d.%I64u)\n", 
        st.wMonth, st.wDay, st.wYear, st.wHour, st.wMinute, st.wSecond, ullNanoseconds);

    wprintf(L"EventRecordID: %I64u\n", pRenderedValues[EvtSystemEventRecordId].UInt64Val);

    if (EvtVarTypeNull != pRenderedValues[EvtSystemActivityID].Type)
    {
        StringFromGUID2(*(pRenderedValues[EvtSystemActivityID].GuidVal), wsGuid, sizeof(wsGuid)/sizeof(WCHAR));
        wprintf(L"Correlation ActivityID: %s\n", wsGuid);
    }

    if (EvtVarTypeNull != pRenderedValues[EvtSystemRelatedActivityID].Type)
    {
        StringFromGUID2(*(pRenderedValues[EvtSystemRelatedActivityID].GuidVal), wsGuid, sizeof(wsGuid)/sizeof(WCHAR));
        wprintf(L"Correlation RelatedActivityID: %s\n", wsGuid);
    }

    wprintf(L"Execution ProcessID: %lu\n", pRenderedValues[EvtSystemProcessID].UInt32Val);
    wprintf(L"Execution ThreadID: %lu\n", pRenderedValues[EvtSystemThreadID].UInt32Val);
    wprintf(L"Channel: %s\n", (EvtVarTypeNull == pRenderedValues[EvtSystemChannel].Type) ? L"" : pRenderedValues[EvtSystemChannel].StringVal);
    wprintf(L"Computer: %s\n", pRenderedValues[EvtSystemComputer].StringVal);

    if (EvtVarTypeNull != pRenderedValues[EvtSystemUserID].Type)
    {
        if (ConvertSidToStringSid(pRenderedValues[EvtSystemUserID].SidVal, &pwsSid))
        {
            wprintf(L"Security UserID: %s\n", pwsSid);
            LocalFree(pwsSid);
        }
    }

cleanup:

    if (hContext)
        EvtClose(hContext);

    if (pRenderedValues)
        free(pRenderedValues);

    return status;
}
```


<span data-ttu-id="c0e87-116">O exemplo a seguir mostra como renderizar os valores específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="c0e87-116">The following example shows how to render the specific values from the event.</span></span> <span data-ttu-id="c0e87-117">Use uma expressão XPath para especificar o nó ou atributo específico a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="c0e87-117">Use an XPath expression to specify the specific node or attribute to retrieve.</span></span> <span data-ttu-id="c0e87-118">Você pode especificar uma ou mais expressões para recuperar um ou mais valores.</span><span class="sxs-lookup"><span data-stu-id="c0e87-118">You can specify one or more expressions to retrieve one or more values.</span></span>


```C++
DWORD PrintEventValues(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hContext = NULL;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    PEVT_VARIANT pRenderedValues = NULL;
    LPWSTR ppValues[] = {L"Event/System/Provider/@Name", L"Event/System/Channel"};
    DWORD count = sizeof(ppValues)/sizeof(LPWSTR);

    // Identify the components of the event that you want to render. In this case,
    // render the provider's name and channel from the system section of the event.
    // To get user data from the event, you can specify an expression such as
    // L"Event/EventData/Data[@Name=\"<data name goes here>\"]".
    hContext = EvtCreateRenderContext(count, (LPCWSTR*)ppValues, EvtRenderContextValues);
    if (NULL == hContext)
    {
        wprintf(L"EvtCreateRenderContext failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    // The function returns an array of variant values for each element or attribute that
    // you want to retrieve from the event. The values are returned in the same order as 
    // you requested them.
    if (!EvtRender(hContext, hEvent, EvtRenderEventValues, dwBufferSize, pRenderedValues, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedValues = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pRenderedValues)
            {
                EvtRender(hContext, hEvent, EvtRenderEventValues, dwBufferSize, pRenderedValues, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    // Print the selected values.
    wprintf(L"\nProvider Name: %s\n", pRenderedValues[0].StringVal);
    wprintf(L"Channel: %s\n", (EvtVarTypeNull == pRenderedValues[1].Type) ? L"" : pRenderedValues[1].StringVal);

cleanup:

    if (hContext)
        EvtClose(hContext);

    if (pRenderedValues)
        free(pRenderedValues);

    return status;
}
```
