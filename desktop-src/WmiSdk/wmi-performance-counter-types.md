---
description: O tipo de contador de desempenho designa uma fórmula necessária para obter contadores de desempenho calculados. Esses são os mesmos tipos de contador usados pelo monitoramento de desempenho do Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipos de contador de desempenho WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091370"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="0c82e-104">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="0c82e-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="0c82e-105">O [tipo de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) de desempenho designa uma fórmula necessária para obter contadores de desempenho calculados.</span><span class="sxs-lookup"><span data-stu-id="0c82e-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="0c82e-106">Esses são os mesmos tipos de contador usados pelo [monitoramento de desempenho](/windows/desktop/PerfCtrs/performance-counters-portal)do Windows.</span><span class="sxs-lookup"><span data-stu-id="0c82e-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="0c82e-107">Nas classes de desempenho WMI, os dados brutos para a fórmula de tipo de contador vêm de uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e o resultado calculado é encontrado na propriedade de mesmo nome de uma classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondente.</span><span class="sxs-lookup"><span data-stu-id="0c82e-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="0c82e-108">Os tipos de contadores aparecem como o qualificador de **tipo** de propriedade nas classes [**\_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e como o qualificador de **Culináriatype** para propriedades em classes [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="0c82e-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="0c82e-109">Por exemplo, a propriedade **AvgDiskBytesPerRead** na classe [**\_ PerfRawData do \_ backfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) é a fonte de dados brutos para a propriedade **AvgDiskBytesPerRead** na classe [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), que contém os mesmos dados, conforme mostrado no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="0c82e-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="0c82e-110">A lista a seguir organiza as descrições de tipo de contador por tipo funcional:</span><span class="sxs-lookup"><span data-stu-id="0c82e-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="0c82e-111">Tipos de contador base</span><span class="sxs-lookup"><span data-stu-id="0c82e-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="0c82e-112">Tipos de contador de algoritmos básicos</span><span class="sxs-lookup"><span data-stu-id="0c82e-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="0c82e-113">Tipos de contadores de algoritmo de contador</span><span class="sxs-lookup"><span data-stu-id="0c82e-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="0c82e-114">Tipos de contadores não computacionais</span><span class="sxs-lookup"><span data-stu-id="0c82e-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="0c82e-115">Tipos de contadores de algoritmo de timer de precisão</span><span class="sxs-lookup"><span data-stu-id="0c82e-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="0c82e-116">Tipos de contadores de algoritmo de comprimento de fila</span><span class="sxs-lookup"><span data-stu-id="0c82e-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="0c82e-117">Tipos de contadores estatísticos</span><span class="sxs-lookup"><span data-stu-id="0c82e-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="0c82e-118">Tipos de contadores de algoritmo de temporizador</span><span class="sxs-lookup"><span data-stu-id="0c82e-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 
