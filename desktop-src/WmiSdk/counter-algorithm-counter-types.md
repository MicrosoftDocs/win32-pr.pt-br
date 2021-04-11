---
description: Os tipos de contador de algoritmos de contador podem calcular taxas ou médias de bytes para uma amostra ou ao longo de um período de tempo para uma operação específica.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296998"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="5bd1f-103">Tipos de contadores de algoritmo de contador</span><span class="sxs-lookup"><span data-stu-id="5bd1f-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="5bd1f-104">Os tipos de contador de algoritmos de contador podem calcular taxas ou médias de bytes para uma amostra ou ao longo de um período de tempo para uma operação específica.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="5bd1f-105">A propriedade **AvgDiskBytesPerTransfer** na classe [**de \_ PhysicalDisk do PerfRawData de \_ perfdisk \_ do Win32**](/previous-versions//aa394308(v=vs.85)) usa o tipo de número de \_ massa médio de perf \_ .</span><span class="sxs-lookup"><span data-stu-id="5bd1f-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="5bd1f-106">Nesse caso, a transferência é a operação e o número acumulado de bytes que são enviados são os dados do contador.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="5bd1f-107">Para quaisquer dois exemplos, dividir a diferença de bytes acumulados pela diferença em acumular transferências produzirá o número médio de bytes por transferência durante o período entre os exemplos.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="5bd1f-108">Os seguintes algoritmos de contador são fornecidos:</span><span class="sxs-lookup"><span data-stu-id="5bd1f-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="5bd1f-109">CounterType</span><span class="sxs-lookup"><span data-stu-id="5bd1f-109">CounterType</span></span>                                                                                              | <span data-ttu-id="5bd1f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bd1f-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd1f-111">[Desempenho \_ MÉDIA decimal \_ em massa](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073874176</span><span class="sxs-lookup"><span data-stu-id="5bd1f-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="5bd1f-112">Número de itens processados, em média, durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="5bd1f-113">Esse tipo de contador exibe uma taxa dos itens processados (como bytes enviados) para o número de operações concluídas e requer uma propriedade base com a \_ \_ base média de perf como o tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="5bd1f-114">[Desempenho \_ \_Contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))de contadores decimal 272696320</span><span class="sxs-lookup"><span data-stu-id="5bd1f-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="5bd1f-115">Número médio de operações concluídas durante cada segundo do intervalo de amostragem.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="5bd1f-116">.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="5bd1f-117">[Desempenho \_ \_Contador de exemplo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4260864</span><span class="sxs-lookup"><span data-stu-id="5bd1f-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="5bd1f-118">Número médio de operações concluídas em um segundo.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="5bd1f-119">Esse tipo de contador requer uma propriedade base com o tipo de contador \_ base de exemplo perf \_ .</span><span class="sxs-lookup"><span data-stu-id="5bd1f-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="5bd1f-120">[Desempenho \_ \_ \_ Contagem de massa de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 272696576</span><span class="sxs-lookup"><span data-stu-id="5bd1f-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="5bd1f-121">Número médio de operações concluídas durante cada segundo do intervalo de amostragem.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="5bd1f-122">Esse tipo de contador é o mesmo que o \_ tipo de contador de contador de desempenho \_ , mas usa campos maiores para acomodar valores maiores.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="5bd1f-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bd1f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bd1f-124">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="5bd1f-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

