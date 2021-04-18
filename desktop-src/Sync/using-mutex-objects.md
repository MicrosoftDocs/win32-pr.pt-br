---
description: Você pode usar um objeto mutex para proteger um recurso compartilhado de acesso simultâneo por vários threads ou processos.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Usando objetos mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756355"
---
# <a name="using-mutex-objects"></a><span data-ttu-id="58eb2-103">Usando objetos mutex</span><span class="sxs-lookup"><span data-stu-id="58eb2-103">Using Mutex Objects</span></span>

<span data-ttu-id="58eb2-104">Você pode usar um [objeto mutex](mutex-objects.md) para proteger um recurso compartilhado de acesso simultâneo por vários threads ou processos.</span><span class="sxs-lookup"><span data-stu-id="58eb2-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="58eb2-105">Cada thread deve aguardar a propriedade do mutex antes de poder executar o código que acessa o recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="58eb2-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="58eb2-106">Por exemplo, se vários threads compartilharem o acesso a um banco de dados, os threads poderão usar um objeto mutex para permitir apenas um thread por vez para gravar no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="58eb2-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="58eb2-107">O exemplo a seguir usa a função [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) para criar um objeto mutex e a função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para criar threads de trabalho.</span><span class="sxs-lookup"><span data-stu-id="58eb2-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="58eb2-108">Quando um thread desse processo grava no banco de dados, ele primeiro solicita a propriedade do mutex usando a função [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="58eb2-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="58eb2-109">Se o thread obtiver a propriedade do mutex, ele gravará no banco de dados e, em seguida, liberará sua propriedade do mutex usando a função [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .</span><span class="sxs-lookup"><span data-stu-id="58eb2-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="58eb2-110">Este exemplo usa manipulação de exceção estruturada para garantir que o thread libere corretamente o objeto mutex.</span><span class="sxs-lookup"><span data-stu-id="58eb2-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="58eb2-111">O bloco **\_ \_ finally** de código é executado independentemente de como o bloco **\_ \_ try** é encerrado (a menos que o bloco **\_ \_ try** inclua uma chamada para a função [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ).</span><span class="sxs-lookup"><span data-stu-id="58eb2-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="58eb2-112">Isso impede que o objeto mutex seja abandonado inadvertidamente.</span><span class="sxs-lookup"><span data-stu-id="58eb2-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="58eb2-113">Se um mutex for abandonado, o thread que possuía o mutex não o liberará corretamente antes de ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="58eb2-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="58eb2-114">Nesse caso, o status do recurso compartilhado é indeterminado e continuar a usar o mutex pode obscurecer um erro potencialmente sério.</span><span class="sxs-lookup"><span data-stu-id="58eb2-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="58eb2-115">Alguns aplicativos podem tentar restaurar o recurso para um estado consistente; Este exemplo simplesmente retorna um erro e para de usar o mutex.</span><span class="sxs-lookup"><span data-stu-id="58eb2-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="58eb2-116">Para obter mais informações, consulte [objetos mutex](mutex-objects.md).</span><span class="sxs-lookup"><span data-stu-id="58eb2-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


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



 

 
