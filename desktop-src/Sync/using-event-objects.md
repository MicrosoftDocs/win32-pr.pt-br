---
description: Os aplicativos podem usar objetos de evento em várias situações para notificar um thread em espera da ocorrência de um evento.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Usando objetos de evento (sincronização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8466ca1104a4d8e6ddaaed3e0618bea3db68bd1954aaf3b859f66fb93a3aac79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765327"
---
# <a name="using-event-objects-synchronization"></a>Usando objetos de evento (sincronização)

Os aplicativos podem usar [objetos de evento](event-objects.md) em várias situações para notificar um thread em espera da ocorrência de um evento. Por exemplo, as operações de e/s sobrepostas em arquivos, pipes nomeados e dispositivos de comunicação usam um objeto de evento para sinalizar sua conclusão. Para obter mais informações sobre o uso de objetos de evento em operações de e/s sobrepostas, consulte [sincronização e entrada e saída sobrepostas](synchronization-and-overlapped-input-and-output.md).

O exemplo a seguir usa objetos de evento para impedir que vários threads leiam de um buffer de memória compartilhado enquanto um thread mestre está gravando nesse buffer. Primeiro, o thread mestre usa a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para criar um objeto de evento de redefinição manual cujo estado inicial é não sinalizado. Em seguida, ele cria vários threads de leitor. O thread mestre executa uma operação de gravação e, em seguida, define o objeto de evento para o estado sinalizado quando a gravação termina.

Antes de iniciar uma operação de leitura, cada thread de leitor usa [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) para aguardar o objeto de evento de redefinição manual ser sinalizado. Quando **WaitForSingleObject** é retornado, isso indica que o thread principal está pronto para que ele comece sua operação de leitura.


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



 

 
