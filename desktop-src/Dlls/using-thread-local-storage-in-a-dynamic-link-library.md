---
description: Esta seção mostra o uso de uma função de ponto de entrada de DLL para configurar um índice de armazenamento local de thread (TLS) para fornecer armazenamento privado para cada thread de um processo multi-threaded.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Usando o armazenamento local de threads em uma biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810925"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="1ebb7-103">Usando o armazenamento local de threads em uma biblioteca de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="1ebb7-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="1ebb7-104">Esta seção mostra o uso de uma função de ponto de entrada de DLL para configurar um índice de armazenamento local de thread (TLS) para fornecer armazenamento privado para cada thread de um processo multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="1ebb7-105">O índice TLS é armazenado em uma variável global, tornando-o disponível para todas as funções de DLL.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="1ebb7-106">Este exemplo pressupõe que os dados globais da DLL não são compartilhados, pois o índice TLS não é necessariamente o mesmo para cada processo que carrega a DLL.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="1ebb7-107">A função de ponto de entrada usa a função [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para alocar um índice TLS sempre que um processo carrega a dll.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="1ebb7-108">Cada thread pode usar esse índice para armazenar um ponteiro para seu próprio bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="1ebb7-109">Quando a função de ponto de entrada é chamada com o \_ valor de anexação do processo de dll \_ , o código executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="1ebb7-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="1ebb7-110">Usa a função [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para alocar um índice TLS.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="1ebb7-111">Aloca um bloco de memória a ser usado exclusivamente pelo thread inicial do processo.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="1ebb7-112">Usa o índice TLS em uma chamada para a função [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) para armazenar o endereço do bloco de memória no slot TLS associado ao índice.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="1ebb7-113">Cada vez que o processo cria um novo thread, a função de ponto de entrada é chamada com o \_ valor de anexação de thread de dll \_ .</span><span class="sxs-lookup"><span data-stu-id="1ebb7-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="1ebb7-114">A função de ponto de entrada aloca um bloco de memória para o novo thread e armazena um ponteiro para ele usando o índice TLS.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="1ebb7-115">Quando uma função requer acesso aos dados associados a um índice TLS, especifique o índice em uma chamada para a função [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) .</span><span class="sxs-lookup"><span data-stu-id="1ebb7-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="1ebb7-116">Isso recupera o conteúdo do slot TLS para o thread de chamada, que nesse caso é um ponteiro para o bloco de memória para os dados.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="1ebb7-117">Quando um processo usa a vinculação de tempo de carga com essa DLL, a função de ponto de entrada é suficiente para gerenciar o armazenamento local de thread.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="1ebb7-118">Podem ocorrer problemas com um processo que usa a vinculação de tempo de execução, pois a função de ponto de entrada não é chamada para threads existentes antes que a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) seja chamada, portanto, a memória TLS não é alocada para esses threads.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="1ebb7-119">Este exemplo resolve esse problema verificando o valor retornado pela função [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) e Alocando memória se o valor indicar que o slot TLS para esse thread não está definido.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="1ebb7-120">Quando cada thread não precisa mais usar um índice TLS, ele deve liberar a memória cujo ponteiro é armazenado no slot TLS.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="1ebb7-121">Quando todos os threads tiverem terminado de usar um índice TLS, use a função [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar o índice.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="1ebb7-122">Quando um thread é encerrado, a função de ponto de entrada é chamada com \_ o \_ valor de desanexação de thread de dll e a memória para esse thread é liberada.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="1ebb7-123">Quando um processo é encerrado, a função de ponto de entrada é chamada com \_ o \_ valor de desanexação do processo de dll e a memória referenciada pelo ponteiro no índice TLS é liberada.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



<span data-ttu-id="1ebb7-124">O código a seguir demonstra o uso das funções de DLL definidas no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

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
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="1ebb7-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ebb7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ebb7-126">Dados da biblioteca de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="1ebb7-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="1ebb7-127">Uso de armazenamento local de thread</span><span class="sxs-lookup"><span data-stu-id="1ebb7-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
