---
description: O exemplo a seguir ilustra o uso da função HeapWalk para enumerar um heap.
ms.assetid: ef37d644-473f-4e51-9785-5b44fe0dce42
title: Enumerando um heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ad6ea7e23f480b4d4e27885d296f1be1632053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754363"
---
# <a name="enumerating-a-heap"></a>Enumerando um heap

O exemplo a seguir ilustra o uso da função [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) para enumerar um heap.

Primeiro, o exemplo cria um heap privado com a função [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) . Em seguida, ele usa [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) para bloquear o heap para que outros threads não possam acessar o heap enquanto ele está sendo enumerado. Em seguida, o exemplo chama [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) com um ponteiro para uma estrutura de [**entrada de \_ heap \_ de processo**](/windows/win32/api/minwinbase/ns-minwinbase-process_heap_entry) e itera através do heap, imprimindo cada entrada para o console.

Após a conclusão da enumeração, o exemplo usa [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) para desbloquear o heap para que outros threads possam acessá-lo. Por fim, o exemplo chama [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) para destruir o heap privado.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain()
{
    DWORD LastError;
    HANDLE hHeap;
    PROCESS_HEAP_ENTRY Entry;

    //
    // Create a new heap with default parameters.
    //
    hHeap = HeapCreate(0, 0, 0);
    if (hHeap == NULL) {
        _tprintf(TEXT("Failed to create a new heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Lock the heap to prevent other threads from accessing the heap 
    // during enumeration.
    //
    if (HeapLock(hHeap) == FALSE) {
        _tprintf(TEXT("Failed to lock heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    _tprintf(TEXT("Walking heap %#p...\n\n"), hHeap);

    Entry.lpData = NULL;
    while (HeapWalk(hHeap, &Entry) != FALSE) {
        if ((Entry.wFlags & PROCESS_HEAP_ENTRY_BUSY) != 0) {
            _tprintf(TEXT("Allocated block"));

            if ((Entry.wFlags & PROCESS_HEAP_ENTRY_MOVEABLE) != 0) {
                _tprintf(TEXT(", movable with HANDLE %#p"), Entry.Block.hMem);
            }

            if ((Entry.wFlags & PROCESS_HEAP_ENTRY_DDESHARE) != 0) {
                _tprintf(TEXT(", DDESHARE"));
            }
        }
        else if ((Entry.wFlags & PROCESS_HEAP_REGION) != 0) {
            _tprintf(TEXT("Region\n  %d bytes committed\n") \
                     TEXT("  %d bytes uncommitted\n  First block address: %#p\n") \
                     TEXT("  Last block address: %#p\n"),
                     Entry.Region.dwCommittedSize,
                     Entry.Region.dwUnCommittedSize,
                     Entry.Region.lpFirstBlock,
                     Entry.Region.lpLastBlock);
        }
        else if ((Entry.wFlags & PROCESS_HEAP_UNCOMMITTED_RANGE) != 0) {
            _tprintf(TEXT("Uncommitted range\n"));
        }
        else {
            _tprintf(TEXT("Block\n"));
        }

        _tprintf(TEXT("  Data portion begins at: %#p\n  Size: %d bytes\n") \
                 TEXT("  Overhead: %d bytes\n  Region index: %d\n\n"),
                 Entry.lpData,
                 Entry.cbData,
                 Entry.cbOverhead,
                 Entry.iRegionIndex);
    }
    LastError = GetLastError();
    if (LastError != ERROR_NO_MORE_ITEMS) {
        _tprintf(TEXT("HeapWalk failed with LastError %d.\n"), LastError);
    }

    //
    // Unlock the heap to allow other threads to access the heap after 
    // enumeration has completed.
    //
    if (HeapUnlock(hHeap) == FALSE) {
        _tprintf(TEXT("Failed to unlock heap with LastError %d.\n"),
                 GetLastError());
    }

    //
    // When a process terminates, allocated memory is reclaimed by the operating
    // system so it is not really necessary to call HeapDestroy in this example.
    // However, it may be advisable to call HeapDestroy in a longer running
    // application.
    //
    if (HeapDestroy(hHeap) == FALSE) {
        _tprintf(TEXT("Failed to destroy heap with LastError %d.\n"),
                 GetLastError());
    }

    return 0;
}
```



A saída a seguir mostra resultados típicos para um heap recém-criado.

``` syntax
Walking heap 0X00530000...

Region
  4096 bytes committed
  258048 bytes uncommitted
  First block address: 0X00530598
  Last block address: 0X00570000
  Data portion begins at: 0X00530000
  Size: 1416 bytes
  Overhead: 0 bytes
  Region index: 0

Block
  Data portion begins at: 0X005307D8
  Size: 2056 bytes
  Overhead: 16 bytes
  Region index: 0

Uncommitted range
  Data portion begins at: 0X00531000
  Size: 258048 bytes
  Overhead: 0 bytes
  Region index: 0
```

 

 
