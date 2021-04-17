---
description: O exemplo a seguir grava dados de desempenho em tempo real em um arquivo de log.
ms.assetid: a1bc40ea-d928-495a-abc0-daf097202a12
title: Gravando dados de desempenho em um arquivo de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afce3c85b36d66f1b621e4c4f174bff327e6084a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754612"
---
# <a name="writing-performance-data-to-a-log-file"></a>Gravando dados de desempenho em um arquivo de log

O exemplo a seguir grava dados de desempenho em tempo real em um arquivo de log. O exemplo chama as funções [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) e [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para criar uma consulta para coletar dados do contador de tempo do processador. Em seguida, o exemplo chama a função [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) para criar o arquivo de log no qual gravar os dados. O exemplo chama a função [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) para coletar um exemplo e atualizar o arquivo de log uma vez por segundo por 20 segundos.

Para obter um exemplo que lê o arquivo de log gerado, consulte [lendo dados de desempenho de um arquivo de log](reading-performance-data-from-a-log-file.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <pdh.h>
#include <pdhmsg.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_PATH    = L"\\Processor(0)\\% Processor Time";
CONST ULONG SAMPLE_INTERVAL_MS = 1000;

void DisplayCommandLineHelp(void)
{
    wprintf(L"The command line must include a valid log file name.\n"); 
}

void wmain(int argc, WCHAR **argv)
{
    HQUERY hQuery = NULL;
    HLOG hLog = NULL;
    PDH_STATUS pdhStatus;
    DWORD dwLogType = PDH_LOG_TYPE_CSV;
    HCOUNTER hCounter;
    DWORD dwCount;

    if (argc != 2) 
    {
        DisplayCommandLineHelp();
        goto cleanup;
    }

    // Open a query object.
    pdhStatus = PdhOpenQuery(NULL, 0, &hQuery);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenQuery failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Add one counter that will provide the data.
    pdhStatus = PdhAddCounter(hQuery,
        COUNTER_PATH,
        0,
        &hCounter);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhAddCounter failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }

    // Open the log file for write access.
    pdhStatus = PdhOpenLog(argv[1], 
        PDH_LOG_WRITE_ACCESS | PDH_LOG_CREATE_ALWAYS,
        &dwLogType,
        hQuery,
        0, 
        NULL,
        &hLog);

    if (pdhStatus != ERROR_SUCCESS)
    {
        wprintf(L"PdhOpenLog failed with 0x%x\n", pdhStatus);
        goto cleanup;
    }
 
    // Write 10 records to the log file.
    for (dwCount = 0; dwCount < 10; dwCount++) 
    {
        wprintf(L"Writing record %d\n", dwCount);

        pdhStatus = PdhUpdateLog (hLog, NULL);
        if (ERROR_SUCCESS != pdhStatus)
        {
            wprintf(L"PdhUpdateLog failed with 0x%x\n", pdhStatus);
            goto cleanup;
        }

        // Wait one second between samples for a counter update.
        Sleep(SAMPLE_INTERVAL_MS); 
    }

cleanup:

    // Close the log file.
    if (hLog)
        PdhCloseLog (hLog, 0);

    // Close the query object.
    if (hQuery)
        PdhCloseQuery (hQuery);
}
```



 

 



