---
title: Consultando eventos
description: Você pode consultar eventos de um canal ou de um arquivo de log.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105781476"
---
# <a name="querying-for-events"></a><span data-ttu-id="cfdc8-103">Consultando eventos</span><span class="sxs-lookup"><span data-stu-id="cfdc8-103">Querying for Events</span></span>

<span data-ttu-id="cfdc8-104">Você pode consultar eventos de um canal ou de um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-104">You can query for events from a channel or a log file.</span></span> <span data-ttu-id="cfdc8-105">O canal ou arquivo de log pode existir no computador local ou em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-105">The channel or log file can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="cfdc8-106">Para especificar os eventos que você deseja obter do canal ou arquivo de log, use uma consulta XPath ou uma consulta XML de estrutura.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-106">To specify the events that you want to get from the channel or log file, you use an XPath query or a structure XML query.</span></span> <span data-ttu-id="cfdc8-107">Para obter detalhes sobre como escrever a consulta, consulte [consumindo eventos](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="cfdc8-107">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="cfdc8-108">Para consultar eventos, chame a função [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) .</span><span class="sxs-lookup"><span data-stu-id="cfdc8-108">To query events, call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function.</span></span> <span data-ttu-id="cfdc8-109">Você pode especificar a ordem na qual os eventos são retornados (o mais antigo para o mais recente (o padrão) ou mais recente para o mais antigo) e se devem tolerar expressões XPath malformadas na consulta (para obter detalhes sobre como a função ignora as expressões malformadas, consulte o sinalizador [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) ).</span><span class="sxs-lookup"><span data-stu-id="cfdc8-109">You can specify the order in which the events are returned (oldest to newest (the default) or newest to oldest) and whether to tolerate malformed XPath expressions in the query (for details on how the function ignores the malformed expressions, see the [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) flag).</span></span>

<span data-ttu-id="cfdc8-110">O exemplo a seguir mostra como consultar eventos de um canal usando uma expressão XPath.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-110">The following example shows how to query events from a channel using an XPath expression.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="cfdc8-111">O exemplo a seguir mostra como consultar eventos de um canal usando uma consulta XML estruturada.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-111">The following example shows how to query events from a channel using a structured XML query.</span></span> <span data-ttu-id="cfdc8-112">Os eventos são retornados na ordem do mais recente para o mais antigo.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-112">The events are returned in order from newest to oldest.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="cfdc8-113">Se você estiver usando uma consulta XML estruturada e passar o sinalizador EvtQueryTolerateQueryErrors para [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), a função terá êxito mesmo que uma ou mais das consultas na consulta estruturada possam ter falhado na verdade.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-113">If you are using a structured XML query and pass the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), the function succeeds even though one or more of the queries in the structured query may have actually failed.</span></span> <span data-ttu-id="cfdc8-114">Para determinar quais consultas na consulta estruturada tiveram êxito ou falharam, chame a função [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) .</span><span class="sxs-lookup"><span data-stu-id="cfdc8-114">To determine which queries in the structured query succeeded or failed, call the [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) function.</span></span> <span data-ttu-id="cfdc8-115">Se você não passar o sinalizador EvtQueryTolerateQueryErrors, a função **EvtQuery** falhará com o primeiro erro encontrado na consulta.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-115">If you do not pass the EvtQueryTolerateQueryErrors flag, the **EvtQuery** function will fail with the first error that it finds in the query.</span></span> <span data-ttu-id="cfdc8-116">Se a consulta falhar com o erro \_ EVT de \_ consulta inválida \_ , chame a função [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) para obter uma cadeia de caracteres de mensagem que descreve o erro XPath.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-116">If the query fails with ERROR\_EVT\_INVALID\_QUERY, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function to get a message string that describes the XPath error.</span></span>

<span data-ttu-id="cfdc8-117">O exemplo a seguir mostra como determinar o êxito ou a falha de cada consulta em uma consulta estruturada ao passar o sinalizador EvtQueryTolerateQueryErrors para [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span><span class="sxs-lookup"><span data-stu-id="cfdc8-117">The following example shows how to determine the success or failure of each query in a structured query when passing the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span></span>


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a><span data-ttu-id="cfdc8-118">Lendo eventos do conjunto de resultados</span><span class="sxs-lookup"><span data-stu-id="cfdc8-118">Reading events from the result set</span></span>

<span data-ttu-id="cfdc8-119">Para enumerar os eventos no conjunto de resultados, chame a função [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) em um loop até que a função retorne **false** e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorne \_ um erro sem \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-119">To enumerate the events in the result set, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop until the function returns **FALSE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="cfdc8-120">Os eventos no conjunto de resultados não são estáticos; novos eventos que são gravados no canal serão incluídos no conjunto de resultados até o erro \_ nenhum \_ outro \_ item for definido.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-120">The events in the result set are not static; new events that are written to the channel will be included in the result set until ERROR\_NO\_MORE\_ITEMS is set.</span></span> <span data-ttu-id="cfdc8-121">Para melhorar o desempenho, busque eventos do conjunto de resultados em lotes (levando em conta o tamanho de cada evento ao determinar o número de eventos a serem obtidos).</span><span class="sxs-lookup"><span data-stu-id="cfdc8-121">To improve performance, fetch events from the result set in batches (taking into account the size of each event when determining the number of events to fetch).</span></span>

<span data-ttu-id="cfdc8-122">O exemplo a seguir mostra como enumerar os eventos em um conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-122">The following example shows how to enumerate the events in a result set.</span></span>


```C++
// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display. PrintEvent is shown in RenderingEvents.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



<span data-ttu-id="cfdc8-123">Para obter detalhes sobre como renderizar os eventos obtidos do conjunto de resultados, consulte [renderizando eventos](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="cfdc8-123">For details on rendering the events that you get from the result set, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="cfdc8-124">Se você quiser consultar eventos de onde parou, crie um indicador do último evento que você leu e use-o na próxima vez em que executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="cfdc8-124">If you want to query for events from where you left off, create a bookmark of the last event that you read and use it the next time you run your query.</span></span> <span data-ttu-id="cfdc8-125">Para obter detalhes, consulte [eventos de indicador](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="cfdc8-125">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

 

 