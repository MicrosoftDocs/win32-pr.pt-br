---
description: Você usa as estruturas a seguir ao trabalhar com dados de desempenho.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Estruturas de contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 00e9a505a9fe74592f571f3db108af2247a6d44889bc3ddbc2e4dae0844600b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674746"
---
# <a name="performance-counters-structures"></a>Estruturas de contadores de desempenho

Você usa as estruturas a seguir ao trabalhar com dados de desempenho.

Para obter informações sobre as funções que estão disponíveis para trabalhar com contadores de desempenho, consulte [funções de contadores de desempenho](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>Estruturas de PDH (auxiliar de dados de desempenho)

Os consumidores que usam as funções [PDH (auxiliar de dados de desempenho)](using-the-pdh-functions-to-consume-counter-data.md) usam as seguintes estruturas:

- [**configuração do PDH \_ Browse \_ DLG \_**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ Browse \_ DLG \_ config \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**\_informações do contador PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**\_elementos do \_ caminho do contador PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**\_elementos de \_ caminho de item de dados PDH \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**metavalor de PDH \_ fmt \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**\_item de \_ metavalor do PDH fmt \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**\_contador bruto de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**\_item de \_ contador \_ bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**\_registro de \_ log \_ bruto do PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**Estatísticas de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**\_informações de tempo de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Estruturas de consumidor de PerfLib v2

Os consumidores que usam as funções de [consumidor da PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) usam as seguintes estruturas:

- [**\_dados do contador de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**\_cabeçalho do contador de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**\_identificador do contador de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**\_informações de \_ reg do contador de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**informações de reg do contador de desempenho \_ \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**\_cabeçalho de dados de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**\_cabeçalho de instância de perf \_**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**\_vários \_ contadores de desempenho**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**\_várias \_ instâncias de desempenho**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**cabeçalho do buffer da cadeia de \_ caracteres perf \_ \_**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**cabeçalho do contador de cadeia de caracteres de desempenho \_ \_ \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Estruturas de provedor de PerfLib v2

Os [provedores de dados de desempenho v2](providing-counter-data-using-version-2-0.md) usam as seguintes estruturas:

- [**\_identidade do contador de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**\_informações do contador de desempenho \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**informações do contador de desempenho \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**instância do contador de desempenho \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**\_contexto do provedor de desempenho \_**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Estruturas de DLL de desempenho

Os [provedores de DLL de extensão de desempenho](providing-counter-data-using-a-performance-dll.md) e os [consumidores que usam as funções de registro para consumir dados de contador](using-the-registry-functions-to-consume-counter-data.md) usam as seguintes estruturas:

- [**\_bloco de contador de desempenho \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**\_definição do contador de desempenho \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**\_bloco de dados de desempenho \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**\_definição de instância de perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**\_tipo de objeto perf \_**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
