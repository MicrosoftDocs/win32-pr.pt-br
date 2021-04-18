---
description: Use as funções a seguir para consumir e fornecer dados de desempenho.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Funções de contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787475"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="a4a72-103">Funções de contadores de desempenho</span><span class="sxs-lookup"><span data-stu-id="a4a72-103">Performance Counters Functions</span></span>

<span data-ttu-id="a4a72-104">Use as funções a seguir para consumir e fornecer dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a4a72-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="a4a72-105">Funções de consumidor</span><span class="sxs-lookup"><span data-stu-id="a4a72-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="a4a72-106">Funções de PDH (auxiliar de dados de desempenho)</span><span class="sxs-lookup"><span data-stu-id="a4a72-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="a4a72-107">Use as funções de PDH (auxiliar de dados de desempenho) para consumir dados de desempenho de provedores de dados de desempenho v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="a4a72-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="a4a72-108">Os aplicativos do Windows OneCore não podem usar as funções PDH.</span><span class="sxs-lookup"><span data-stu-id="a4a72-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="a4a72-109">Se você estiver escrevendo aplicativos do Windows OneCore, use as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="a4a72-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="a4a72-110">*CounterPathCallBack*</span><span class="sxs-lookup"><span data-stu-id="a4a72-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="a4a72-111">**PdhAddCounter**</span><span class="sxs-lookup"><span data-stu-id="a4a72-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="a4a72-112">**PdhAddEnglishCounter**</span><span class="sxs-lookup"><span data-stu-id="a4a72-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="a4a72-113">**PdhBindInputDataSource**</span><span class="sxs-lookup"><span data-stu-id="a4a72-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="a4a72-114">**PdhBrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="a4a72-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="a4a72-115">**PdhBrowseCountersH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="a4a72-116">**PdhCalculateCounterFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="a4a72-117">**PdhCloseLog**</span><span class="sxs-lookup"><span data-stu-id="a4a72-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="a4a72-118">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="a4a72-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="a4a72-119">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="a4a72-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="a4a72-120">**PdhCollectQueryDataEx**</span><span class="sxs-lookup"><span data-stu-id="a4a72-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="a4a72-121">**PdhCollectQueryDataWithTime**</span><span class="sxs-lookup"><span data-stu-id="a4a72-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="a4a72-122">**PdhComputeCounterStatistics**</span><span class="sxs-lookup"><span data-stu-id="a4a72-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="a4a72-123">**PdhConnectMachine**</span><span class="sxs-lookup"><span data-stu-id="a4a72-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="a4a72-124">**PdhEnumLogSetNames**</span><span class="sxs-lookup"><span data-stu-id="a4a72-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="a4a72-125">**PdhEnumMachines**</span><span class="sxs-lookup"><span data-stu-id="a4a72-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="a4a72-126">**PdhEnumMachinesH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="a4a72-127">**PdhEnumObjectItems**</span><span class="sxs-lookup"><span data-stu-id="a4a72-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="a4a72-128">**PdhEnumObjectItemsH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="a4a72-129">**PdhEnumObjects**</span><span class="sxs-lookup"><span data-stu-id="a4a72-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="a4a72-130">**PdhEnumObjectsH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="a4a72-131">**PdhExpandCounterPath**</span><span class="sxs-lookup"><span data-stu-id="a4a72-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="a4a72-132">**PdhExpandWildCardPath**</span><span class="sxs-lookup"><span data-stu-id="a4a72-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="a4a72-133">**PdhExpandWildCardPathH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="a4a72-134">**PdhFormatFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="a4a72-135">**PdhGetCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="a4a72-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="a4a72-136">**PdhGetCounterTimeBase**</span><span class="sxs-lookup"><span data-stu-id="a4a72-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="a4a72-137">**PdhGetDataSourceTimeRange**</span><span class="sxs-lookup"><span data-stu-id="a4a72-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="a4a72-138">**PdhGetDataSourceTimeRangeH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="a4a72-139">**PdhGetDefaultPerfCounter**</span><span class="sxs-lookup"><span data-stu-id="a4a72-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="a4a72-140">**PdhGetDefaultPerfCounterH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="a4a72-141">**PdhGetDefaultPerfObject**</span><span class="sxs-lookup"><span data-stu-id="a4a72-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="a4a72-142">**PdhGetDefaultPerfObjectH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="a4a72-143">**PdhGetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="a4a72-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="a4a72-144">**PdhGetFormattedCounterArray**</span><span class="sxs-lookup"><span data-stu-id="a4a72-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="a4a72-145">**PdhGetFormattedCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="a4a72-146">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="a4a72-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="a4a72-147">**PdhGetRawCounterArray**</span><span class="sxs-lookup"><span data-stu-id="a4a72-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="a4a72-148">**PdhGetRawCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="a4a72-149">**PdhIsRealTimeQuery**</span><span class="sxs-lookup"><span data-stu-id="a4a72-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="a4a72-150">**PdhLookupPerfIndexByName**</span><span class="sxs-lookup"><span data-stu-id="a4a72-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="a4a72-151">**PdhLookupPerfNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="a4a72-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="a4a72-152">**PdhMakeCounterPath**</span><span class="sxs-lookup"><span data-stu-id="a4a72-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="a4a72-153">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="a4a72-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="a4a72-154">**PdhOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="a4a72-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="a4a72-155">**PdhOpenQueryH**</span><span class="sxs-lookup"><span data-stu-id="a4a72-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="a4a72-156">**PdhParseCounterPath**</span><span class="sxs-lookup"><span data-stu-id="a4a72-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="a4a72-157">**PdhParseInstanceName**</span><span class="sxs-lookup"><span data-stu-id="a4a72-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="a4a72-158">**PdhReadRawLogRecord**</span><span class="sxs-lookup"><span data-stu-id="a4a72-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="a4a72-159">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="a4a72-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="a4a72-160">**PdhSelectDataSource**</span><span class="sxs-lookup"><span data-stu-id="a4a72-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="a4a72-161">**PdhSetCounterScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="a4a72-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="a4a72-162">**PdhSetDefaultRealTimeDataSource**</span><span class="sxs-lookup"><span data-stu-id="a4a72-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="a4a72-163">**PdhSetQueryTimeRange**</span><span class="sxs-lookup"><span data-stu-id="a4a72-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="a4a72-164">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="a4a72-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="a4a72-165">**PdhUpdateLogFileCatalog**</span><span class="sxs-lookup"><span data-stu-id="a4a72-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="a4a72-166">**PdhValidatePath**</span><span class="sxs-lookup"><span data-stu-id="a4a72-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="a4a72-167">**PdhValidatePathEx**</span><span class="sxs-lookup"><span data-stu-id="a4a72-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="a4a72-168">Funções de consumidor de PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="a4a72-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="a4a72-169">Use as funções de consumidor do PerfLib v2 para consumir dados de desempenho de provedores de dados de desempenho v2 se você não puder usar as funções PDH (auxiliar de dados de desempenho).</span><span class="sxs-lookup"><span data-stu-id="a4a72-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="a4a72-170">Essas funções podem ser usadas ao escrever aplicativos OneCore para coletar conjuntos de registros v2 ou quando você precisa coletar conjuntos de valores v2 específicos com dependências mínimas e sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="a4a72-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="a4a72-171">As funções de consumidor do PerfLib v2 são mais difíceis de usar do que as funções PDH (auxiliar de dados de desempenho) e dão suporte apenas à coleta de dados de provedores v2.</span><span class="sxs-lookup"><span data-stu-id="a4a72-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="a4a72-172">As funções de PDH devem ser preferenciais para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a4a72-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="a4a72-173">**PerfAddCounters**</span><span class="sxs-lookup"><span data-stu-id="a4a72-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="a4a72-174">**PerfCloseQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="a4a72-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="a4a72-175">**PerfDeleteCounters**</span><span class="sxs-lookup"><span data-stu-id="a4a72-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="a4a72-176">**PerfEnumerateCounterSet**</span><span class="sxs-lookup"><span data-stu-id="a4a72-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="a4a72-177">**PerfEnumerateCounterSetInstances**</span><span class="sxs-lookup"><span data-stu-id="a4a72-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="a4a72-178">**PerfOpenQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="a4a72-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="a4a72-179">**PerfQueryCounterData**</span><span class="sxs-lookup"><span data-stu-id="a4a72-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="a4a72-180">**PerfQueryCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="a4a72-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="a4a72-181">**PerfQueryCounterSetRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="a4a72-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="a4a72-182">Funções de provedor</span><span class="sxs-lookup"><span data-stu-id="a4a72-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="a4a72-183">Funções de provedor de PerfLib v2</span><span class="sxs-lookup"><span data-stu-id="a4a72-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="a4a72-184">Os [provedores de dados de desempenho v2](providing-counter-data-using-version-2-0.md) usam as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="a4a72-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="a4a72-185">*AllocateMemory*</span><span class="sxs-lookup"><span data-stu-id="a4a72-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="a4a72-186">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="a4a72-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="a4a72-187">**Prolimpeza**</span><span class="sxs-lookup"><span data-stu-id="a4a72-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="a4a72-188">**Preinicializar**</span><span class="sxs-lookup"><span data-stu-id="a4a72-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="a4a72-189">*FreeMemory*</span><span class="sxs-lookup"><span data-stu-id="a4a72-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="a4a72-190">**PerfCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="a4a72-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="a4a72-191">**PerfDecrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="a4a72-192">**PerfDecrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="a4a72-193">**PerfDeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="a4a72-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="a4a72-194">**PerfIncrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="a4a72-195">**PerfIncrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="a4a72-196">**PerfQueryInstance**</span><span class="sxs-lookup"><span data-stu-id="a4a72-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="a4a72-197">**PerfSetCounterSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a4a72-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="a4a72-198">**PerfSetULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="a4a72-199">**PerfSetULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="a4a72-200">**PerfSetCounterRefValue**</span><span class="sxs-lookup"><span data-stu-id="a4a72-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="a4a72-201">**PerfStartProvider**</span><span class="sxs-lookup"><span data-stu-id="a4a72-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="a4a72-202">**PerfStartProviderEx**</span><span class="sxs-lookup"><span data-stu-id="a4a72-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="a4a72-203">**PerfStopProvider**</span><span class="sxs-lookup"><span data-stu-id="a4a72-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="a4a72-204">Para instalar e desinstalar provedores v2, use as ferramentas **lodctr** e **Unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="a4a72-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="a4a72-205">As funções **LoadPerfCounterTextStrings** e **UnloadPerfCounterTextStrings** não podem ser usadas para instalar e desinstalar provedores v2.</span><span class="sxs-lookup"><span data-stu-id="a4a72-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="a4a72-206">Funções de DLL de desempenho</span><span class="sxs-lookup"><span data-stu-id="a4a72-206">Performance DLL functions</span></span>

<span data-ttu-id="a4a72-207">Os [provedores de dados de desempenho v1](providing-counter-data-using-a-performance-dll.md) implementam uma DLL que fornece as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="a4a72-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="a4a72-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="a4a72-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="a4a72-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="a4a72-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="a4a72-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a4a72-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="a4a72-211">Devido a problemas significativos de desempenho e confiabilidade, os provedores de dados de desempenho v1 são preteridos.</span><span class="sxs-lookup"><span data-stu-id="a4a72-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="a4a72-212">Embora você ainda possa usar uma DLL de extensão de desempenho para fornecer dados de contador, é recomendável [criar um provedor v2](providing-counter-data-using-version-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a72-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="a4a72-213">Você também é incentivado a substituir provedores v1 existentes por provedores v2.</span><span class="sxs-lookup"><span data-stu-id="a4a72-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="a4a72-214">Os provedores v1 podem ser instalados e desinstalados usando as ferramentas **lodctr** e **Unlodctr** ou chamando as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="a4a72-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="a4a72-215">**LoadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="a4a72-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="a4a72-216">**UnloadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="a4a72-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
