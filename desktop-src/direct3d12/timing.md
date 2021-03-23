---
title: Tempo (gráficos do Direct3D 12)
description: Esta seção aborda a consulta de carimbos de data/hora e a calibragem dos contadores de timestamp e da CPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548321"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="74b0b-103">Tempo (gráficos do Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="74b0b-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="74b0b-104">Esta seção aborda a consulta de carimbos de data/hora e a calibragem dos contadores de timestamp e da CPU.</span><span class="sxs-lookup"><span data-stu-id="74b0b-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="74b0b-105">Frequência de carimbo de hora</span><span class="sxs-lookup"><span data-stu-id="74b0b-105">Timestamp frequency</span></span>

<span data-ttu-id="74b0b-106">Seu aplicativo pode consultar a frequência de carimbo de data/hora de GPU em uma base de fila por comando (consulte o método [**ID3D12CommandQueue:: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).</span><span class="sxs-lookup"><span data-stu-id="74b0b-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="74b0b-107">A frequência retornada é medida em Hz (tiques/s).</span><span class="sxs-lookup"><span data-stu-id="74b0b-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="74b0b-108">Se a fila de comandos especificada não oferecer suporte a carimbos de data/hora (consulte a tabela na seção [consultas](queries.md) ), essa API falhará (e retornará **E_FAIL**).</span><span class="sxs-lookup"><span data-stu-id="74b0b-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="74b0b-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) sempre dão suporte a carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="74b0b-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="74b0b-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) opcionalmente dá suporte a carimbos de data/hora se o membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) for **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="74b0b-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="74b0b-111">Calibragem de timestamp</span><span class="sxs-lookup"><span data-stu-id="74b0b-111">Timestamp calibration</span></span>

<span data-ttu-id="74b0b-112">O D3D12 permite que os aplicativos correlacionem os resultados obtidos de consultas de carimbo de data/hora com os resultados obtidos da chamada `QueryPerformanceCounter` .</span><span class="sxs-lookup"><span data-stu-id="74b0b-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="74b0b-113">Isso é habilitado pela chamada [**ID3D12CommandQueue:: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span><span class="sxs-lookup"><span data-stu-id="74b0b-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="74b0b-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) amostra o contador de carimbo de data/hora da GPU para uma determinada fila de comandos e amostra o contador de CPU via `QueryPerformanceCounter` quase ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="74b0b-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="74b0b-115">Novamente, essa API falhará (retornando E \_ falhará) se a fila de comandos especificada não oferecer suporte a carimbos de data/hora (consulte a tabela no tópico [consultas](queries.md) ).</span><span class="sxs-lookup"><span data-stu-id="74b0b-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="74b0b-116">Observe que os contadores de carimbo de data/hora da GPU e da CPU não estão necessariamente diretamente relacionados à velocidade do relógio desses processadores, mas sim para trabalhar com tiques de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="74b0b-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="74b0b-117">Consultas de carimbo de hora</span><span class="sxs-lookup"><span data-stu-id="74b0b-117">Timestamp queries</span></span>

<span data-ttu-id="74b0b-118">Você pode obter carimbos de data/hora como parte de uma lista de comandos (em vez de uma chamada do lado da CPU em uma fila de comando) por meio de consultas de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="74b0b-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="74b0b-119">(Consulte [consultas](queries.md) para obter mais informações sobre consultas em geral).</span><span class="sxs-lookup"><span data-stu-id="74b0b-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="74b0b-120">Todas as consultas de carimbo de data/hora usam o tipo [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) para a consulta real.</span><span class="sxs-lookup"><span data-stu-id="74b0b-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="74b0b-121">No entanto, devido a limitações de hardware, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usar um [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) diferente daquele que [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usa.</span><span class="sxs-lookup"><span data-stu-id="74b0b-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="74b0b-122">As filas de computação e diretas usam [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="74b0b-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="74b0b-123">As filas de cópia usam [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="74b0b-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="74b0b-124">As consultas de fila de cópia só têm suporte se o membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) for **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="74b0b-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="74b0b-125">As consultas de carimbo de data/hora, uma vez resolvidas por meio de [**ID3D12GraphicsCommandList:: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), são um **UINT64** que representa tiques, como é retornado por [**ID3D12CommandQueue:: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), e como tal, ele deve ser dividido pela frequência de fila para obter o comprimento em segundos.</span><span class="sxs-lookup"><span data-stu-id="74b0b-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74b0b-126">Para exatidão, use a aritmética de ponto flutuante ao calcular o segundo ou intervalos de milissegundos de carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="74b0b-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="74b0b-127">Por exemplo, use `queriedTicks / (double)Frequency` ao invés de `queriedTicks / Frequency`.</span><span class="sxs-lookup"><span data-stu-id="74b0b-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74b0b-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74b0b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b0b-129">Contadores e consultas</span><span class="sxs-lookup"><span data-stu-id="74b0b-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="74b0b-130">**ID3D12Device::SetStablePowerState**</span><span class="sxs-lookup"><span data-stu-id="74b0b-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="74b0b-131">**ID3D12Object:: SetName**</span><span class="sxs-lookup"><span data-stu-id="74b0b-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="74b0b-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="74b0b-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="74b0b-133">Medição de desempenho</span><span class="sxs-lookup"><span data-stu-id="74b0b-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>
