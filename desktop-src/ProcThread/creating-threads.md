---
description: Revise como usar a função CreateThread para criar um novo thread para um processo. Examine um exemplo de código que mostra seu uso.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Criando threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dee74cb81c886fe05d07a0970f7d8946d123d92810e6f22dd094e1d8d00466a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081426"
---
# <a name="creating-threads"></a>Criando threads

A [**função CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) cria um novo thread para um processo. O thread de criação deve especificar o endereço inicial do código que o novo thread deve executar. Normalmente, o endereço inicial é o nome de uma função definida no código do programa (para obter mais informações, consulte [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))). Essa função recebe um único parâmetro e retorna um **valor DWORD.** Um processo pode ter vários threads executando simultaneamente a mesma função.

Veja a seguir um exemplo simples que demonstra como criar um novo thread que executa a função definida localmente, `MyThreadFunction` .

O thread de chamada usa a [**função WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) para persistir até que todos os threads de trabalho tenham terminado. O thread de chamada é bloco enquanto ele está aguardando; para continuar o processamento, um thread de chamada usaria [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) e aguardaria cada thread de trabalho sinalizar seu objeto de espera. Observe que, se você fechar o handle para um thread de trabalho antes de ser encerrado, isso não encerrará o thread de trabalho. No entanto, o handle não estará disponível para uso em chamadas de função subsequentes.


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



A função evita o uso da CRT (biblioteca em tempo de executar C), pois muitas de suas funções não são thread-safe, especialmente se você não estiver usando o `MyThreadFunction` CRT multithread. Se você quiser usar o CRT em uma função, use a `ThreadProc` **\_ função beginthreadex.**

É arriscado passar o endereço de uma variável local se o thread de criação sair antes do novo thread, porque o ponteiro se torna inválido. Em vez disso, passe um ponteiro para a memória alocada dinamicamente ou faça com que o thread de criação aguarde até que o novo thread seja encerrado. Os dados também podem ser passados do thread de criação para o novo thread usando variáveis globais. Com variáveis globais, geralmente é necessário sincronizar o acesso por vários threads. Para obter mais informações sobre sincronização, consulte [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).

O thread de criação pode usar os argumentos para [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para especificar o seguinte:

-   Os atributos de segurança do alça para o novo thread. Esses atributos de segurança incluem um sinalizador de herança que determina se o handle pode ser herdado por processos filho. Os atributos de segurança também incluem um descritor de segurança, que o sistema usa para executar verificações de acesso em todos os usos subsequentes do handle do thread antes que o acesso seja concedido.
-   O tamanho da pilha inicial do novo thread. A pilha do thread é alocada automaticamente no espaço de memória do processo; o sistema aumenta a pilha conforme necessário e a libera quando o thread é encerrado. Para obter mais informações, consulte [Tamanho da pilha de threads](thread-stack-size.md).
-   Um sinalizador de criação que permite que você crie o thread em um estado suspenso. Quando suspenso, o thread não é executado até que [**a função ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) seja chamada.

Você também pode criar um thread chamando a [**função CreateRemoteThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) Essa função é usada pelos processos do depurador para criar um thread que é executado no espaço de endereço do processo que está sendo depurado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Encerrando um thread](terminating-a-thread.md)
</dt> </dl>

 

 
