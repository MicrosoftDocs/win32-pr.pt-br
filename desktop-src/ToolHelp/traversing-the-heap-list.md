---
title: Atravessando a lista de heaps
description: Exemplos que mostram como obter uma lista de heaps para o processo atual.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994496"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="673c0-103">Atravessando a lista de heaps</span><span class="sxs-lookup"><span data-stu-id="673c0-103">Traversing the Heap List</span></span>

<span data-ttu-id="673c0-104">O exemplo a seguir obtém uma lista de heaps para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="673c0-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="673c0-105">Ele tira um instantâneo dos heaps usando a função [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e, em seguida, percorre a lista usando as funções [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) e [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) .</span><span class="sxs-lookup"><span data-stu-id="673c0-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="673c0-106">Para cada heap, ele usa as funções [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) para percorrer os blocos de heap.</span><span class="sxs-lookup"><span data-stu-id="673c0-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="673c0-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) são ineficientes, especialmente para grandes heaps.</span><span class="sxs-lookup"><span data-stu-id="673c0-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="673c0-108">No entanto, eles são úteis para consultar outros processos em que você normalmente precisa injetar um thread no outro processo para coletar as informações (essas APIs fazem isso para você).</span><span class="sxs-lookup"><span data-stu-id="673c0-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="673c0-109">Veja o segundo exemplo de uma alternativa equivalente, muito mais eficiente, que usa [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) em vez de [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span><span class="sxs-lookup"><span data-stu-id="673c0-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="673c0-110">Observe que [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) só pode ser usado para o mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="673c0-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

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

<span data-ttu-id="673c0-111">O trecho de código a seguir usa a função [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) para movimentar os heaps de processo, produzindo uma saída idêntica ao exemplo anterior, mas com muito mais eficiência:</span><span class="sxs-lookup"><span data-stu-id="673c0-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

<span data-ttu-id="673c0-112">A movimentação de um heap com a função [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) é aproximadamente linear no tamanho do heap, ao passo que a movimentação de um heap com a função [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) é aproximadamente quadrática no tamanho do heap.</span><span class="sxs-lookup"><span data-stu-id="673c0-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="673c0-113">Mesmo para um heap modesto com alocações de 10.000, o [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) é executado 10.000 vezes mais rápido do que o [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , fornecendo informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="673c0-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="673c0-114">A diferença no desempenho se torna ainda mais dramática à medida que o tamanho do heap aumenta.</span><span class="sxs-lookup"><span data-stu-id="673c0-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="673c0-115">Para obter um exemplo mais detalhado de como percorrer o heap com a função [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , consulte [enumerando um heap](/windows/win32/memory/enumerating-a-heap).</span><span class="sxs-lookup"><span data-stu-id="673c0-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
