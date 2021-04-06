---
description: O desempenho formatado do WMI de alto desempenho Provedor de Dados calcula os tipos de contadores estatísticos em um número especificado de amostras de dados de contador bruto.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipos de contadores estatísticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011347"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="a067c-103">Tipos de contadores estatísticos</span><span class="sxs-lookup"><span data-stu-id="a067c-103">Statistical Counter Types</span></span>

<span data-ttu-id="a067c-104">O [desempenho formatado](formatted-performance-data-provider.md) do WMI de alto desempenho provedor de dados calcula os tipos de contadores estatísticos em um número especificado de amostras de dados de contador bruto.</span><span class="sxs-lookup"><span data-stu-id="a067c-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="a067c-105">Os algoritmos para os tipos de contador não exigem Propriedades de frequência ou carimbo de data/hora herdadas (como **carimbo de data/hora \_** ou **frequência \_ PerfTime**) que outros tipos de contador exigem.</span><span class="sxs-lookup"><span data-stu-id="a067c-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="a067c-106">Em vez disso, os tipos de contadores estatísticos dão suporte a um **qualificador** que identifica quantas amostras usar.</span><span class="sxs-lookup"><span data-stu-id="a067c-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="a067c-107">Um exemplo é coletado quando o método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) é chamado para o objeto de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a067c-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="a067c-108">Para scripts, use o método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="a067c-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="a067c-109">Os dados calculados contêm o resultado do cálculo realizado no número **SampleWindow** de amostras da propriedade dados brutos.</span><span class="sxs-lookup"><span data-stu-id="a067c-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="a067c-110">Os dados brutos do cálculo vêm de frm o nome da propriedade especificada no qualificador do **contador** .</span><span class="sxs-lookup"><span data-stu-id="a067c-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="a067c-111">Para obter mais informações, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md) e [acessando classes de desempenho de WMI pré-instalado](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="a067c-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="a067c-112">Constante de tipo</span><span class="sxs-lookup"><span data-stu-id="a067c-112">CounterType Constant</span></span>                    | <span data-ttu-id="a067c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a067c-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a067c-114">média de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="a067c-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="a067c-115">Soma observações repetidas de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e divide a soma pelo número de observações.</span><span class="sxs-lookup"><span data-stu-id="a067c-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="a067c-116">COOKER \_ Max</span><span class="sxs-lookup"><span data-stu-id="a067c-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="a067c-117">Maior valor de um conjunto de observações de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="a067c-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="a067c-118">COOKER \_ mín.</span><span class="sxs-lookup"><span data-stu-id="a067c-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="a067c-119">Menor valor de um conjunto de observações de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="a067c-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="a067c-120">intervalo de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="a067c-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="a067c-121">Diferença entre os valores [mínimo](cooker-min.md) e [máximo](cooker-max.md) para um conjunto de observações brutas de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="a067c-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="a067c-122">variância de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="a067c-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="a067c-123">Medida de variabilidade que pode ser usada para caracterizar a dispersão de um conjunto de observações brutas de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="a067c-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="a067c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a067c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a067c-125">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="a067c-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="a067c-126">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="a067c-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="a067c-127">Atualizando dados do WMI em scripts</span><span class="sxs-lookup"><span data-stu-id="a067c-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="a067c-128">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="a067c-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="a067c-129">Acessando dados de desempenho em C++</span><span class="sxs-lookup"><span data-stu-id="a067c-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
