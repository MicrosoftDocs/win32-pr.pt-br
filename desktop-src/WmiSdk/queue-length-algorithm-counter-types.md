---
description: Os tipos de contadores de algoritmo de comprimento de fila incrementam o número de itens em uma fila em cada intervalo de amostragem, conforme especificado pela propriedade Frequency apropriada&\# 8212; Frequência \_ PerfTime e assim por diante.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de comprimento de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165221"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="e7399-103">Tipos de contadores de algoritmo de comprimento de fila</span><span class="sxs-lookup"><span data-stu-id="e7399-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="e7399-104">Os tipos de contadores de algoritmo de comprimento de fila incrementam o número de itens em uma fila em cada intervalo de amostragem, conforme especificado pela frequência de propriedade de frequência apropriada \_ e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e7399-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="e7399-105">O resultado de cooked divide pelo número de amostras para produzir o comprimento médio da fila.</span><span class="sxs-lookup"><span data-stu-id="e7399-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="e7399-106">Um exemplo é a propriedade **AvgDiskQueueLength** no [**\_ LogicalDisk do PerfRawData de \_ perfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) que usa o tipo de contador contador de desempenho de \_ \_ 100 NS \_ QUEUELEN \_ tipo.</span><span class="sxs-lookup"><span data-stu-id="e7399-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="e7399-107">Constante de tipo</span><span class="sxs-lookup"><span data-stu-id="e7399-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="e7399-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7399-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7399-109">[Desempenho \_ COUNTER \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523008</span><span class="sxs-lookup"><span data-stu-id="e7399-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="e7399-110">Duração média de uma fila para um recurso ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="e7399-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="e7399-111">Ele mostra a diferença entre os tamanhos de fila observados durante os últimos dois intervalos de amostragem divididos pela duração do intervalo.</span><span class="sxs-lookup"><span data-stu-id="e7399-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="e7399-112">[Desempenho \_ COUNTER \_ grande \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523264</span><span class="sxs-lookup"><span data-stu-id="e7399-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="e7399-113">Duração média de uma fila para um recurso ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="e7399-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="e7399-114">Contadores desse tipo mostram a diferença entre os tamanhos de fila observados durante os últimos dois intervalos de amostragem divididos pela duração do intervalo.</span><span class="sxs-lookup"><span data-stu-id="e7399-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="e7399-115">[Desempenho \_ COUNTER \_ 100ns \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 5571840</span><span class="sxs-lookup"><span data-stu-id="e7399-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="e7399-116">Duração média de uma fila para um recurso ao longo do tempo em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e7399-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="e7399-117">[Desempenho \_ \_Tipo de \_ \_ QUEUELEN \_ de tempo de OBJ de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 6620416</span><span class="sxs-lookup"><span data-stu-id="e7399-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="e7399-118">Hora em que um objeto está em uma fila.</span><span class="sxs-lookup"><span data-stu-id="e7399-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="e7399-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7399-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7399-120">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="e7399-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

