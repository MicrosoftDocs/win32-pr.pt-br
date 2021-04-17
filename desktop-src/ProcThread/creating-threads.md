---
description: A função CreateThread cria um novo thread para um processo.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Criando threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545088779bdaff665a8079296014535ab244e821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782299"
---
# <a name="creating-threads"></a><span data-ttu-id="b3fa9-103">Criando threads</span><span class="sxs-lookup"><span data-stu-id="b3fa9-103">Creating Threads</span></span>

<span data-ttu-id="b3fa9-104">A função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) cria um novo thread para um processo.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="b3fa9-105">O thread de criação deve especificar o endereço inicial do código que o novo thread será executado.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-105">The creating thread must specify the starting address of the code that the new thread is to execute.</span></span> <span data-ttu-id="b3fa9-106">Normalmente, o endereço inicial é o nome de uma função definida no código do programa (para obter mais informações, consulte [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="b3fa9-106">Typically, the starting address is the name of a function defined in the program code (for more information, see [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span></span> <span data-ttu-id="b3fa9-107">Essa função usa um único parâmetro e retorna um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b3fa9-107">This function takes a single parameter and returns a **DWORD** value.</span></span> <span data-ttu-id="b3fa9-108">Um processo pode ter vários threads executando simultaneamente a mesma função.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-108">A process can have multiple threads simultaneously executing the same function.</span></span>

<span data-ttu-id="b3fa9-109">Veja a seguir um exemplo simples que demonstra como criar um novo thread que executa a função definida localmente, `MyThreadFunction` .</span><span class="sxs-lookup"><span data-stu-id="b3fa9-109">The following is a simple example that demonstrates how to create a new thread that executes the locally defined function, `MyThreadFunction`.</span></span>

<span data-ttu-id="b3fa9-110">O thread de chamada usa a função [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para persistir até que todos os threads de trabalho sejam encerrados.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-110">The calling thread uses the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to persist until all worker threads have terminated.</span></span> <span data-ttu-id="b3fa9-111">O thread de chamada é bloqueado enquanto está aguardando; para continuar o processamento, um thread de chamada usará [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) e aguardaria que cada thread de trabalho sinalize seu objeto de espera.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-111">The calling thread blocks while it is waiting; to continue processing, a calling thread would use [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) and wait for each worker thread to signal its wait object.</span></span> <span data-ttu-id="b3fa9-112">Observe que se você fechar o identificador para um thread de trabalho antes de ele ser encerrado, isso não encerrará o thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-112">Note that if you were to close the handle to a worker thread before it terminated, this does not terminate the worker thread.</span></span> <span data-ttu-id="b3fa9-113">No entanto, o identificador não estará disponível para uso em chamadas de função subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-113">However, the handle will be unavailable for use in subsequent function calls.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



<span data-ttu-id="b3fa9-114">A `MyThreadFunction` função evita o uso da CRT (biblioteca de tempo de execução) do C, pois muitas de suas funções não são thread-safe, especialmente se você não estiver usando o CRT multithread.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-114">The `MyThreadFunction` function avoids the use of the C run-time library (CRT), as many of its functions are not thread-safe, particularly if you are not using the multithreaded CRT.</span></span> <span data-ttu-id="b3fa9-115">Se você quiser usar o CRT em uma `ThreadProc` função, use a função **\_ beginthreadex** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-115">If you would like to use the CRT in a `ThreadProc` function, use the **\_beginthreadex** function instead.</span></span>

<span data-ttu-id="b3fa9-116">É arriscado passar o endereço de uma variável local se o thread de criação sair antes do novo thread, porque o ponteiro se torna inválido.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-116">It is risky to pass the address of a local variable if the creating thread exits before the new thread, because the pointer becomes invalid.</span></span> <span data-ttu-id="b3fa9-117">Em vez disso, passe um ponteiro para a memória alocada dinamicamente ou faça a espera da criação do thread para que o novo thread seja encerrado.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-117">Instead, either pass a pointer to dynamically allocated memory or make the creating thread wait for the new thread to terminate.</span></span> <span data-ttu-id="b3fa9-118">Os dados também podem ser passados do thread de criação para o novo thread usando variáveis globais.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-118">Data can also be passed from the creating thread to the new thread using global variables.</span></span> <span data-ttu-id="b3fa9-119">Com variáveis globais, geralmente é necessário sincronizar o acesso por vários threads.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-119">With global variables, it is usually necessary to synchronize access by multiple threads.</span></span> <span data-ttu-id="b3fa9-120">Para obter mais informações sobre sincronização, consulte [sincronizando a execução de vários threads](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="b3fa9-120">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="b3fa9-121">O thread de criação pode usar os argumentos para [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para especificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3fa9-121">The creating thread can use the arguments to [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to specify the following:</span></span>

-   <span data-ttu-id="b3fa9-122">Os atributos de segurança para o identificador para o novo thread.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-122">The security attributes for the handle to the new thread.</span></span> <span data-ttu-id="b3fa9-123">Esses atributos de segurança incluem um sinalizador de herança que determina se o identificador pode ser herdado por processos filho.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-123">These security attributes include an inheritance flag that determines whether the handle can be inherited by child processes.</span></span> <span data-ttu-id="b3fa9-124">Os atributos de segurança também incluem um descritor de segurança, que o sistema usa para executar verificações de acesso em todos os usos subsequentes do identificador do thread antes de o acesso ser concedido.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-124">The security attributes also include a security descriptor, which the system uses to perform access checks on all subsequent uses of the thread's handle before access is granted.</span></span>
-   <span data-ttu-id="b3fa9-125">O tamanho inicial da pilha do novo thread.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-125">The initial stack size of the new thread.</span></span> <span data-ttu-id="b3fa9-126">A pilha do thread é alocada automaticamente no espaço de memória do processo; o sistema aumenta a pilha conforme necessário e a libera quando o thread é encerrado.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-126">The thread's stack is allocated automatically in the memory space of the process; the system increases the stack as needed and frees it when the thread terminates.</span></span> <span data-ttu-id="b3fa9-127">Para obter mais informações, consulte [tamanho da pilha de threads](thread-stack-size.md).</span><span class="sxs-lookup"><span data-stu-id="b3fa9-127">For more information, see [Thread Stack Size](thread-stack-size.md).</span></span>
-   <span data-ttu-id="b3fa9-128">Um sinalizador de criação que permite que você crie o thread em um estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-128">A creation flag that enables you to create the thread in a suspended state.</span></span> <span data-ttu-id="b3fa9-129">Quando suspenso, o thread não é executado até que a função [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) seja chamada.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-129">When suspended, the thread does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function is called.</span></span>

<span data-ttu-id="b3fa9-130">Você também pode criar um thread chamando a função [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) .</span><span class="sxs-lookup"><span data-stu-id="b3fa9-130">You can also create a thread by calling the [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) function.</span></span> <span data-ttu-id="b3fa9-131">Essa função é usada pelos processos do depurador para criar um thread que é executado no espaço de endereço do processo que está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="b3fa9-131">This function is used by debugger processes to create a thread that runs in the address space of the process being debugged.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3fa9-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3fa9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3fa9-133">Finalizando um thread</span><span class="sxs-lookup"><span data-stu-id="b3fa9-133">Terminating a Thread</span></span>](terminating-a-thread.md)
</dt> </dl>

 

 
