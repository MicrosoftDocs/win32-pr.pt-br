---
description: A função OpenPerformanceData oferece ao provedor uma oportunidade de inicializar suas estruturas de dados de desempenho.
ms.assetid: 0849d9cb-90d1-4b79-810d-b43f69cc9055
title: Implementando OpenPerformanceData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835c60e449e7e95264c20623dc103395d34b770feb632ba2409e3d658094d289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579826"
---
# <a name="implementing-openperformancedata"></a>Implementando OpenPerformanceData

A [**função OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) oferece ao provedor uma oportunidade de inicializar suas estruturas de dados de desempenho. O sistema chama sua função aberta na primeira vez que um consumidor chama [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)ou se o consumidor usa a função [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) ou [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) para abrir **HKEY \_ PERFORMANCE \_ DATA**.

O exemplo a seguir mostra uma implementação da [**função OpenPerformanceData.**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) O arquivo de header que contém a definição dos contadores usados nesta função segue este exemplo. Se você usar c++ para implementar essa função, use extern "C" ao declarar sua função. As constantes de deslocamento de contador usadas neste exemplo são definidas no arquivo CounterOffsets.h mostrado em Adicionando nomes de contadores e [Descrição ao Registro](adding-counter-names-and-descriptions-to-the-registry.md).


```C++
#include "provider.h"


// Callback that the performance service calls once for each consumer that wants 
// to consume one or more of your counters. You can use this notification to 
// prepare the counter data structures and setup communications with the 
// application that is providing the actual performance data.
extern "C" DWORD APIENTRY OpenPerfData(LPWSTR pContext)
{
    DWORD FirstCounterIndex = 0;
    DWORD FirstHelpIndex = 0;
    DWORD DataSize = sizeof(DWORD);  // Used in the RegQueryValueEx call
    HKEY hkey;
    LONG rc = ERROR_SUCCESS;

    // Use g_OpenCount to prevent initializing the data more than once.
    
    if (g_OpenCount > 1)
    {
        goto cleanup;
    }

    // Retrieve the application specific context data
    // if you define an Export value under the 
    // HKLM\SYSTEM\CurrentControlSet\Services\MyProvider\Linkage key.
    // The context string is a REG_MULTI_SZ string.

    if (pContext)
    {
        for (; *pContext; pContext += (wcslen(pContext)+1))
        {
            // Do something with the string.
        }
    }

    // Retrieve the starting index values for your counters and help strings. You add 
    // your offset values (see Adding Counter Names and Descriptions to the Registry)
    // to these index values to determine your actual object and counter index values.

    rc = RegOpenKeyEx(HKEY_LOCAL_MACHINE, PERFORMANCE_REGISTRY_PATH, 0, KEY_READ, &hkey);
    if (ERROR_SUCCESS == rc)
    {
        rc = RegQueryValueEx(hkey, L"First Counter", NULL, NULL, (LPBYTE)&FirstCounterIndex, &DataSize);
        if (ERROR_SUCCESS == rc)
        {
            rc = RegQueryValueEx(hkey, L"First Help", NULL, NULL, (LPBYTE)&FirstHelpIndex, &DataSize);        
        }

        RegCloseKey(hkey);
    }

    // If you could not open the key or retrieve the value, exit.

    if (ERROR_SUCCESS != rc)
    {
        // If you return a non-success code, the service adds a Disable Performance 
        // Counters value to your Performance key to disable your provider.
        // Consider logging an event and returning success instead of failing.

        rc = ERROR_SUCCESS;
        goto cleanup;
    }

    // Initialize the Transfer object. This is a single instance object, so you can
    // initialize each member of the object and its counters.

    ZeroMemory(&g_Transfer, TransferSize);
    g_Transfer.Object.TotalByteLength = TransferSize;
    g_Transfer.Object.DefinitionLength = sizeof(PERF_OBJECT_TYPE) + 
        sizeof(PERF_COUNTER_DEFINITION) * NumberOfTransferCounters;
    g_Transfer.Object.HeaderLength = sizeof(PERF_OBJECT_TYPE);
    g_TransferIndex = FirstCounterIndex;
    g_Transfer.Object.ObjectNameTitleIndex = g_TransferIndex;
    g_Transfer.Object.ObjectHelpTitleIndex = FirstHelpIndex;
    g_Transfer.Object.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Transfer.Object.NumCounters = NumberOfTransferCounters;
    g_Transfer.Object.DefaultCounter = -1;  // No default counter
    g_Transfer.Object.NumInstances = PERF_NO_INSTANCES;

    // Initialize the bytes sent counter.

    g_Transfer.BytesSentCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Transfer.BytesSentCounter.CounterNameTitleIndex = FirstCounterIndex + BYTES_SENT;
    g_Transfer.BytesSentCounter.CounterHelpTitleIndex = FirstHelpIndex + BYTES_SENT;
    g_Transfer.BytesSentCounter.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Transfer.BytesSentCounter.CounterType = PERF_COUNTER_RAWCOUNT;
    g_Transfer.BytesSentCounter.CounterSize = sizeof(DWORD);
    g_Transfer.BytesSentCounter.CounterOffset = BytesSentOffset;

    // Initialize the available bandwidth counter.

    g_Transfer.AvailableBandwidthCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Transfer.AvailableBandwidthCounter.CounterNameTitleIndex = FirstCounterIndex + AVAILABLE_BANDWIDTH;
    g_Transfer.AvailableBandwidthCounter.CounterHelpTitleIndex = FirstHelpIndex + AVAILABLE_BANDWIDTH;
    g_Transfer.AvailableBandwidthCounter.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Transfer.AvailableBandwidthCounter.CounterType = PERF_RAW_FRACTION;
    g_Transfer.AvailableBandwidthCounter.CounterSize = sizeof(DWORD);
    g_Transfer.AvailableBandwidthCounter.CounterOffset = AvailableBandwidthOffset;

    // Initialize the total bandwidth counter. This is a base counter for the
    // available bandwidth counter. You do not specify index values for base counters.

    g_Transfer.TotalBandwidthBaseCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Transfer.TotalBandwidthBaseCounter.CounterType = PERF_RAW_BASE;
    g_Transfer.TotalBandwidthBaseCounter.CounterSize = sizeof(DWORD);
    g_Transfer.TotalBandwidthBaseCounter.CounterOffset = TotalBandwidthBaseOffset;

    // Specify the size of the counter block which contains the raw counter values. 

    g_Transfer.CounterBlock.ByteLength = EndOfTransferData;

    // Initialize the Peer object. This is a multiple instance object. You cannot 
    // initialize all members of the Peer object because you do not know how 
    // many instances there will be until the object data is queried. You set 
    // the TotalByteLength and NumInstances members in the CollectPerfData function.

    ZeroMemory(&g_Peer, sizeof(PEER));
    g_Peer.Object.DefinitionLength = sizeof(PERF_OBJECT_TYPE) + 
        sizeof(PERF_COUNTER_DEFINITION) * NumberOfPeerCounters;
    g_Peer.Object.HeaderLength = sizeof(PERF_OBJECT_TYPE);
    g_PeerIndex = FirstCounterIndex + PEER_OBJECT;
    g_Peer.Object.ObjectNameTitleIndex = g_PeerIndex;
    g_Peer.Object.ObjectHelpTitleIndex = FirstHelpIndex + PEER_OBJECT;
    g_Peer.Object.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Peer.Object.NumCounters = NumberOfPeerCounters;
    g_Peer.Object.DefaultCounter = -1;  // No default counter

    // Initialize the bytes served counter.

    g_Peer.BytesServedCounter.ByteLength = sizeof(PERF_COUNTER_DEFINITION);
    g_Peer.BytesServedCounter.CounterNameTitleIndex = FirstCounterIndex + BYTES_SERVED;
    g_Peer.BytesServedCounter.CounterHelpTitleIndex = FirstHelpIndex + BYTES_SERVED;
    g_Peer.BytesServedCounter.DetailLevel = PERF_DETAIL_ADVANCED;
    g_Peer.BytesServedCounter.CounterType = PERF_COUNTER_RAWCOUNT;
    g_Peer.BytesServedCounter.CounterSize = sizeof(DWORD);
    g_Peer.BytesServedCounter.CounterOffset = BytesServedOffset;

    InterlockedIncrement(&g_OpenCount);  // Decremented in ClosePerfData

cleanup:
    
    return rc;
}
```



A seguir está o arquivo de header usado neste exemplo.


```C++
#ifndef _PROVIDER_H
#define _PROVIDER_H

#include <windows.h>
#include <strsafe.h>
#include "CounterOffsets.h"

extern "C" DWORD APIENTRY OpenPerfData(LPWSTR pContext);
extern "C" DWORD APIENTRY CollectPerfData(LPWSTR pQuery, PVOID* ppData, LPDWORD pcbData, LPDWORD pObjectsReturned);
extern "C" DWORD APIENTRY ClosePerfData();
BOOL IsQuerySupported(LPWSTR pQuery, DWORD* pQueriedObjects);
DWORD GetQuerySize(DWORD QueriedObjects);

// Define the Transfer counter object. This object is a single 
// instance counter object, so you can define it completely.
typedef struct _transfer 
{
    PERF_OBJECT_TYPE Object;
    PERF_COUNTER_DEFINITION BytesSentCounter;
    PERF_COUNTER_DEFINITION AvailableBandwidthCounter;
    PERF_COUNTER_DEFINITION TotalBandwidthBaseCounter;
    PERF_COUNTER_BLOCK CounterBlock;
    DWORD BytesSentData;
    DWORD AvailableBandwidthData;
    DWORD TotalBandwidthData;
} TRANSFER, *PTRANSFER;

// Define offsets to counter data
#define BytesSentOffset sizeof(PERF_COUNTER_BLOCK)
#define AvailableBandwidthOffset BytesSentOffset + sizeof(DWORD)
#define TotalBandwidthBaseOffset AvailableBandwidthOffset + sizeof(DWORD)
#define EndOfTransferData TotalBandwidthBaseOffset + sizeof(DWORD)
#define TransferSize sizeof(TRANSFER)

#define NumberOfTransferCounters 3

#define MAX_INSTANCE_NAME_LEN 15 

// Define the Peer counter object. This object is a multiple
// instance object, so you must define the object and instances
// separately.
typedef struct _peer {
  PERF_OBJECT_TYPE Object;
  PERF_COUNTER_DEFINITION BytesServedCounter;
} PEER, *PPEER;

typedef struct _peerinstance {
  PERF_INSTANCE_DEFINITION Instance;
  WCHAR InstanceName[MAX_INSTANCE_NAME_LEN+1];
  PERF_COUNTER_BLOCK CounterBlock;
  DWORD BytesServedData;
} PEER_INSTANCE, *PPEER_INSTANCE;

#define BytesServedOffset sizeof(PERF_COUNTER_BLOCK)
#define EndOfPeerData BytesServedOffset + sizeof(DWORD)
#define NumberOfPeerCounters 1

// For this example, the instances are static, so predefine the names.
#define INSTANCE_NAME_1 L"Peer 1"
#define INSTANCE_NAME_2 L"Peer 2"
#define PERFORMANCE_REGISTRY_PATH L"SYSTEM\\CurrentControlSet\\Services\\MyApplication\\Performance"

typedef enum _queriedflags { 
  QUERIED_TRANSFER_OBJECT = 1,
  QUERIED_PEER_OBJECT = 2,
  QUERIED_ALL_OBJECTS = 0xFFFF
} QUERIED_FLAGS;

//Globals
TRANSFER g_Transfer;             // Transfer object
PEER g_Peer;                     // Peer object
DWORD g_TransferIndex = 0;       // Index value for the Transfer object
DWORD g_PeerIndex = 0;           // Index value for the Peer object
DWORD g_QueriedObjects = 0;      // Objects that were queried
UNALIGNED LONG g_OpenCount = 0;  // Reference count for the number of times
                                 // that OpenPerfData is called.
#endif
```



O exemplo a seguir mostra o arquivo de definição de módulo (.def) usado para exportar as funções open, collect e close.


```C++
LIBRARY    "PerfProvider"

EXPORTS
    OpenPerfData    @1
    CollectPerfData    @2
    ClosePerfData    @3
```



O exemplo a seguir mostra uma implementação da [*função ClosePerformanceData.*](/windows/win32/api/winperf/nc-winperf-pm_close_proc) O sistema chama sua função close quando um consumidor chama [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) para fechar **os DADOS DE DESEMPENHO \_ do \_ HKEY.** Os provedores usam essa chamada para liberar todos os recursos que eles alocaram.


```C++
// Callback that the performance service calls once for each consumer that has
// finished consuming your performance counters. Cleanup any resources that 
// you allocated for your performance counters.
extern "C" DWORD APIENTRY ClosePerfData(void)
{
    if (g_OpenCount > 0)
    {
        InterlockedDecrement(&g_OpenCount);
    }

    return ERROR_SUCCESS;
}
```



 

 
