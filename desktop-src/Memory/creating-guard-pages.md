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
# <a name="creating-guard-pages"></a>Criando páginas de proteção

Uma página de proteção fornece um alarme único para acesso à página de memória. Isso pode ser útil para um aplicativo que precisa monitorar o crescimento de grandes estruturas de dados dinâmicos. Por exemplo, há sistemas operacionais que usam páginas de proteção para implementar a verificação automática de pilha.

Para criar uma página de proteção, defina o modificador proteção de página do **Page \_ Guard** para a página. Esse valor pode ser especificado, juntamente com outros modificadores de proteção de página, nas funções [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)e [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) . O modificador de página pode ser usado com qualquer outro modificador de proteção de página, exceto a **página \_ NoAccess**. **\_**

Se um programa tentar acessar um endereço dentro de uma página de proteção, o sistema gerará uma exceção de violação de página de proteção de status (0x80000001). **\_ \_ \_** O sistema também limpa o modificador de **\_ proteção de página** , removendo o status da página de proteção da página de memória. O sistema não irá parar a próxima tentativa de acessar a página de memória com uma exceção de **violação de página de proteção de status \_ \_ \_** .

Se ocorrer uma exceção de página de proteção durante um serviço do sistema, o serviço falhará e normalmente retornará algum indicador de status de falha. Como o sistema também remove o status da página de proteção da página de memória relevante, a próxima invocação do mesmo serviço do sistema não falhará devido a uma exceção de **violação de página do status de \_ \_ \_ proteção** (a menos que, é claro, alguém restabeleça a página de proteção).

O programa curto a seguir ilustra o comportamento da proteção de página de protetor.


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



A primeira tentativa de bloquear o bloco de memória falha, gerando uma exceção de **violação de página de proteção de status \_ \_ \_** . A segunda tentativa é realizada com sucesso, porque a proteção de página do bloco de memória foi alternada pela primeira tentativa.

 

 
