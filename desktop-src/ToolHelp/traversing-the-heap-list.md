---
title: Atravessando a lista de heaps
description: O exemplo a seguir obtém uma lista de heaps para o processo atual.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25179ab78f59c111d41849bda28184fcbfa7f612
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005827"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="1882c-103">Atravessando a lista de heaps</span><span class="sxs-lookup"><span data-stu-id="1882c-103">Traversing the Heap List</span></span>

<span data-ttu-id="1882c-104">O exemplo a seguir obtém uma lista de heaps para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="1882c-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="1882c-105">Ele tira um instantâneo dos heaps usando a função [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e, em seguida, percorre a lista usando as funções [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) e [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) .</span><span class="sxs-lookup"><span data-stu-id="1882c-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="1882c-106">Para cada heap, ele usa as funções [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) para percorrer os blocos de heap.</span><span class="sxs-lookup"><span data-stu-id="1882c-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>


```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```



 

 




