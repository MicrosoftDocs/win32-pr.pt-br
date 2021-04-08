---
description: Este exemplo ilustra o uso da função GetProcessHeaps para recuperar identificadores para o heap de processo padrão e quaisquer heaps privados que estejam ativos para o processo atual.
ms.assetid: 00f69593-f03b-4f30-aeec-db3fda0ac356
title: Obtendo heaps de processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caffc8dcc69b02ab671b379dbb5e133e65f8d448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921649"
---
# <a name="getting-process-heaps"></a><span data-ttu-id="0feae-103">Obtendo heaps de processo</span><span class="sxs-lookup"><span data-stu-id="0feae-103">Getting Process Heaps</span></span>

<span data-ttu-id="0feae-104">Este exemplo ilustra o uso da função [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) para recuperar identificadores para o heap de processo padrão e quaisquer heaps privados que estejam ativos para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="0feae-104">This example illustrates the use of the [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) function to retrieve handles to the default process heap and any private heaps that are active for the current process.</span></span>

<span data-ttu-id="0feae-105">O exemplo chama [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) duas vezes, primeiro para calcular o tamanho do buffer necessário e novamente para recuperar identificadores no buffer.</span><span class="sxs-lookup"><span data-stu-id="0feae-105">The example calls [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) twice, first to calculate the size of the buffer needed and again to retrieve handles into the buffer.</span></span> <span data-ttu-id="0feae-106">O buffer é alocado a partir do heap de processo padrão, usando o identificador retornado por [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap).</span><span class="sxs-lookup"><span data-stu-id="0feae-106">The buffer is allocated from the default process heap, using the handle returned by [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap).</span></span> <span data-ttu-id="0feae-107">O exemplo imprime o endereço inicial de cada heap para o console.</span><span class="sxs-lookup"><span data-stu-id="0feae-107">The example prints the starting address of each heap to the console.</span></span> <span data-ttu-id="0feae-108">Em seguida, ele usa a função [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) para liberar memória alocada para o buffer.</span><span class="sxs-lookup"><span data-stu-id="0feae-108">It then uses the [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) function to free memory allocated for the buffer.</span></span>

<span data-ttu-id="0feae-109">O número de heaps em um processo pode variar.</span><span class="sxs-lookup"><span data-stu-id="0feae-109">The number of heaps in a process may vary.</span></span> <span data-ttu-id="0feae-110">Um processo sempre tem pelo menos um heap — o heap de processo padrão — e ele pode ter um ou mais heaps privados criados pelo aplicativo ou DLLs que são carregados no espaço de endereço do processo.</span><span class="sxs-lookup"><span data-stu-id="0feae-110">A process always has at least one heap—the default process heap—and it may have one or more private heaps created by the application or by DLLs that are loaded into the address space of the process.</span></span>

<span data-ttu-id="0feae-111">Observe que um aplicativo deve chamar funções de heap somente em seu heap de processo padrão ou em heaps particulares que o aplicativo criou; chamar funções de heap em um heap privado de propriedade de outro componente pode causar um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="0feae-111">Note that an application should call heap functions only on its default process heap or on private heaps that the application has created; calling heap functions on a private heap owned by another component may cause undefined behavior.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <intsafe.h>

int __cdecl _tmain()
{
    DWORD NumberOfHeaps;
    DWORD HeapsIndex;
    DWORD HeapsLength;
    HANDLE hDefaultProcessHeap;
    HRESULT Result;
    PHANDLE aHeaps;
    SIZE_T BytesToAllocate;

    //
    // Retrieve the number of active heaps for the current process
    // so we can calculate the buffer size needed for the heap handles.
    //
    NumberOfHeaps = GetProcessHeaps(0, NULL);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve the number of heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Calculate the buffer size.
    //
    Result = SIZETMult(NumberOfHeaps, sizeof(*aHeaps), &BytesToAllocate);
    if (Result != S_OK) {
        _tprintf(TEXT("SIZETMult failed with HR %d.\n"), Result);
        return 1;
    }

    //
    // Get a handle to the default process heap.
    //
    hDefaultProcessHeap = GetProcessHeap();
    if (hDefaultProcessHeap == NULL) {
        _tprintf(TEXT("Failed to retrieve the default process heap with LastError %d.\n"),
                 GetLastError());
        return 1;
    }

    //
    // Allocate the buffer from the default process heap.
    //
    aHeaps = (PHANDLE)HeapAlloc(hDefaultProcessHeap, 0, BytesToAllocate);
    if (aHeaps == NULL) {
        _tprintf(TEXT("HeapAlloc failed to allocate %d bytes.\n"),
                 BytesToAllocate);
        return 1;
    }

    // 
    // Save the original number of heaps because we are going to compare it
    // to the return value of the next GetProcessHeaps call.
    //
    HeapsLength = NumberOfHeaps;

    //
    // Retrieve handles to the process heaps and print them to stdout. 
    // Note that heap functions should be called only on the default heap of the process
    // or on private heaps that your component creates by calling HeapCreate.
    //
    NumberOfHeaps = GetProcessHeaps(HeapsLength, aHeaps);
    if (NumberOfHeaps == 0) {
        _tprintf(TEXT("Failed to retrieve heaps with LastError %d.\n"),
                 GetLastError());
        return 1;
    }
    else if (NumberOfHeaps > HeapsLength) {

        //
        // Compare the latest number of heaps with the original number of heaps.
        // If the latest number is larger than the original number, another
        // component has created a new heap and the buffer is too small.
        //
        _tprintf(TEXT("Another component created a heap between calls. ") \
                 TEXT("Please try again.\n"));
        return 1;
    }

    _tprintf(TEXT("Process has %d heaps.\n"), HeapsLength);
    for (HeapsIndex = 0; HeapsIndex < HeapsLength; ++HeapsIndex) {
        _tprintf(TEXT("Heap %d at address: %#p.\n"),
                 HeapsIndex,
                 aHeaps[HeapsIndex]);
    }
  
    //
    // Release memory allocated from default process heap.
    //
    if (HeapFree(hDefaultProcessHeap, 0, aHeaps) == FALSE) {
        _tprintf(TEXT("Failed to free allocation from default process heap.\n"));
    }

    return 0;
}
```



 

 



