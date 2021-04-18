---
description: Uma página de proteção fornece um alarme único para acesso à página de memória.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Criando páginas de proteção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778423"
---
# <a name="creating-guard-pages"></a><span data-ttu-id="00a7b-103">Criando páginas de proteção</span><span class="sxs-lookup"><span data-stu-id="00a7b-103">Creating Guard Pages</span></span>

<span data-ttu-id="00a7b-104">Uma página de proteção fornece um alarme único para acesso à página de memória.</span><span class="sxs-lookup"><span data-stu-id="00a7b-104">A guard page provides a one-shot alarm for memory page access.</span></span> <span data-ttu-id="00a7b-105">Isso pode ser útil para um aplicativo que precisa monitorar o crescimento de grandes estruturas de dados dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="00a7b-105">This can be useful for an application that needs to monitor the growth of large dynamic data structures.</span></span> <span data-ttu-id="00a7b-106">Por exemplo, há sistemas operacionais que usam páginas de proteção para implementar a verificação automática de pilha.</span><span class="sxs-lookup"><span data-stu-id="00a7b-106">For example, there are operating systems that use guard pages to implement automatic stack checking.</span></span>

<span data-ttu-id="00a7b-107">Para criar uma página de proteção, defina o modificador proteção de página do **Page \_ Guard** para a página.</span><span class="sxs-lookup"><span data-stu-id="00a7b-107">To create a guard page, set the **PAGE\_GUARD** page protection modifier for the page.</span></span> <span data-ttu-id="00a7b-108">Esse valor pode ser especificado, juntamente com outros modificadores de proteção de página, nas funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)e [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) .</span><span class="sxs-lookup"><span data-stu-id="00a7b-108">This value can be specified, along with other page protection modifiers, in the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect), and [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) functions.</span></span> <span data-ttu-id="00a7b-109">O modificador de página pode ser usado com qualquer outro modificador de proteção de página, exceto a **página \_ NoAccess**. **\_**</span><span class="sxs-lookup"><span data-stu-id="00a7b-109">The **PAGE\_GUARD** modifier can be used with any other page protection modifiers, except **PAGE\_NOACCESS**.</span></span>

<span data-ttu-id="00a7b-110">Se um programa tentar acessar um endereço dentro de uma página de proteção, o sistema gerará uma exceção de violação de página de proteção de status (0x80000001). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00a7b-110">If a program attempts to access an address within a guard page, the system raises a **STATUS\_GUARD\_PAGE\_VIOLATION** (0x80000001) exception.</span></span> <span data-ttu-id="00a7b-111">O sistema também limpa o modificador de **\_ proteção de página** , removendo o status da página de proteção da página de memória.</span><span class="sxs-lookup"><span data-stu-id="00a7b-111">The system also clears the **PAGE\_GUARD** modifier, removing the memory page's guard page status.</span></span> <span data-ttu-id="00a7b-112">O sistema não irá parar a próxima tentativa de acessar a página de memória com uma exceção de **violação de página de proteção de status \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="00a7b-112">The system will not stop the next attempt to access the memory page with a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span>

<span data-ttu-id="00a7b-113">Se ocorrer uma exceção de página de proteção durante um serviço do sistema, o serviço falhará e normalmente retornará algum indicador de status de falha.</span><span class="sxs-lookup"><span data-stu-id="00a7b-113">If a guard page exception occurs during a system service, the service fails and typically returns some failure status indicator.</span></span> <span data-ttu-id="00a7b-114">Como o sistema também remove o status da página de proteção da página de memória relevante, a próxima invocação do mesmo serviço do sistema não falhará devido a uma exceção de **violação de página do status de \_ \_ \_ proteção** (a menos que, é claro, alguém restabeleça a página de proteção).</span><span class="sxs-lookup"><span data-stu-id="00a7b-114">Since the system also removes the relevant memory page's guard page status, the next invocation of the same system service won't fail due to a **STATUS\_GUARD\_PAGE\_VIOLATION** exception (unless, of course, someone reestablishes the guard page).</span></span>

<span data-ttu-id="00a7b-115">O programa curto a seguir ilustra o comportamento da proteção de página de protetor.</span><span class="sxs-lookup"><span data-stu-id="00a7b-115">The following short program illustrates the behavior of guard page protection.</span></span>


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



<span data-ttu-id="00a7b-116">A primeira tentativa de bloquear o bloco de memória falha, gerando uma exceção de **violação de página de proteção de status \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="00a7b-116">The first attempt to lock the memory block fails, raising a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span> <span data-ttu-id="00a7b-117">A segunda tentativa é realizada com sucesso, porque a proteção de página do bloco de memória foi alternada pela primeira tentativa.</span><span class="sxs-lookup"><span data-stu-id="00a7b-117">The second attempt succeeds, because the memory block's guard page protection has been toggled off by the first attempt.</span></span>

 

 
