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
# <a name="traversing-the-heap-list"></a>Atravessando a lista de heaps

O exemplo a seguir obtém uma lista de heaps para o processo atual. Ele tira um instantâneo dos heaps usando a função [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) e, em seguida, percorre a lista usando as funções [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) e [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . Para cada heap, ele usa as funções [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) para percorrer os blocos de heap.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) são ineficientes, especialmente para grandes heaps. No entanto, eles são úteis para consultar outros processos em que você normalmente precisa injetar um thread no outro processo para coletar as informações (essas APIs fazem isso para você).

Veja o segundo exemplo de uma alternativa equivalente, muito mais eficiente, que usa [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) em vez de [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next). Observe que [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) só pode ser usado para o mesmo processo.

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

O trecho de código a seguir usa a função [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) para movimentar os heaps de processo, produzindo uma saída idêntica ao exemplo anterior, mas com muito mais eficiência:

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

A movimentação de um heap com a função [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) é aproximadamente linear no tamanho do heap, ao passo que a movimentação de um heap com a função [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) é aproximadamente quadrática no tamanho do heap.
Mesmo para um heap modesto com alocações de 10.000, o [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) é executado 10.000 vezes mais rápido do que o [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , fornecendo informações mais detalhadas. A diferença no desempenho se torna ainda mais dramática à medida que o tamanho do heap aumenta.

Para obter um exemplo mais detalhado de como percorrer o heap com a função [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) , consulte [enumerando um heap](/windows/win32/memory/enumerating-a-heap).
