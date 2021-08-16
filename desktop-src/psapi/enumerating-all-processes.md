---
title: Enumerando todos os processos
description: O código de exemplo a seguir usa a função EnumProcesses para enumerar os processos atuais no sistema.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89798ed3d2d7e44f014d95833302edb5d5be078daf557eed32d3496c863539e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681003"
---
# <a name="enumerating-all-processes"></a>Enumerando todos os processos

O código de exemplo a seguir usa a função [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) para recuperar o identificador de processo para cada objeto de processo no sistema. Em seguida, [EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) é chamado para obter cada nome de processo e imprimi-lo.

>[!NOTE]
> Para processos de 64 bits, use a função [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) .

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }


    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



A função main Obtém uma lista de processos usando a função [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Para cada processo, Main chama a função **PrintProcessNameAndID** , passando-a para o identificador do processo. O **PrintProcessNameAndID** , por sua vez, chama a função [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obter o identificador de processo. Se **OpenProcess** falhar, a saída mostrará o nome do processo como <unknown> . Por exemplo, **OpenProcess** falha para os processos Idle e CSRSS porque suas restrições de acesso impedem que o código do usuário os abra. Em seguida, **PrintProcessNameAndID** chama a função [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obter as alças do módulo. Por fim, **PrintProcessNameAndID** chama a função [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) para obter o nome do arquivo executável e exibe o nome junto com o identificador do processo.

 

 
