---
title: Consultando eventos
description: Você pode consultar eventos de um canal ou de um arquivo de log.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 981e4a8c39daebbce641c79e7d26331b9b36845d3c71fd1902ea667ca85c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587797"
---
# <a name="querying-for-events"></a>Consultando eventos

Você pode consultar eventos de um canal ou de um arquivo de log. O canal ou o arquivo de log pode existir no computador local ou em um computador remoto. Para especificar os eventos que você deseja obter do canal ou arquivo de log, use uma consulta XPath ou uma consulta XML de estrutura. Para obter detalhes sobre como escrever a consulta, consulte [Consumindo eventos](consuming-events.md).

Para consultar eventos, chame a [**função EvtQuery.**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) Você pode especificar a ordem na qual os eventos são retornados (mais antigo para o mais recente (o padrão) ou mais recente para o mais antigo) e se deve tolerar expressões XPath malformadas na consulta (para obter detalhes sobre como a função ignora as expressões malformadas, consulte o sinalizador [**EvtQueryTolerateQueryErrors).**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)

O exemplo a seguir mostra como consultar eventos de um canal usando uma expressão XPath.


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



O exemplo a seguir mostra como consultar eventos de um canal usando uma consulta XML estruturada. Os eventos são retornados na ordem do mais recente para o mais antigo.


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



Se você estiver usando uma consulta XML estruturada e passar o sinalizador EvtQueryTolerateQueryErrors para [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), a função terá êxito mesmo que uma ou mais das consultas na consulta estruturada possam ter realmente falhado. Para determinar quais consultas na consulta estruturada tiveram êxito ou falharam, chame a [**função EvtGetQueryInfo.**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) Se você não passar o sinalizador EvtQueryTolerateQueryErrors, a **função EvtQuery** falhará com o primeiro erro encontrado na consulta. Se a consulta falhar com ERROR \_ EVT INVALID QUERY, chame a função \_ \_ [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) para obter uma cadeia de caracteres de mensagem que descreve o erro XPath.

O exemplo a seguir mostra como determinar o sucesso ou a falha de cada consulta em uma consulta estruturada ao passar o sinalizador EvtQueryTolerateQueryErrors para [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).


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



## <a name="reading-events-from-the-result-set"></a>Lendo eventos do conjunto de resultados

Para enumerar os eventos no conjunto de resultados, chame a função [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) em um loop até que a função retorne **FALSE** e a [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorne ERROR \_ NO MORE \_ \_ ITEMS. Os eventos no conjunto de resultados não são estáticos; novos eventos gravados no canal serão incluídos no conjunto de resultados até que ERROR \_ NO MORE ITEMS seja \_ \_ definido. Para melhorar o desempenho, busque eventos do conjunto de resultados em lotes (levando em conta o tamanho de cada evento ao determinar o número de eventos a buscar).

O exemplo a seguir mostra como enumerar os eventos em um conjunto de resultados.


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



Para obter detalhes sobre como renderizar os eventos que você obter do conjunto de resultados, consulte [Eventos de renderização](rendering-events.md).

Se você quiser consultar eventos de onde paramos, crie um indicador do último evento que você leu e use-o na próxima vez que executar a consulta. Para obter detalhes, consulte [Eventos de indicadores](bookmarking-events.md).

 

 