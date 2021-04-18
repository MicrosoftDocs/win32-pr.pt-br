---
title: Usando as funções PerfLib para consumir dados de contador
description: As funções de API de PerfLib podem ser usadas para consumir dados do contador de desempenho v2 diretamente quando a PDH não puder ser usada.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2020
ms.locfileid: "105795498"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>Usando as funções PerfLib para consumir dados de contador

Use as funções de consumidor de PerfLib para consumir dados de desempenho de provedores de dados de desempenho v2 Quando você não puder usar as [funções de PDH (auxiliar de dados de desempenho)](using-the-pdh-functions-to-consume-counter-data.md). Essas funções podem ser usadas ao escrever aplicativos OneCore para coletar conjuntos de registros v2 ou quando você precisa coletar conjuntos de registros V2 com dependências mínimas e sobrecarga.

> [!TIP]
> As funções de consumidor do PerfLib v2 são mais difíceis de usar do que as funções PDH (auxiliar de dados de desempenho) e dão suporte apenas à coleta de dados de provedores v2. As funções de PDH devem ser preferenciais para a maioria dos aplicativos.

As funções de consumidor do PerfLib v2 são a API de nível baixo para coletar dados de **provedores v2**. As funções de consumidor do PerfLib v2 não dão suporte à coleta de dados de **provedores v1**.

> [!WARNING]
> As funções de consumidor de PerfLib v2 podem potencialmente coletar dados de fontes não confiáveis, por exemplo, de serviços locais de privilégios limitados ou de máquinas remotas. As funções de consumidor do PerfLib v2 não validam os dados quanto à integridade ou consistência. Cabe ao seu aplicativo de consumidor verificar se os dados retornados são consistentes, por exemplo, que os valores de tamanho no bloco de dados retornado não excedem o tamanho real do bloco de dados retornado. Isso é especialmente importante quando o aplicativo consumidor é executado com privilégios elevados.

## <a name="perflib-usage"></a>Uso de PerfLib

O `perflib.h` cabeçalho inclui as declarações usadas por provedores de modo de usuário v2 (ou seja, a API do provedor de Perflib) e consumidores v2 (ou seja, a API de cliente do Perflib). Ele declara as seguintes funções para consumir dados de desempenho de v2:

- Use [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) para obter os GUIDs dos conjuntos de valores que são registrados pelos provedores V2 no sistema.
- Use [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) para obter informações sobre um conjunto de contadores específico, como o nome do contador, a descrição, o tipo (instância única ou várias instâncias), tipos de contadores, nomes de contadores e descrições de contadores.
- Use [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) para obter os nomes das instâncias atualmente ativas de um contador de várias instâncias.
- Use [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) para criar um novo identificador de consulta a ser usado para coletar dados de um ou mais conjuntos de linhas.
- Use [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) para fechar um identificador de consulta.
- Use [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) para adicionar uma consulta a um identificador de consulta.
- Use [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) para remover uma consulta de um identificador de consulta.
- Use [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) para obter informações sobre as consultas atuais em um identificador de consulta.
- Use [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) para coletar os dados de desempenho de um identificador de consulta.

Se o consumidor estiver consumindo dados somente de um provedor específico em que os índices GUID e contador são estáveis e você tiver acesso ao arquivo de símbolo gerado pelo [ctrpp](ctrpp.md)(a partir do `-ch` parâmetro ctrpp), poderá embutir em código o GUID do contador e os valores do índice do contador em seu consumidor.

Caso contrário, você precisará carregar os metadados do CounterSet para determinar os GUIDs do contador e os índices do contador a serem usados na consulta da seguinte maneira:

- Use **PerfEnumerateCounterSet** para obter uma lista de GUIDs do CounterSet com suporte.
- Para cada GUID, use **PerfQueryCounterSetRegistrationInfo** para carregar o nome do CounterSet. Pare quando encontrar o nome que você está procurando.
- Use **PerfQueryCounterSetRegistrationInfo** para carregar os metadados restantes (configuração do CounterSet, nomes de contadores, índices de contadores, tipos de contadores) para esse contador.

Se você só precisar saber os nomes das instâncias atualmente ativas de um CounterSet (ou seja, se não precisar dos valores de dados de desempenho reais), poderá usar **PerfEnumerateCounterSetInstances**. Isso usa um CounterSet GUID como entrada e retorna um `PERF_INSTANCE_HEADER` bloco com os nomes e as IDs das instâncias atualmente ativas do CounterSet especificado.

### <a name="queries"></a>Consultas

Para coletar dados de desempenho, você precisa criar um identificador de consulta, adicionar consultas a ele e coletar os dados das consultas.

Um identificador de consulta pode ter muitas consultas associadas a ele. Quando você chamar **PerfQueryCounterData** para um identificador de consulta, o PerfLib executará todas as consultas do manipulador e coletará todos os resultados.

Cada consulta especifica um GUID do CounterSet, um filtro de nome de instância, um filtro de ID de instância opcional e um filtro de ID de contador opcional.

- O GUID do CounterSet é necessário. Indica o GUID do CounterSet do qual a consulta coletará dados. Isso é semelhante à `FROM` cláusula de uma consulta SQL.
- O filtro de nome de instância é necessário. Ele indica um padrão de caractere curinga que o nome da instância deve corresponder para a instância a ser incluída na consulta, com a `*` indicação de "qualquer caractere" e `?` indicando "um caracteres". Para conjuntos de ocorrências de instância única, isso **deve** ser definido como uma cadeia de caracteres de comprimento zero `""` . Para conjuntos de contrainstâncias de várias instâncias, isso **deve** ser definido como uma cadeia de caracteres não vazia (use `"*"` para aceitar todos os nomes de instância). Isso é semelhante a uma `WHERE InstanceName LIKE NameFilter` cláusula de uma consulta SQL.
- O filtro de ID de instância é opcional. Se presente (ou seja, se definido com um valor diferente de `0xFFFFFFFF` ), ele indica que a consulta só deve coletar instâncias em que a ID da instância corresponda à ID especificada. Se estiver ausente (ou seja, se definido como `0xFFFFFFFF` ), isso indica que a consulta deve aceitar todas as IDs de instância. Isso é semelhante a uma `WHERE InstanceId == IdFilter` cláusula de uma consulta SQL.
- O filtro de ID do contador é opcional. Se presente (ou seja, se definido com um valor diferente de `PERF_WILDCARD_COUNTER` ), ele indica que a consulta deve coletar um único contador, semelhante a uma `SELECT CounterName` cláusula de uma consulta SQL. Se estiver ausente (ou seja, se definido como `PERF_WILDCARD_COUNTER` ), isso indica que a consulta deve coletar todos os contadores disponíveis, de forma semelhante a uma `SELECT *` cláusula de uma consulta SQL.

Use **PerfAddCounters** para adicionar consultas a um identificador de consulta. Use **PerfDeleteCounters** para remover consultas de um identificador de consulta.

Depois de alterar as consultas em um identificador de consulta, use **PerfQueryCounterInfo** para obter os índices de consulta. Os índices indicam a ordem na qual os resultados da consulta serão retornados por **PerfQueryCounterData** (os resultados nem sempre corresponderão à ordem na qual as consultas foram adicionadas).

Depois que o identificador de consulta estiver pronto, use **PerfQueryCounterData** para coletar os dados. Normalmente, você coletará os dados periodicamente (uma vez por segundo ou uma vez por minuto) e processará os dados conforme necessário.

> [!NOTE]
> Os contadores de desempenho não foram projetados para serem coletados mais de uma vez por segundo.

**PerfQueryCounterData** retornará um `PERF_DATA_HEADER` bloco, que consiste em um cabeçalho de dados com carimbos de data/hora seguidos por uma sequência de `PERF_COUNTER_HEADER` blocos, cada um contendo os resultados de uma consulta.

O `PERF_COUNTER_HEADER` pode conter vários tipos diferentes de dados, conforme indicado pelo valor do `dwType` campo:

- `PERF_ERROR_RETURN` -PerfLib não pode obter dados de contador válidos de volta do provedor.
- `PERF_SINGLE_COUNTER` -A consulta foi para um único contador de um contador de instância única. Os resultados contêm apenas o valor do contador solicitado.
- `PERF_MULTIPLE_COUNTERS` -A consulta foi para vários contadores de um contador de instância única. O resultado contém os valores do contador, juntamente com informações para correspondência de cada valor com o contador correspondente (ou seja, títulos de coluna).
- `PERF_MULTIPLE_INSTANCES` -A consulta foi para um único contador de um contador de várias instâncias. Os resultados contêm as informações da instância (ou seja, cabeçalhos de linha) e um valor de contador por instância.
- `PERF_COUNTERSET` -A consulta foi para vários contadores de um contador de várias instâncias. Os resultados contêm as informações da instância (ou seja, cabeçalhos de linha), os valores de contador para cada instância e informações para correspondência de cada valor com o contador correspondente (ou seja, títulos de coluna).

Os valores retornados por **PerfQueryCounterData** são `UINT32` ou `UINT64` valores brutos. Normalmente, eles exigem algum processamento para produzir os valores formatados esperados. O processamento necessário depende do tipo do contador. Muitos tipos de contador exigem informações adicionais para o processamento completo, como um carimbo de data/hora ou um valor de um contador "base" no mesmo exemplo.

Alguns tipos de contadores são contadores "Delta" que só são significativos quando comparados com os dados de um exemplo anterior. Por exemplo, um contador de tipo `PERF_SAMPLE_COUNTER` tem um valor formatado que deve mostrar uma taxa (o número de vezes que uma coisa específica ocorreu por segundo no intervalo de amostragem), mas o valor bruto real é apenas uma contagem (o número de vezes que um determinado item ocorreu no total). Para produzir o valor de "taxa" formatado, você deve aplicar a fórmula correspondente ao tipo de contador. A fórmula para `PERF_SAMPLE_COUNTER` é `(N1 - N0) / ((T1 - T0) / F)` : subtrair o valor da amostra atual do valor do exemplo anterior (dando o número de vezes que o evento ocorreu durante o intervalo de amostragem) e dividir o resultado pelo número de segundos no intervalo de amostragem (obtido subtraindo o carimbo de data/hora atual do carimbo de data/hora do exemplo anterior e dividindo por frequência para converter o TimeSpan em segundos)

Consulte [calculando valores de contador](calculating-counter-values.md) para obter mais informações sobre como calcular valores formatados de valores brutos.

## <a name="sample"></a>Amostra

O código a seguir implementa um consumidor que usa as funções de consumidor do PerfLib v2 para ler informações de desempenho da CPU do contador de "informações do processador".

O consumidor é organizado da seguinte maneira:

- A `CpuPerfCounters` classe implementa a lógica para o consumo de dados de desempenho. Ele encapsula um identificador de consulta e um buffer de dados no qual os resultados da consulta são registrados.
- A `CpuPerfTimestamp` estrutura armazena as informações de carimbo de data/hora de um exemplo. Cada vez que os dados são coletados, o chamador recebe um único `CpuPerfTimestamp` .
- A `CpuPerfData` estrutura armazena as informações de desempenho (nome da instância e valores de desempenho brutos) para uma CPU. Cada vez que os dados são coletados, o chamador recebe uma matriz de `CpuPerfData` (um por CPU).

Este exemplo usa os valores de GUIDset de contador e ID de contador embutidos em código porque ele é otimizado para um contador específico (informações do processador) que não alterará os valores GUID ou ID. Uma classe mais genérica que lê dados de desempenho de conjuntos arbitrários precisaria usar **PerfQueryCounterSetRegistrationInfo** para pesquisar o mapeamento entre IDs de contador e valores de contador em tempo de execução.

Um `CpuPerfCountersConsumer.cpp` programa simples mostra como usar os valores da `CpuPerfCounters` classe.

### <a name="cpuperfcountersh"></a>CpuPerfCounters. h

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a>CpuPerfCounters. cpp

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a>CpuPerfCountersConsumer. cpp

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
