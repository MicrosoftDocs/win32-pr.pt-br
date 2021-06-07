---
description: O exemplo a seguir cria uma rotina de temporizador que será executada por um thread de uma fila de temporizador após um atraso de 10 segundos.
ms.assetid: 779156fe-f825-452b-acbe-e2cb189e24d2
title: Usando filas de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d084a03eb25301f94361c1e7ca6b76dd9fee269
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549928"
---
# <a name="using-timer-queues"></a><span data-ttu-id="3f369-103">Usando filas de temporizador</span><span class="sxs-lookup"><span data-stu-id="3f369-103">Using Timer Queues</span></span>

<span data-ttu-id="3f369-104">O exemplo a seguir cria uma rotina de temporizador que será executada por um thread de uma fila [de temporizador](timer-queues.md) após um atraso de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="3f369-104">The following example creates a timer routine that will be executed by a thread from a [timer queue](timer-queues.md) after a 10 second delay.</span></span> <span data-ttu-id="3f369-105">Primeiro, o código usa a [**função CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para criar um objeto de evento que é sinalizado quando o thread de fila de temporizador é concluído.</span><span class="sxs-lookup"><span data-stu-id="3f369-105">First, the code uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create an event object that is signaled when the timer-queue thread completes.</span></span> <span data-ttu-id="3f369-106">Em seguida, ele cria uma fila de temporizador e um temporizador de fila, usando as funções [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) e [**CreateTimerQueueTimer,**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3f369-106">Then it creates a timer queue and a timer-queue timer, using the [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) and [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) functions, respectively.</span></span> <span data-ttu-id="3f369-107">O código usa a [**função WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para determinar quando a rotina do temporizador foi concluída.</span><span class="sxs-lookup"><span data-stu-id="3f369-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer routine has completed.</span></span> <span data-ttu-id="3f369-108">Por fim, o código [**chama DeleteTimerQueue**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue) para limpar.</span><span class="sxs-lookup"><span data-stu-id="3f369-108">Finally, the code calls [**DeleteTimerQueue**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue) to clean up.</span></span>

<span data-ttu-id="3f369-109">Para obter mais informações sobre a rotina do temporizador, [**consulte WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f369-109">For more information on the timer routine, see [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE gDoneEvent;

VOID CALLBACK TimerRoutine(PVOID lpParam, BOOLEAN TimerOrWaitFired)
{
    if (lpParam == NULL)
    {
        printf("TimerRoutine lpParam is NULL\n");
    }
    else
    {
        // lpParam points to the argument; in this case it is an int

        printf("Timer routine called. Parameter is %d.\n", 
                *(int*)lpParam);
        if(TimerOrWaitFired)
        {
            printf("The wait timed out.\n");
        }
        else
        {
            printf("The wait event was signaled.\n");
        }
    }

    SetEvent(gDoneEvent);
}

int main()
{
    HANDLE hTimer = NULL;
    HANDLE hTimerQueue = NULL;
    int arg = 123;

    // Use an event object to track the TimerRoutine execution
    gDoneEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == gDoneEvent)
    {
        printf("CreateEvent failed (%d)\n", GetLastError());
        return 1;
    }

    // Create the timer queue.
    hTimerQueue = CreateTimerQueue();
    if (NULL == hTimerQueue)
    {
        printf("CreateTimerQueue failed (%d)\n", GetLastError());
        return 2;
    }

    // Set a timer to call the timer routine in 10 seconds.
    if (!CreateTimerQueueTimer( &hTimer, hTimerQueue, 
            (WAITORTIMERCALLBACK)TimerRoutine, &arg , 10000, 0, 0))
    {
        printf("CreateTimerQueueTimer failed (%d)\n", GetLastError());
        return 3;
    }

    // TODO: Do other useful work here 

    printf("Call timer routine in 10 seconds...\n");

    // Wait for the timer-queue thread to complete using an event 
    // object. The thread will signal the event at that time.

    if (WaitForSingleObject(gDoneEvent, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());

    CloseHandle(gDoneEvent);

    // Delete all timers in the timer queue.
    if (!DeleteTimerQueue(hTimerQueue))
        printf("DeleteTimerQueue failed (%d)\n", GetLastError());

    return 0;
}
```



 

 
