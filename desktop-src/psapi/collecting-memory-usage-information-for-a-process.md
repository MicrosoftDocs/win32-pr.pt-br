---
title: Coletando informações de uso de memória para um processo
description: Para determinar a eficiência do seu aplicativo, talvez você queira examinar seu uso de memória. O código de exemplo a seguir usa a função GetProcessMemoryInfo para obter informações sobre o uso de memória de um processo.
ms.assetid: 23641bf8-3653-4cb9-8008-cd99137ca268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9c2217f01c2c0f3a3ee1d2516b2e531cc243f5ac71c4022632d1b1c4dd4983
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462974"
---
# <a name="collecting-memory-usage-information-for-a-process"></a>Coletando informações de uso de memória para um processo

Para determinar a eficiência do seu aplicativo, talvez você queira examinar seu uso de memória. O código de exemplo a seguir usa a [**função GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) para obter informações sobre o uso de memória de um processo.


```C++
#include <windows.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintMemoryInfo( DWORD processID )
{
    HANDLE hProcess;
    PROCESS_MEMORY_COUNTERS pmc;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Print information about the memory usage of the process.

    hProcess = OpenProcess(  PROCESS_QUERY_INFORMATION |
                                    PROCESS_VM_READ,
                                    FALSE, processID );
    if (NULL == hProcess)
        return;

    if ( GetProcessMemoryInfo( hProcess, &pmc, sizeof(pmc)) )
    {
        printf( "\tPageFaultCount: 0x%08X\n", pmc.PageFaultCount );
        printf( "\tPeakWorkingSetSize: 0x%08X\n", 
                  pmc.PeakWorkingSetSize );
        printf( "\tWorkingSetSize: 0x%08X\n", pmc.WorkingSetSize );
        printf( "\tQuotaPeakPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakPagedPoolUsage );
        printf( "\tQuotaPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPagedPoolUsage );
        printf( "\tQuotaPeakNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaPeakNonPagedPoolUsage );
        printf( "\tQuotaNonPagedPoolUsage: 0x%08X\n", 
                  pmc.QuotaNonPagedPoolUsage );
        printf( "\tPagefileUsage: 0x%08X\n", pmc.PagefileUsage ); 
        printf( "\tPeakPagefileUsage: 0x%08X\n", 
                  pmc.PeakPagefileUsage );
    }

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

    // Print the memory usage for each process

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintMemoryInfo( aProcesses[i] );
    }

    return 0;
}
```



A função principal obtém uma lista de processos usando a [**função EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Para cada processo, main chama a função PrintMemoryInfo, passando o identificador do processo. PrintMemoryInfo, por sua vez, chama a [**função OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) para obter o alçamento do processo. Se **OpenProcess** falhar, a saída mostrará apenas o identificador do processo. Por exemplo, **o OpenProcess** falha nos processos Ocioso e CSRSS porque suas restrições de acesso impedem que o código no nível do usuário os abra. Por fim, PrintMemoryInfo chama a [**função GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) para obter as informações de uso de memória.

 

 