---
description: O armazenamento local de thread (TLS) permite que vários threads do mesmo processo usem um índice alocado pela função TlsAlloc para armazenar e recuperar um valor que seja local para o thread.
ms.assetid: b7f5a206-a827-4b6b-86f6-5e3aea1246b7
title: Uso de armazenamento local de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9221d4d0d68891ab8e2d0f2462b7c0aae307c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812880"
---
# <a name="using-thread-local-storage"></a><span data-ttu-id="0368f-103">Uso de armazenamento local de thread</span><span class="sxs-lookup"><span data-stu-id="0368f-103">Using Thread Local Storage</span></span>

<span data-ttu-id="0368f-104">O [armazenamento local de thread](thread-local-storage.md) (TLS) permite que vários threads do mesmo processo usem um índice alocado pela função [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para armazenar e recuperar um valor que seja local para o thread.</span><span class="sxs-lookup"><span data-stu-id="0368f-104">[Thread local storage](thread-local-storage.md) (TLS) enables multiple threads of the same process to use an index allocated by the [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to store and retrieve a value that is local to the thread.</span></span> <span data-ttu-id="0368f-105">Neste exemplo, um índice é alocado quando o processo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0368f-105">In this example, an index is allocated when the process starts.</span></span> <span data-ttu-id="0368f-106">Quando cada thread é iniciado, ele aloca um bloco de memória dinâmica e armazena um ponteiro para essa memória no slot TLS usando a função [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) .</span><span class="sxs-lookup"><span data-stu-id="0368f-106">When each thread starts, it allocates a block of dynamic memory and stores a pointer to this memory in the TLS slot using the [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function.</span></span> <span data-ttu-id="0368f-107">A função CommonFunc usa a função [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) para acessar os dados associados ao índice que é local para o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="0368f-107">The CommonFunc function uses the [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function to access the data associated with the index that is local to the calling thread.</span></span> <span data-ttu-id="0368f-108">Antes que cada thread seja encerrado, ele libera sua memória dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0368f-108">Before each thread terminates, it releases its dynamic memory.</span></span> <span data-ttu-id="0368f-109">Antes que o processo seja encerrado, ele chama [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar o índice.</span><span class="sxs-lookup"><span data-stu-id="0368f-109">Before the process terminates, it calls [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree) to release the index.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
DWORD dwTlsIndex; 
 
VOID ErrorExit (LPCSTR message);
 
VOID CommonFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Retrieve a data pointer for the current thread. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if ((lpvData == 0) && (GetLastError() != ERROR_SUCCESS)) 
      ErrorExit("TlsGetValue error"); 
 
// Use the data stored for the current thread. 
 
   printf("common: thread %d: lpvData=%lx\n", 
      GetCurrentThreadId(), lpvData); 
 
   Sleep(5000); 
} 
 
DWORD WINAPI ThreadFunc(VOID) 
{ 
   LPVOID lpvData; 
 
// Initialize the TLS index for this thread. 
 
   lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
   if (! TlsSetValue(dwTlsIndex, lpvData)) 
      ErrorExit("TlsSetValue error"); 
 
   printf("thread %d: lpvData=%lx\n", GetCurrentThreadId(), lpvData); 
 
   CommonFunc(); 
 
// Release the dynamic memory before the thread returns. 
 
   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData != 0) 
      LocalFree((HLOCAL) lpvData); 
 
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
 
// Allocate a TLS index. 
 
   if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
      ErrorExit("TlsAlloc failed"); 
 
// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   for (i = 0; i < THREADCOUNT; i++) 
      WaitForSingleObject(hThread[i], INFINITE); 
 
   TlsFree(dwTlsIndex);

   return 0; 
} 
 
VOID ErrorExit (LPCSTR message)
{ 
   fprintf(stderr, "%s\n", message); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="0368f-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0368f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0368f-111">Usando o armazenamento local de threads em uma biblioteca de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="0368f-111">Using Thread Local Storage in a Dynamic-Link Library</span></span>](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
