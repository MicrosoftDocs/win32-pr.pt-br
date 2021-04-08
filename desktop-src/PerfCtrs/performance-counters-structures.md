---
description: Você usa as estruturas a seguir ao trabalhar com dados de desempenho.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Estruturas de contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921730"
---
# <a name="performance-counters-structures"></a><span data-ttu-id="9e900-103">Estruturas de contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="9e900-103">Performance Counters Structures</span></span>

<span data-ttu-id="9e900-104">Você usa as estruturas a seguir ao trabalhar com dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9e900-104">You use the following structures when working with performance data.</span></span>

<span data-ttu-id="9e900-105">Para obter informações sobre as funções que estão disponíveis para trabalhar com contadores de desempenho, consulte [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9e900-105">For information about the functions that are available for working with performance counters, see [Performance Counters Functions](performance-counters-functions.md).</span></span>

## <a name="performance-data-helper-pdh-structures"></a><span data-ttu-id="9e900-106">Estruturas de PDH (auxiliar de dados de desempenho)</span><span class="sxs-lookup"><span data-stu-id="9e900-106">Performance Data Helper (PDH) structures</span></span>

<span data-ttu-id="9e900-107">Os consumidores que usam as funções [PDH (auxiliar de dados de desempenho)](using-the-pdh-functions-to-consume-counter-data.md) usam as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="9e900-107">Consumers that use the [Performance Data Helper (PDH)](using-the-pdh-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="9e900-108">**configuração do PDH \_ Browse \_ DLG \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-108">**PDH\_BROWSE\_DLG\_CONFIG**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [<span data-ttu-id="9e900-109">**PDH \_ Browse \_ DLG \_ config \_ H**</span><span class="sxs-lookup"><span data-stu-id="9e900-109">**PDH\_BROWSE\_DLG\_CONFIG\_H**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [<span data-ttu-id="9e900-110">**\_informações do contador PDH \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-110">**PDH\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [<span data-ttu-id="9e900-111">**\_elementos do \_ caminho do contador PDH \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-111">**PDH\_COUNTER\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [<span data-ttu-id="9e900-112">**\_elementos de \_ caminho de item de dados PDH \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-112">**PDH\_DATA\_ITEM\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [<span data-ttu-id="9e900-113">**metavalor de PDH \_ fmt \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-113">**PDH\_FMT\_COUNTERVALUE**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [<span data-ttu-id="9e900-114">**\_item de \_ metavalor do PDH fmt \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-114">**PDH\_FMT\_COUNTERVALUE\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [<span data-ttu-id="9e900-115">**\_contador bruto de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-115">**PDH\_RAW\_COUNTER**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [<span data-ttu-id="9e900-116">**\_item de \_ contador \_ bruto de PDH**</span><span class="sxs-lookup"><span data-stu-id="9e900-116">**PDH\_RAW\_COUNTER\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [<span data-ttu-id="9e900-117">**\_registro de \_ log \_ bruto do PDH**</span><span class="sxs-lookup"><span data-stu-id="9e900-117">**PDH\_RAW\_LOG\_RECORD**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [<span data-ttu-id="9e900-118">**Estatísticas de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-118">**PDH\_STATISTICS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [<span data-ttu-id="9e900-119">**\_informações de tempo de PDH \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-119">**PDH\_TIME\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a><span data-ttu-id="9e900-120">Estruturas de consumidor de PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="9e900-120">PerfLib V2 Consumer structures</span></span>

<span data-ttu-id="9e900-121">Os consumidores que usam as funções de [consumidor da PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) usam as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="9e900-121">Consumers that use the [PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="9e900-122">**\_dados do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-122">**PERF\_COUNTER\_DATA**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [<span data-ttu-id="9e900-123">**\_cabeçalho do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-123">**PERF\_COUNTER\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [<span data-ttu-id="9e900-124">**\_identificador do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-124">**PERF\_COUNTER\_IDENTIFIER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [<span data-ttu-id="9e900-125">**\_informações de \_ reg do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-125">**PERF\_COUNTER\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [<span data-ttu-id="9e900-126">**informações de reg do contador de desempenho \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-126">**PERF\_COUNTERSET\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [<span data-ttu-id="9e900-127">**\_cabeçalho de dados de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-127">**PERF\_DATA\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [<span data-ttu-id="9e900-128">**\_cabeçalho de instância de perf \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-128">**PERF\_INSTANCE\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [<span data-ttu-id="9e900-129">**\_vários \_ contadores de desempenho**</span><span class="sxs-lookup"><span data-stu-id="9e900-129">**PERF\_MULTI\_COUNTERS**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [<span data-ttu-id="9e900-130">**\_várias \_ instâncias de desempenho**</span><span class="sxs-lookup"><span data-stu-id="9e900-130">**PERF\_MULTI\_INSTANCES**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [<span data-ttu-id="9e900-131">**cabeçalho do buffer da cadeia de \_ caracteres perf \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-131">**PERF\_STRING\_BUFFER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [<span data-ttu-id="9e900-132">**cabeçalho do contador de cadeia de caracteres de desempenho \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-132">**PERF\_STRING\_COUNTER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a><span data-ttu-id="9e900-133">Estruturas de provedor de PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="9e900-133">PerfLib V2 Provider structures</span></span>

<span data-ttu-id="9e900-134">Os [provedores de dados de desempenho v2](providing-counter-data-using-version-2-0.md) usam as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="9e900-134">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following structures:</span></span>

- [<span data-ttu-id="9e900-135">**\_identidade do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-135">**PERF\_COUNTER\_IDENTITY**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="9e900-136">**\_informações do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-136">**PERF\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="9e900-137">**informações do contador de desempenho \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-137">**PERF\_COUNTERSET\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="9e900-138">**instância do contador de desempenho \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-138">**PERF\_COUNTERSET\_INSTANCE**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [<span data-ttu-id="9e900-139">**\_contexto do provedor de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-139">**PERF\_PROVIDER\_CONTEXT**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a><span data-ttu-id="9e900-140">Estruturas de DLL de desempenho</span><span class="sxs-lookup"><span data-stu-id="9e900-140">Performance DLL structures</span></span>

<span data-ttu-id="9e900-141">Os [provedores de DLL de extensão de desempenho](providing-counter-data-using-a-performance-dll.md) e os [consumidores que usam as funções de registro para consumir dados de contador](using-the-registry-functions-to-consume-counter-data.md) usam as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="9e900-141">[Performance extension DLL providers](providing-counter-data-using-a-performance-dll.md) and [consumers that use the registry functions to consume counter data](using-the-registry-functions-to-consume-counter-data.md) use the following structures:</span></span>

- [<span data-ttu-id="9e900-142">**\_bloco de contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-142">**PERF\_COUNTER\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [<span data-ttu-id="9e900-143">**\_definição do contador de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-143">**PERF\_COUNTER\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [<span data-ttu-id="9e900-144">**\_bloco de dados de desempenho \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-144">**PERF\_DATA\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [<span data-ttu-id="9e900-145">**\_definição de instância de perf \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-145">**PERF\_INSTANCE\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [<span data-ttu-id="9e900-146">**\_tipo de objeto perf \_**</span><span class="sxs-lookup"><span data-stu-id="9e900-146">**PERF\_OBJECT\_TYPE**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
