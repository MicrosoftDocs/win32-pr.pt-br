---
title: Enumerando todos os módulos para um processo
description: Para determinar quais processos carregaram uma DLL específica, você deve enumerar os módulos para cada processo. O código de exemplo a seguir usa a função EnumProcessModules para enumerar os módulos dos processos atuais no sistema.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17012019c21f550940ea8c11c07153b0c3495471b4d62bf2f8af469ef6b7b90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032984"
---
# <a name="enumerating-all-modules-for-a-process"></a>Enumerando todos os módulos para um processo

Para determinar quais processos carregaram uma DLL específica, você deve enumerar os módulos para cada processo. O código de exemplo a seguir usa a [**função EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para enumerar os módulos dos processos atuais no sistema.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



A função principal obtém uma lista de processos usando a [**função EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Para cada processo, a função principal chama a função PrintModules, passando-a para o identificador do processo. PrintModules, por sua vez, chama a [**função OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obter o alçamento do processo. Se **OpenProcess** falhar, a saída mostrará apenas o identificador do processo. Por exemplo, **o OpenProcess** falha nos processos Ocioso e CSRSS porque suas restrições de acesso impedem que o código no nível do usuário os abra. Em seguida, PrintModules chama a [**função EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obter a função de alças do módulo. Por fim, PrintModules chama a [**função GetModuleFileNameEx,**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) uma vez para cada módulo, para obter os nomes do módulo.

 

 