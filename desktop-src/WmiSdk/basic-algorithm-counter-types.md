---
description: Representam diferenças entre amostras ao longo do tempo e geralmente usa um valor base para o cálculo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipos de contador de algoritmos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797632"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="ee0c0-103">Tipos de contador de algoritmos básicos</span><span class="sxs-lookup"><span data-stu-id="ee0c0-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="ee0c0-104">Os tipos de contador de algoritmos básicos geralmente representam as diferenças entre os exemplos ao longo do tempo e geralmente usam um valor base para o cálculo.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="ee0c0-105">Por exemplo, a propriedade **PercentFreeSpace** da classe [**de \_ PhysicalDisk do PerfFormattedData de \_ perfdisk \_ do Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa a proporção do espaço livre disponível na unidade de disco físico para o espaço utilizável total fornecido pela unidade de disco físico selecionada.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="ee0c0-106">Essa classe também contém o valor base, **PercentFreeSpace \_ base**.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="ee0c0-107">A porcentagem de espaço livre em disco é obtida com a divisão de **PercentFreeSpace** por **PercentFreeSpace \_ base** e a multiplicação por 100%.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="ee0c0-108">Os algoritmos básicos na tabela a seguir são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="ee0c0-109">Constante de tipo</span><span class="sxs-lookup"><span data-stu-id="ee0c0-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="ee0c0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee0c0-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0c0-111">[Desempenho \_ \_Fração bruta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 537003008</span><span class="sxs-lookup"><span data-stu-id="ee0c0-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="ee0c0-112">Taxa de um subconjunto para seu conjunto como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="ee0c0-113">Esse tipo de contador exibe apenas a porcentagem atual, não uma média ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="ee0c0-114">[Desempenho \_ \_Fração de exemplo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 549585920</span><span class="sxs-lookup"><span data-stu-id="ee0c0-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="ee0c0-115">Taxa média de ocorrências para todas as operações durante os dois últimos intervalos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="ee0c0-116">Esse tipo de contador requer uma propriedade base com o \_ tipo de contador de base perf Sample \_ .</span><span class="sxs-lookup"><span data-stu-id="ee0c0-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="ee0c0-117">[Desempenho \_ \_Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal do contador 4195328</span><span class="sxs-lookup"><span data-stu-id="ee0c0-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="ee0c0-118">Esse tipo de contador mostra a alteração no atributo medido entre os dois intervalos de amostra mais recentes.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="ee0c0-119">[Desempenho \_ Decimal \_ \_ Delta grande do contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584</span><span class="sxs-lookup"><span data-stu-id="ee0c0-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="ee0c0-120">O mesmo que \_ o Delta do contador de desempenho \_ , mas uma representação de 64 bits para valores maiores.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="ee0c0-121">[Desempenho \_ \_Tempo decorrido](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 807666944</span><span class="sxs-lookup"><span data-stu-id="ee0c0-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="ee0c0-122">Tempo total entre o início do processo e a hora em que esse valor é calculado.</span><span class="sxs-lookup"><span data-stu-id="ee0c0-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ee0c0-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee0c0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee0c0-124">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="ee0c0-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

