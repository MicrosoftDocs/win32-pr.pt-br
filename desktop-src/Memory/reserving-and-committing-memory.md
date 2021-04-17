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
# <a name="reserving-and-committing-memory"></a><span data-ttu-id="7839e-103">Reservando e confirmando memória</span><span class="sxs-lookup"><span data-stu-id="7839e-103">Reserving and Committing Memory</span></span>

<span data-ttu-id="7839e-104">O exemplo a seguir ilustra o uso das funções do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e do [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) no reservando e confirmando a memória conforme necessário para uma matriz dinâmica.</span><span class="sxs-lookup"><span data-stu-id="7839e-104">The following example illustrates the use of the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) and [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) functions in reserving and committing memory as needed for a dynamic array.</span></span> <span data-ttu-id="7839e-105">Primeiro, o **VirtualAlloc** é chamado para reservar um bloco de páginas com **NULL** especificado como o parâmetro de endereço base, forçando o sistema a determinar o local do bloco.</span><span class="sxs-lookup"><span data-stu-id="7839e-105">First, **VirtualAlloc** is called to reserve a block of pages with **NULL** specified as the base address parameter, forcing the system to determine the location of the block.</span></span> <span data-ttu-id="7839e-106">Posteriormente, o **VirtualAlloc** é chamado sempre que for necessário confirmar uma página dessa região reservada e o endereço base da próxima página a ser confirmada for especificado.</span><span class="sxs-lookup"><span data-stu-id="7839e-106">Later, **VirtualAlloc** is called whenever it is necessary to commit a page from this reserved region, and the base address of the next page to be committed is specified.</span></span>

<span data-ttu-id="7839e-107">O exemplo usa a sintaxe de manipulação de exceção estruturada para confirmar páginas da região reservada.</span><span class="sxs-lookup"><span data-stu-id="7839e-107">The example uses structured exception-handling syntax to commit pages from the reserved region.</span></span> <span data-ttu-id="7839e-108">Sempre que ocorre uma exceção de falha de página durante a execução do bloco **\_ \_ try** , a função Filter na expressão que antecede o bloco **\_ \_ Except** é executada.</span><span class="sxs-lookup"><span data-stu-id="7839e-108">Whenever a page fault exception occurs during the execution of the **\_\_try** block, the filter function in the expression preceding the **\_\_except** block is executed.</span></span> <span data-ttu-id="7839e-109">Se a função de filtro puder alocar outra página, a execução continuará no bloco **\_ \_ try** no ponto em que a exceção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7839e-109">If the filter function can allocate another page, execution continues in the **\_\_try** block at the point where the exception occurred.</span></span> <span data-ttu-id="7839e-110">Caso contrário, o manipulador de exceção no bloco **\_ \_ Except** será executado.</span><span class="sxs-lookup"><span data-stu-id="7839e-110">Otherwise, the exception handler in the **\_\_except** block is executed.</span></span> <span data-ttu-id="7839e-111">Para obter mais informações, consulte [manipulação de exceção estruturada](../debug/structured-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7839e-111">For more information, see [Structured Exception Handling](../debug/structured-exception-handling.md).</span></span>

<span data-ttu-id="7839e-112">Como uma alternativa à alocação dinâmica, o processo pode simplesmente confirmar a região inteira, em vez de apenas reservá-la.</span><span class="sxs-lookup"><span data-stu-id="7839e-112">As an alternative to dynamic allocation, the process can simply commit the entire region instead of only reserving it.</span></span> <span data-ttu-id="7839e-113">Ambos os métodos resultam no mesmo uso de memória física porque as páginas confirmadas não consomem nenhum armazenamento físico até serem acessadas pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="7839e-113">Both methods result in the same physical memory usage because committed pages do not consume any physical storage until they are first accessed.</span></span> <span data-ttu-id="7839e-114">A vantagem da alocação dinâmica é que ela minimiza o número total de páginas confirmadas no sistema.</span><span class="sxs-lookup"><span data-stu-id="7839e-114">The advantage of dynamic allocation is that it minimizes the total number of committed pages on the system.</span></span> <span data-ttu-id="7839e-115">Para alocações muito grandes, a confirmação de uma alocação inteira pode fazer com que o sistema fique sem páginas confirmadas, resultando em falhas de alocação de memória virtual.</span><span class="sxs-lookup"><span data-stu-id="7839e-115">For very large allocations, pre-committing an entire allocation can cause the system to run out of committable pages, resulting in virtual memory allocation failures.</span></span>

<span data-ttu-id="7839e-116">A função [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) no bloco **\_ \_ Except** libera automaticamente as alocações de memória virtual, portanto, não é necessário liberar explicitamente as páginas quando o programa termina nesse caminho de execução.</span><span class="sxs-lookup"><span data-stu-id="7839e-116">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function in the **\_\_except** block automatically releases virtual memory allocations, so it is not necessary to explicitly free the pages when the program terminates through this execution path.</span></span> <span data-ttu-id="7839e-117">A função [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libera as páginas reservadas e confirmadas se o programa for criado com a manipulação de exceção desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7839e-117">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function frees the reserved and committed pages if the program is built with exception handling disabled.</span></span> <span data-ttu-id="7839e-118">Essa função usa **a \_ liberação mem** para desconfirmar e liberar toda a região de páginas reservadas e confirmadas.</span><span class="sxs-lookup"><span data-stu-id="7839e-118">This function uses **MEM\_RELEASE** to decommit and release the entire region of reserved and committed pages.</span></span>

<span data-ttu-id="7839e-119">O exemplo de C++ a seguir demonstra a alocação de memória dinâmica usando um manipulador de exceção estruturado.</span><span class="sxs-lookup"><span data-stu-id="7839e-119">The following C++ example demonstrates dynamic memory allocation using a structured exception handler.</span></span>


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



 

 
