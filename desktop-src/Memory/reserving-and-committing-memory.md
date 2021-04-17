---
description: O exemplo a seguir ilustra o uso das funções do VirtualAlloc e do VirtualFree no reservando e confirmando a memória conforme necessário para uma matriz dinâmica.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Reservando e confirmando memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782796"
---
# <a name="reserving-and-committing-memory"></a>Reservando e confirmando memória

O exemplo a seguir ilustra o uso das funções do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e do [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) no reservando e confirmando a memória conforme necessário para uma matriz dinâmica. Primeiro, o **VirtualAlloc** é chamado para reservar um bloco de páginas com **NULL** especificado como o parâmetro de endereço base, forçando o sistema a determinar o local do bloco. Posteriormente, o **VirtualAlloc** é chamado sempre que for necessário confirmar uma página dessa região reservada e o endereço base da próxima página a ser confirmada for especificado.

O exemplo usa a sintaxe de manipulação de exceção estruturada para confirmar páginas da região reservada. Sempre que ocorre uma exceção de falha de página durante a execução do bloco **\_ \_ try** , a função Filter na expressão que antecede o bloco **\_ \_ Except** é executada. Se a função de filtro puder alocar outra página, a execução continuará no bloco **\_ \_ try** no ponto em que a exceção ocorreu. Caso contrário, o manipulador de exceção no bloco **\_ \_ Except** será executado. Para obter mais informações, consulte [manipulação de exceção estruturada](../debug/structured-exception-handling.md).

Como uma alternativa à alocação dinâmica, o processo pode simplesmente confirmar a região inteira, em vez de apenas reservá-la. Ambos os métodos resultam no mesmo uso de memória física porque as páginas confirmadas não consomem nenhum armazenamento físico até serem acessadas pela primeira vez. A vantagem da alocação dinâmica é que ela minimiza o número total de páginas confirmadas no sistema. Para alocações muito grandes, a confirmação de uma alocação inteira pode fazer com que o sistema fique sem páginas confirmadas, resultando em falhas de alocação de memória virtual.

A função [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) no bloco **\_ \_ Except** libera automaticamente as alocações de memória virtual, portanto, não é necessário liberar explicitamente as páginas quando o programa termina nesse caminho de execução. A função [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libera as páginas reservadas e confirmadas se o programa for criado com a manipulação de exceção desabilitada. Essa função usa **a \_ liberação mem** para desconfirmar e liberar toda a região de páginas reservadas e confirmadas.

O exemplo de C++ a seguir demonstra a alocação de memória dinâmica usando um manipulador de exceção estruturado.


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



 

 
