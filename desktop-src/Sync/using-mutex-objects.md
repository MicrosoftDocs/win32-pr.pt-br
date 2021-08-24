---
description: Você pode usar um objeto mutex para proteger um recurso compartilhado de acesso simultâneo por vários threads ou processos.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Usando objetos mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c629d90e1cd811c62f62e1151cee4c3e2af77b84133e142fcfe7f93a35b2e5bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739256"
---
# <a name="using-mutex-objects"></a>Usando objetos mutex

Você pode usar um [objeto mutex](mutex-objects.md) para proteger um recurso compartilhado de acesso simultâneo por vários threads ou processos. Cada thread deve aguardar a propriedade do mutex antes de poder executar o código que acessa o recurso compartilhado. Por exemplo, se vários threads compartilharem o acesso a um banco de dados, os threads poderão usar um objeto mutex para permitir apenas um thread por vez para gravar no banco de dados.

O exemplo a seguir usa a função [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para criar um objeto mutex e a função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para criar threads de trabalho.

Quando um thread desse processo grava no banco de dados, ele primeiro solicita a propriedade do mutex usando a função [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) . Se o thread obtiver a propriedade do mutex, ele gravará no banco de dados e, em seguida, liberará sua propriedade do mutex usando a função [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .

Este exemplo usa manipulação de exceção estruturada para garantir que o thread libere corretamente o objeto mutex. O bloco **\_ \_ finally** de código é executado independentemente de como o bloco **\_ \_ try** é encerrado (a menos que o bloco **\_ \_ try** inclua uma chamada para a função [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ). Isso impede que o objeto mutex seja abandonado inadvertidamente.

Se um mutex for abandonado, o thread que possuía o mutex não o liberará corretamente antes de ser encerrado. Nesse caso, o status do recurso compartilhado é indeterminado e continuar a usar o mutex pode obscurecer um erro potencialmente sério. Alguns aplicativos podem tentar restaurar o recurso para um estado consistente; Este exemplo simplesmente retorna um erro e para de usar o mutex. Para obter mais informações, consulte [objetos mutex](mutex-objects.md).


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
