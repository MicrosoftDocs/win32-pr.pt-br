---
description: O exemplo a seguir demonstra como a função de ponto de entrada de DLL pode usar um objeto de mapeamento de arquivo para configurar a memória que pode ser compartilhada por processos que carregam a DLL.
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: Usando memória compartilhada em uma biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827516"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>Usando memória compartilhada em uma biblioteca de Dynamic-Link

O exemplo a seguir demonstra como a função de ponto de entrada de DLL pode usar um objeto de mapeamento de arquivo para configurar a memória que pode ser compartilhada por processos que carregam a DLL. A memória da DLL compartilhada persiste somente enquanto a DLL é carregada. Os aplicativos podem usar as funções SetSharedMem e GetSharedMem para acessar a memória compartilhada.

## <a name="dll-that-implements-the-shared-memory"></a>DLL que implementa a memória compartilhada

O exemplo usa mapeamento de arquivo para mapear um bloco de memória compartilhada nomeada para o espaço de endereço virtual de cada processo que carrega a DLL. Para fazer isso, a função de ponto de entrada deve:

1.  Chame a função [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) para obter um identificador para um objeto de mapeamento de arquivo. O primeiro processo que carrega a DLL cria o objeto de mapeamento de arquivo. Os processos subsequentes abrem um identificador para o objeto existente. Para obter mais informações, consulte [criando um objeto de File-Mapping](/windows/desktop/Memory/creating-a-file-mapping-object).
2.  Chame a função [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) para mapear uma exibição para o espaço de endereço virtual. Isso permite que o processo acesse a memória compartilhada. Para obter mais informações, consulte [criando uma exibição de arquivo](/windows/desktop/Memory/creating-a-file-view).

Observe que, embora você possa especificar atributos de segurança padrão passando um valor nulo para o parâmetro *lpAttributes* de [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), você pode optar por usar uma estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) para fornecer segurança adicional.


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



A memória compartilhada pode ser mapeada para um endereço diferente em cada processo. Por esse motivo, cada processo tem sua própria instância de lpvMem, que é declarada como uma variável global para que ela fique disponível para todas as funções de DLL. O exemplo supõe que os dados globais de DLL não são compartilhados, portanto, cada processo que carrega a DLL tem sua própria instância de lpvMem.

Observe que a memória compartilhada é liberada quando o último identificador para o objeto de mapeamento de arquivos é fechado. Para criar uma memória compartilhada persistente, você precisaria garantir que algum processo sempre tenha um identificador aberto para o objeto de mapeamento de arquivo.

## <a name="processes-that-use-the-shared-memory"></a>Processos que usam a memória compartilhada

Os processos a seguir usam a memória compartilhada fornecida pela DLL definida acima. O primeiro processo chama SetSharedMem para gravar uma cadeia de caracteres enquanto o segundo processo chama GetSharedMem para recuperar essa cadeia de caracteres.

Esse processo usa a função SetSharedMem implementada pela DLL para gravar a cadeia de caracteres "esta é uma cadeia de caracteres de teste" para a memória compartilhada. Ele também inicia um processo filho que lerá a cadeia de caracteres da memória compartilhada.


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



Esse processo usa a função GetSharedMem implementada pela DLL para ler uma cadeia de caracteres da memória compartilhada. Ele é iniciado pelo processo pai acima.


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dados da biblioteca de vínculo dinâmico](dynamic-link-library-data.md)
</dt> </dl>

 

 
