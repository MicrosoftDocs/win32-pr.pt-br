---
description: Os aplicativos podem usar objetos de evento em várias situações para notificar um thread em espera da ocorrência de um evento.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Usando objetos de evento (sincronização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c0c7ee5f58b8359e989b19ffc9c016dd1a6593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828531"
---
# <a name="using-event-objects-synchronization"></a><span data-ttu-id="df5bc-103">Usando objetos de evento (sincronização)</span><span class="sxs-lookup"><span data-stu-id="df5bc-103">Using Event Objects (Synchronization)</span></span>

<span data-ttu-id="df5bc-104">Os aplicativos podem usar [objetos de evento](event-objects.md) em várias situações para notificar um thread em espera da ocorrência de um evento.</span><span class="sxs-lookup"><span data-stu-id="df5bc-104">Applications can use [event objects](event-objects.md) in a number of situations to notify a waiting thread of the occurrence of an event.</span></span> <span data-ttu-id="df5bc-105">Por exemplo, as operações de e/s sobrepostas em arquivos, pipes nomeados e dispositivos de comunicação usam um objeto de evento para sinalizar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="df5bc-105">For example, overlapped I/O operations on files, named pipes, and communications devices use an event object to signal their completion.</span></span> <span data-ttu-id="df5bc-106">Para obter mais informações sobre o uso de objetos de evento em operações de e/s sobrepostas, consulte [sincronização e entrada e saída sobrepostas](synchronization-and-overlapped-input-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="df5bc-106">For more information about the use of event objects in overlapped I/O operations, see [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).</span></span>

<span data-ttu-id="df5bc-107">O exemplo a seguir usa objetos de evento para impedir que vários threads leiam de um buffer de memória compartilhado enquanto um thread mestre está gravando nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="df5bc-107">The following example uses event objects to prevent several threads from reading from a shared memory buffer while a master thread is writing to that buffer.</span></span> <span data-ttu-id="df5bc-108">Primeiro, o thread mestre usa a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para criar um objeto de evento de redefinição manual cujo estado inicial é não sinalizado.</span><span class="sxs-lookup"><span data-stu-id="df5bc-108">First, the master thread uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event object whose initial state is nonsignaled.</span></span> <span data-ttu-id="df5bc-109">Em seguida, ele cria vários threads de leitor.</span><span class="sxs-lookup"><span data-stu-id="df5bc-109">Then it creates several reader threads.</span></span> <span data-ttu-id="df5bc-110">O thread mestre executa uma operação de gravação e, em seguida, define o objeto de evento para o estado sinalizado quando a gravação termina.</span><span class="sxs-lookup"><span data-stu-id="df5bc-110">The master thread performs a write operation and then sets the event object to the signaled state when it has finished writing.</span></span>

<span data-ttu-id="df5bc-111">Antes de iniciar uma operação de leitura, cada thread de leitor usa [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para aguardar o objeto de evento de redefinição manual ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="df5bc-111">Before starting a read operation, each reader thread uses [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the manual-reset event object to be signaled.</span></span> <span data-ttu-id="df5bc-112">Quando **WaitForSingleObject** é retornado, isso indica que o thread principal está pronto para que ele comece sua operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="df5bc-112">When **WaitForSingleObject** returns, this indicates that the main thread is ready for it to begin its read operation.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 4 

HANDLE ghWriteEvent; 
HANDLE ghThreads[THREADCOUNT];

DWORD WINAPI ThreadProc(LPVOID);

void CreateEventsAndThreads(void) 
{
    int i; 
    DWORD dwThreadID; 

    // Create a manual-reset event object. The write thread sets this
    // object to the signaled state when it finishes writing to a 
    // shared buffer. 

    ghWriteEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        TEXT("WriteEvent")  // object name
        ); 

    if (ghWriteEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    // Create multiple threads to read from the buffer.

    for(i = 0; i < THREADCOUNT; i++) 
    {
        // TODO: More complex scenarios may require use of a parameter
        //   to the thread procedure, such as an event per thread to  
        //   be used for synchronization.
        ghThreads[i] = CreateThread(
            NULL,              // default security
            0,                 // default stack size
            ThreadProc,        // name of the thread function
            NULL,              // no thread parameters
            0,                 // default startup flags
            &dwThreadID); 

        if (ghThreads[i] == NULL) 
        {
            printf("CreateThread failed (%d)\n", GetLastError());
            return;
        }
    }
}

void WriteToBuffer(VOID) 
{
    // TODO: Write to the shared buffer.
    
    printf("Main thread writing to the shared buffer...\n");

    // Set ghWriteEvent to signaled

    if (! SetEvent(ghWriteEvent) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return;
    }
}

void CloseEvents()
{
    // Close all event handles (currently, only one global handle).
    
    CloseHandle(ghWriteEvent);
}

int main( void )
{
    DWORD dwWaitResult;

    // TODO: Create the shared buffer

    // Create events and THREADCOUNT threads to read from the buffer

    CreateEventsAndThreads();

    // At this point, the reader threads have started and are most
    // likely waiting for the global event to be signaled. However, 
    // it is safe to write to the buffer because the event is a 
    // manual-reset event.
    
    WriteToBuffer();

    printf("Main thread waiting for threads to exit...\n");

    // The handle for each thread is signaled when the thread is
    // terminated.
    dwWaitResult = WaitForMultipleObjects(
        THREADCOUNT,   // number of handles in array
        ghThreads,     // array of thread handles
        TRUE,          // wait until all are signaled
        INFINITE);

    switch (dwWaitResult) 
    {
        // All thread objects were signaled
        case WAIT_OBJECT_0: 
            printf("All threads ended, cleaning up for application exit...\n");
            break;

        // An error occurred
        default: 
            printf("WaitForMultipleObjects failed (%d)\n", GetLastError());
            return 1;
    } 
            
    // Close the events to clean up

    CloseEvents();

    return 0;
}

DWORD WINAPI ThreadProc(LPVOID lpParam) 
{
    // lpParam not used in this example.
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult;

    printf("Thread %d waiting for write event...\n", GetCurrentThreadId());
    
    dwWaitResult = WaitForSingleObject( 
        ghWriteEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            //
            // TODO: Read from the shared buffer
            //
            printf("Thread %d reading from buffer\n", 
                   GetCurrentThreadId());
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    // Now that we are done reading the buffer, we could use another
    // event to signal that this thread is no longer reading. This
    // example simply uses the thread handle for synchronization (the
    // handle is signaled when the thread terminates.)

    printf("Thread %d exiting\n", GetCurrentThreadId());
    return 1;
}

```



 

 
