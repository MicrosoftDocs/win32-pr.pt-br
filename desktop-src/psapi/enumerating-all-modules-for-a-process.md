---
title: Enumerando todos os módulos para um processo
description: Para determinar quais processos carregaram uma DLL específica, você deve enumerar os módulos para cada processo. O código de exemplo a seguir usa a função EnumProcessModules para enumerar os módulos dos processos atuais no sistema.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294066"
---
# <a name="enumerating-all-modules-for-a-process"></a><span data-ttu-id="73eaa-104">Enumerando todos os módulos para um processo</span><span class="sxs-lookup"><span data-stu-id="73eaa-104">Enumerating All Modules For a Process</span></span>

<span data-ttu-id="73eaa-105">Para determinar quais processos carregaram uma DLL específica, você deve enumerar os módulos para cada processo.</span><span class="sxs-lookup"><span data-stu-id="73eaa-105">To determine which processes have loaded a particular DLL, you must enumerate the modules for each process.</span></span> <span data-ttu-id="73eaa-106">O código de exemplo a seguir usa a função [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para enumerar os módulos dos processos atuais no sistema.</span><span class="sxs-lookup"><span data-stu-id="73eaa-106">The following sample code uses the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to enumerate the modules of current processes in the system.</span></span>


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



<span data-ttu-id="73eaa-107">A função main Obtém uma lista de processos usando a função [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="73eaa-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="73eaa-108">Para cada processo, a função Main chama a função de módulo de busca, passando-a para o identificador do processo.</span><span class="sxs-lookup"><span data-stu-id="73eaa-108">For each process, the main function calls the PrintModules function, passing it the process identifier.</span></span> <span data-ttu-id="73eaa-109">Os módulos de suplemento, por sua vez, chamam a função [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obter o identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="73eaa-109">PrintModules in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="73eaa-110">Se **OpenProcess** falhar, a saída mostrará apenas o identificador do processo.</span><span class="sxs-lookup"><span data-stu-id="73eaa-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="73eaa-111">Por exemplo, **OpenProcess** falha para os processos Idle e CSRSS porque suas restrições de acesso impedem que o código do usuário os abra.</span><span class="sxs-lookup"><span data-stu-id="73eaa-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="73eaa-112">Em seguida, o defaultmodules chama a função [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) para obter a função de identificadores de módulo.</span><span class="sxs-lookup"><span data-stu-id="73eaa-112">Next, PrintModules calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles function.</span></span> <span data-ttu-id="73eaa-113">Por fim, os módulos de busca chamam a função [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) , uma vez para cada módulo, para obter os nomes de módulo.</span><span class="sxs-lookup"><span data-stu-id="73eaa-113">Finally, PrintModules calls the [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) function, once for each module, to obtain the module names.</span></span>

 

 