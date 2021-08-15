---
description: O exemplo a seguir ilustra o uso das funções VirtualAlloc e VirtualFree na reserva e confirmação de memória conforme necessário para uma matriz dinâmica.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Reservando e comando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615f3c4321dc432b5ef83a841cea12215563e7d103443512a4d3b2c553849540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386274"
---
# <a name="reserving-and-committing-memory"></a>Reservando e comando memória

O exemplo a seguir ilustra o uso das funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) na reserva e confirmação de memória conforme necessário para uma matriz dinâmica. Primeiro, **VirtualAlloc** é chamado para reservar um bloco de páginas com **NULL** especificado como o parâmetro de endereço base, forçando o sistema a determinar o local do bloco. Posteriormente, **VirtualAlloc** é chamado sempre que é necessário fazer commit de uma página dessa região reservada e o endereço base da próxima página a ser confirmado é especificado.

O exemplo usa a sintaxe estruturada de tratamento de exceções para fazer commit de páginas da região reservada. Sempre que ocorre uma exceção de falha de página durante a execução do bloco **\_ \_ try,** a função de filtro na expressão anterior ao bloco **\_ \_ except** é executada. Se a função de filtro puder alocar outra página, a execução continuará no **\_ \_ bloco try** no ponto em que a exceção ocorreu. Caso contrário, o manipulador de exceção no **\_ \_ bloco except** será executado. Para obter mais informações, consulte [Tratamento de exceções estruturadas.](../debug/structured-exception-handling.md)

Como alternativa à alocação dinâmica, o processo pode simplesmente fazer commit de toda a região em vez de apenas reservá-la. Ambos os métodos resultam no mesmo uso de memória física porque as páginas comprometidas não consomem nenhum armazenamento físico até que sejam acessadas pela primeira vez. A vantagem da alocação dinâmica é que ela minimiza o número total de páginas comprometidas no sistema. Para alocações muito grandes, a pré-confirmação de uma alocação inteira pode fazer com que o sistema fique sem páginas committable, resultando em falhas de alocação de memória virtual.

A [**função ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) no bloco except libera automaticamente as alocações de memória virtual, portanto, não é necessário liberar explicitamente as páginas quando o programa terminar por meio desse caminho de execução. **\_ \_** A [**função VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) liberará as páginas reservadas e comprometidas se o programa for criado com o tratamento de exceção desabilitado. Essa função usa **MEM \_ RELEASE** para delimitar e liberar toda a região de páginas reservadas e comprometidas.

O exemplo C++ a seguir demonstra a alocação de memória dinâmica usando um manipulador de exceção estruturado.


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
