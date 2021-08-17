---
description: O exemplo a seguir é o código-fonte necessário para criar uma DLL simples, Myputs.dll.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Criando uma biblioteca de Dynamic-Link simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c3708f98c6b916c54940bc1667ebc4827b29c78596f55102331491aca29e65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963786"
---
# <a name="creating-a-simple-dynamic-link-library"></a>Criando uma biblioteca de Dynamic-Link simples

O exemplo a seguir é o código-fonte necessário para criar uma DLL simples, Myputs.dll. Ele define uma função de impressão de cadeia de caracteres simples chamada myPuts. A DLL myputs não define uma função de ponto de entrada, pois está vinculada à biblioteca em tempo de execução C e não tem nenhuma função de inicialização ou limpeza própria para executar.

Para criar a DLL, siga as instruções na documentação incluída com suas ferramentas de desenvolvimento.

Para ver um exemplo que usa myPuts, consulte [Using Load-Time Dynamic Linking or](using-load-time-dynamic-linking.md) Using Run-Time Dynamic [Linking](using-run-time-dynamic-linking.md).


```C++
// The myPuts function writes a null-terminated string to
// the standard output device.
 
// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.
 
 
#include <windows.h>
 
#define EOF (-1)
 
#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif
 
__declspec(dllexport) int __cdecl myPuts(LPWSTR lpszMsg)
{
    DWORD cchWritten;
    HANDLE hConout;
    BOOL fRet;
 
    // Get a handle to the console output device.

    hConout = CreateFileW(L"CONOUT$",
                         GENERIC_WRITE,
                         FILE_SHARE_WRITE,
                         NULL,
                         OPEN_EXISTING,
                         FILE_ATTRIBUTE_NORMAL,
                         NULL);

    if (INVALID_HANDLE_VALUE == hConout)
        return EOF;
 
    // Write a null-terminated string to the console output device.
 
    while (*lpszMsg != L'\0')
    {
        fRet = WriteConsole(hConout, lpszMsg, 1, &cchWritten, NULL);
        if( (FALSE == fRet) || (1 != cchWritten) )
            return EOF;
        lpszMsg++;
    }
    return 1;
}
 
#ifdef __cplusplus
}
#endif
```



 

 



