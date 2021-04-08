---
description: A fórmula do tipo de contador de variância de COOKER \_ fornece variabilidade que usa para caracterizar a dispersão para um conjunto de observações brutas de uma propriedade em uma instância do Win32 \_ PerfRawData.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010820"
---
# <a name="cooker_variance"></a><span data-ttu-id="87332-103">variância de COOKER \_</span><span class="sxs-lookup"><span data-stu-id="87332-103">COOKER\_VARIANCE</span></span>

<span data-ttu-id="87332-104">A fórmula do tipo de contador de variância de COOKER \_ fornece variabilidade que usa para caracterizar a dispersão para um conjunto de observações brutas de uma propriedade em uma instância do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="87332-104">The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance.</span></span> <span data-ttu-id="87332-105">A variação é calculada pela divisão da soma do quadrado do desvio da média de cada contador pelo número de contadores.</span><span class="sxs-lookup"><span data-stu-id="87332-105">The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters.</span></span> <span data-ttu-id="87332-106">Em outras palavras, a variação é a média dos desvios quadrados da média de cada contador.</span><span class="sxs-lookup"><span data-stu-id="87332-106">In other words, the variance is the average of the squared deviations from the mean for each counter.</span></span> <span data-ttu-id="87332-107">Esse tipo de contador é definido somente dentro do WMI e não está disponível para as tecnologias de monitoramento de desempenho, como [contadores de desempenho versão 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="87332-107">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="87332-108">Para obter mais informações sobre a fórmula de tipo de contador, consulte [tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="87332-108">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="87332-109">Para obter mais informações sobre provedores de alto desempenho e scripts, consulte [tipos de contador de desempenho WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="87332-109">For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="87332-110">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="87332-110">Example Code</span></span>

<span data-ttu-id="87332-111">Para obter exemplos de código, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="87332-111">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87332-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87332-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87332-113">Tipos de contadores estatísticos</span><span class="sxs-lookup"><span data-stu-id="87332-113">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="87332-114">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="87332-114">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
