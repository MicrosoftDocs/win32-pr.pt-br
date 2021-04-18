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
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Usando o armazenamento local de threads em uma biblioteca de Dynamic-Link

Esta seção mostra o uso de uma função de ponto de entrada de DLL para configurar um índice de armazenamento local de thread (TLS) para fornecer armazenamento privado para cada thread de um processo multi-threaded.

O índice TLS é armazenado em uma variável global, tornando-o disponível para todas as funções de DLL. Este exemplo pressupõe que os dados globais da DLL não são compartilhados, pois o índice TLS não é necessariamente o mesmo para cada processo que carrega a DLL.

A função de ponto de entrada usa a função [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para alocar um índice TLS sempre que um processo carrega a dll. Cada thread pode usar esse índice para armazenar um ponteiro para seu próprio bloco de memória.

Quando a função de ponto de entrada é chamada com o \_ valor de anexação do processo de dll \_ , o código executa as seguintes ações:

1.  Usa a função [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para alocar um índice TLS.
2.  Aloca um bloco de memória a ser usado exclusivamente pelo thread inicial do processo.
3.  Usa o índice TLS em uma chamada para a função [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) para armazenar o endereço do bloco de memória no slot TLS associado ao índice.

Cada vez que o processo cria um novo thread, a função de ponto de entrada é chamada com o \_ valor de anexação de thread de dll \_ . A função de ponto de entrada aloca um bloco de memória para o novo thread e armazena um ponteiro para ele usando o índice TLS.

Quando uma função requer acesso aos dados associados a um índice TLS, especifique o índice em uma chamada para a função [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) . Isso recupera o conteúdo do slot TLS para o thread de chamada, que nesse caso é um ponteiro para o bloco de memória para os dados. Quando um processo usa a vinculação de tempo de carga com essa DLL, a função de ponto de entrada é suficiente para gerenciar o armazenamento local de thread. Podem ocorrer problemas com um processo que usa a vinculação de tempo de execução, pois a função de ponto de entrada não é chamada para threads existentes antes que a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) seja chamada, portanto, a memória TLS não é alocada para esses threads. Este exemplo resolve esse problema verificando o valor retornado pela função [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) e Alocando memória se o valor indicar que o slot TLS para esse thread não está definido.

Quando cada thread não precisa mais usar um índice TLS, ele deve liberar a memória cujo ponteiro é armazenado no slot TLS. Quando todos os threads tiverem terminado de usar um índice TLS, use a função [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar o índice.

Quando um thread é encerrado, a função de ponto de entrada é chamada com \_ o \_ valor de desanexação de thread de dll e a memória para esse thread é liberada. Quando um processo é encerrado, a função de ponto de entrada é chamada com \_ o \_ valor de desanexação do processo de dll e a memória referenciada pelo ponteiro no índice TLS é liberada.


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



O código a seguir demonstra o uso das funções de DLL definidas no exemplo anterior.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dados da biblioteca de vínculo dinâmico](dynamic-link-library-data.md)
</dt> <dt>

[Uso de armazenamento local de thread](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
