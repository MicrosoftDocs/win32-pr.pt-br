---
description: A função CreateProcess cria um novo processo, que é executado independentemente do processo de criação. No entanto, para simplificar, a relação é conhecida como uma relação pai-filho.
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Criando processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8e5e4340f5c956e964b74ab134a7618a4c4bf0fa44eee1989a0457741d7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143099"
---
# <a name="creating-processes"></a>Criando processos

A [**função CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) cria um novo processo, que é executado independentemente do processo de criação. No entanto, para simplificar, a relação é conhecida como uma relação pai-filho.

O código a seguir demonstra como criar um processo.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



Se [**CreateProcess for**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) bem-sucedido, ele retornará uma estrutura [**PROCESS \_ INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) contendo identificadores e identificadores para o novo processo e seu thread primário. Os alças de thread e processo são criados com direitos de acesso completo, embora o acesso possa ser restrito se você especificar descritores de segurança. Quando você não precisar mais desses alças, feche-os usando a [**função CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

Você também pode criar um processo usando a [**função CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) [**ou CreateProcessWithLogonW.**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) Isso permite que você especifique o contexto de segurança da conta de usuário na qual o processo será executado.

 

 
