---
description: O exemplo a seguir usa a função CreateEvent para criar dois objetos de evento e a função CreateThread para criar um thread.
ms.assetid: 0132ac94-b45b-438a-b96a-e77cfe522702
title: Aguardando vários objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c8ac12585a32ede0fc96506fa770a19198b18fea833b42a5cf45c75be677b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765037"
---
# <a name="waiting-for-multiple-objects"></a>Aguardando vários objetos

O exemplo a seguir usa a [**função CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para criar dois objetos de evento e a [**função CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para criar um thread. Em seguida, ele usa a função [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) para aguardar o thread definir o estado de um dos objetos a ser sinalizado usando a [**função SetEvent.**](/windows/win32/api/synchapi/nf-synchapi-resetevent)

Para ver um exemplo que aguarda um único objeto, consulte [Usando objetos Mutex](using-mutex-objects.md).


```C++
#include <windows.h>
#include <stdio.h>

HANDLE ghEvents[2];

DWORD WINAPI ThreadProc( LPVOID );

int main( void )
{
    HANDLE hThread; 
    DWORD i, dwEvent, dwThreadID; 

    // Create two event objects

    for (i = 0; i < 2; i++) 
    { 
        ghEvents[i] = CreateEvent( 
            NULL,   // default security attributes
            FALSE,  // auto-reset event object
            FALSE,  // initial state is nonsignaled
            NULL);  // unnamed object

        if (ghEvents[i] == NULL) 
        { 
            printf("CreateEvent error: %d\n", GetLastError() ); 
            ExitProcess(0); 
        } 
    } 

    // Create a thread

    hThread = CreateThread( 
                 NULL,         // default security attributes
                 0,            // default stack size
                 (LPTHREAD_START_ROUTINE) ThreadProc, 
                 NULL,         // no thread function arguments
                 0,            // default creation flags
                 &dwThreadID); // receive thread identifier

    if( hThread == NULL )
    {
        printf("CreateThread error: %d\n", GetLastError());
        return 1;
    }

    // Wait for the thread to signal one of the event objects

    dwEvent = WaitForMultipleObjects( 
        2,           // number of objects in array
        ghEvents,     // array of objects
        FALSE,       // wait for any object
        5000);       // five-second wait

    // The return value indicates which event is signaled

    switch (dwEvent) 
    { 
        // ghEvents[0] was signaled
        case WAIT_OBJECT_0 + 0: 
            // TODO: Perform tasks required by this event
            printf("First event was signaled.\n");
            break; 

        // ghEvents[1] was signaled
        case WAIT_OBJECT_0 + 1: 
            // TODO: Perform tasks required by this event
            printf("Second event was signaled.\n");
            break; 

        case WAIT_TIMEOUT:
            printf("Wait timed out.\n");
            break;

        // Return value is invalid.
        default: 
            printf("Wait error: %d\n", GetLastError()); 
            ExitProcess(0); 
    }

    // Close event handles

    for (i = 0; i < 2; i++) 
        CloseHandle(ghEvents[i]); 
    
    return 0;   
}

DWORD WINAPI ThreadProc( LPVOID lpParam )
{

    // lpParam not used in this example
    UNREFERENCED_PARAMETER( lpParam);

    // Set one event to the signaled state

    if ( !SetEvent(ghEvents[0]) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return 1;
    }
    return 0;
}
```



 

 
