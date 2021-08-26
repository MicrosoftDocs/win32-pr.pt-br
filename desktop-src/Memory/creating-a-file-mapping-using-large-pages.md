---
description: O exemplo a seguir usa a função CreateFileMapping com o sinalizador SEC \_ LARGE PAGES para usar páginas \_ grandes. Ele requer Windows Server 2003 com Service Pack 1 (SP1) ou posterior.
ms.assetid: be2cdcbc-03e8-407d-8ae2-569f8fd8cba8
title: Criando um mapeamento de arquivo usando páginas grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df68cc483856d0fe7f329b4f5e6e5c8a424a8c0e55958ca1da8de1ce51cbf71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869936"
---
# <a name="creating-a-file-mapping-using-large-pages"></a>Criando um mapeamento de arquivo usando páginas grandes

O exemplo a seguir usa a [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) com o sinalizador **SEC LARGE \_ \_ PAGES** para usar páginas grandes. O buffer deve ser grande o suficiente para conter o tamanho mínimo de uma página grande. Esse valor é obtido usando a [**função GetLargePageMinimum.**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) Esse recurso também requer o privilégio "SeLockMemoryPrivilege".

> [!NOTE]
> Começando no Windows 10, versão 1703, a função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) mapeia uma exibição usando páginas pequenas por padrão, mesmo para objetos de mapeamento de arquivo criados com o sinalizador **SEC LARGE \_ \_ PAGES.** Neste e em versões posteriores do sistema operacional, você deve especificar o sinalizador **FILE \_ MAP LARGE \_ \_ PAGES** com a [**função MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para mapear páginas grandes. Esse sinalizador é ignorado nas versões do sistema operacional antes Windows 10, versão 1703.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUF_SIZE 65536

TCHAR szName[]=TEXT("LARGEPAGE");
typedef int (*GETLARGEPAGEMINIMUM)(void);

void DisplayError(const wchar_t* pszAPI, DWORD dwError)
{
    LPVOID lpvMessageBuffer;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER |
                  FORMAT_MESSAGE_FROM_SYSTEM |
                  FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL, dwError,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR)&lpvMessageBuffer, 0, NULL);

    //... now display this string
    _tprintf(TEXT("ERROR: API        = %s\n"), pszAPI);
    _tprintf(TEXT("       error code = %d\n"), dwError);
    _tprintf(TEXT("       message    = %s\n"), lpvMessageBuffer);

    // Free the buffer allocated by the system
    LocalFree(lpvMessageBuffer);

    ExitProcess(GetLastError());
}

void Privilege(const wchar_t* pszPrivilege, BOOL bEnable)
{
    HANDLE           hToken;
    TOKEN_PRIVILEGES tp;
    BOOL             status;
    DWORD            error;

    // open process token
    if (!OpenProcessToken(GetCurrentProcess(), TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken))
        DisplayError(TEXT("OpenProcessToken"), GetLastError());

    // get the luid
    if (!LookupPrivilegeValue(NULL, pszPrivilege, &tp.Privileges[0].Luid))
        DisplayError(TEXT("LookupPrivilegeValue"), GetLastError());

    tp.PrivilegeCount = 1;

    // enable or disable privilege
    if (bEnable)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // enable or disable privilege
    status = AdjustTokenPrivileges(hToken, FALSE, &tp, 0, (PTOKEN_PRIVILEGES)NULL, 0);

    // It is possible for AdjustTokenPrivileges to return TRUE and still not succeed.
    // So always check for the last error value.
    error = GetLastError();
    if (!status || (error != ERROR_SUCCESS))
        DisplayError(TEXT("AdjustTokenPrivileges"), GetLastError());

    // close the handle
    if (!CloseHandle(hToken))
        DisplayError(TEXT("CloseHandle"), GetLastError());
}

int _tmain(void)
{
    HANDLE hMapFile;
    LPCTSTR pBuf;
    DWORD size;
    GETLARGEPAGEMINIMUM pGetLargePageMinimum;
    HINSTANCE  hDll;

    // call succeeds only on Windows Server 2003 SP1 or later
    hDll = LoadLibrary(TEXT("kernel32.dll"));
    if (hDll == NULL)
        DisplayError(TEXT("LoadLibrary"), GetLastError());

    pGetLargePageMinimum = (GETLARGEPAGEMINIMUM)GetProcAddress(hDll,
        "GetLargePageMinimum");
    if (pGetLargePageMinimum == NULL)
        DisplayError(TEXT("GetProcAddress"), GetLastError());

    size = (*pGetLargePageMinimum)();

    FreeLibrary(hDll);

    _tprintf(TEXT("Page Size: %u\n"), size);

    Privilege(TEXT("SeLockMemoryPrivilege"), TRUE);

    hMapFile = CreateFileMapping(
         INVALID_HANDLE_VALUE,    // use paging file
         NULL,                    // default security
         PAGE_READWRITE | SEC_COMMIT | SEC_LARGE_PAGES,
         0,                       // max. object size
         size,                    // buffer size
         szName);                 // name of mapping object

    if (hMapFile == NULL)
        DisplayError(TEXT("CreateFileMapping"), GetLastError());
    else
        _tprintf(TEXT("File mapping object successfully created.\n"));

    Privilege(TEXT("SeLockMemoryPrivilege"), FALSE);

    pBuf = (LPTSTR) MapViewOfFile(hMapFile,          // handle to map object
         FILE_MAP_ALL_ACCESS | FILE_MAP_LARGE_PAGES, // read/write permission
         0,
         0,
         BUF_SIZE);

    if (pBuf == NULL)
        DisplayError(TEXT("MapViewOfFile"), GetLastError());
    else
        _tprintf(TEXT("View of file successfully mapped.\n"));

    // do nothing, clean up an exit
    UnmapViewOfFile(pBuf);
    CloseHandle(hMapFile);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um objeto de mapeamento de arquivo](creating-a-file-mapping-object.md)
</dt> <dt>

[Suporte a página grande](large-page-support.md)
</dt> </dl>

 

 
