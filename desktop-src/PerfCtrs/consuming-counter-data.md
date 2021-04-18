---
description: 'Você pode consumir dados de desempenho usando uma das seguintes interfaces: a interface do auxiliar de dados de desempenho (PDH), que fornece acesso de alto nível aos dados dos provedores de contador de desempenho da versão 1 e da versão 2. A interface do registro, que fornece acesso de baixo nível aos dados de provedores de contador de desempenho. A interface de biblioteca de desempenho, que fornece acesso direto aos dados dos provedores de contador de desempenho da versão 2. A interface PDH é mais fácil de usar do que a interface do registro e é recomendada para a maioria das tarefas de coleta de dados de desempenho. A interface PDH é essencialmente uma abstração de nível superior da funcionalidade fornecida pela interface do registro. Use a interface de biblioteca de desempenho somente se você não puder usar as funções de camada de abstração de PDH.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Consumindo dados do contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753243"
---
# <a name="consuming-counter-data"></a><span data-ttu-id="07c3c-105">Consumindo dados do contador</span><span class="sxs-lookup"><span data-stu-id="07c3c-105">Consuming Counter Data</span></span>

<span data-ttu-id="07c3c-106">Os programas que desejam ler e usar os dados do contador de desempenho do Windows podem usar uma das várias interfaces conforme apropriado para o cenário.</span><span class="sxs-lookup"><span data-stu-id="07c3c-106">Programs that want to read and make use of Windows Performance Counter data can use one of several interfaces as appropriate for the scenario.</span></span>

- <span data-ttu-id="07c3c-107">Os scripts podem usar as [classes do contador de desempenho WMI](/windows/desktop/WmiSdk/monitoring-performance-data) ou a ferramenta [TypePerf](/windows-server/administration/windows-commands/typeperf) .</span><span class="sxs-lookup"><span data-stu-id="07c3c-107">Scripts can use the [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) or the [TypePerf](/windows-server/administration/windows-commands/typeperf) tool.</span></span>
- <span data-ttu-id="07c3c-108">Os programas .NET podem usar a [classe PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).</span><span class="sxs-lookup"><span data-stu-id="07c3c-108">.NET programs can use the [PerformanceCounter Class](/dotnet/api/system.diagnostics.performancecounter).</span></span>
- <span data-ttu-id="07c3c-109">A [biblioteca do auxiliar de dados de desempenho (PDH)](using-the-pdh-functions-to-consume-counter-data.md) fornece acesso de alto nível aos dados de provedores de contador de desempenho v1 e v2 por meio de uma API Win32 (C/C++).</span><span class="sxs-lookup"><span data-stu-id="07c3c-109">The [Performance Data Helper (PDH) library](using-the-pdh-functions-to-consume-counter-data.md) provides high-level access to data from both V1 and V2 performance counter providers via a Win32 (C/C++) API.</span></span>
- <span data-ttu-id="07c3c-110">A [interface do registro](using-the-registry-functions-to-consume-counter-data.md) fornece acesso a dados de provedores de contador de desempenho v1 e v2 por meio da `HKEY_PERFORMANCE_DATA` chave do registro especial.</span><span class="sxs-lookup"><span data-stu-id="07c3c-110">The [registry interface](using-the-registry-functions-to-consume-counter-data.md) provides access to data from both V1 and V2 performance counter providers via the special `HKEY_PERFORMANCE_DATA` registry key.</span></span>
- <span data-ttu-id="07c3c-111">As [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md) fornecem acesso de baixo nível aos dados de provedores de contador de desempenho v2 por meio de uma API Win32 (C/C++).</span><span class="sxs-lookup"><span data-stu-id="07c3c-111">The [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) provide low-level access to data from V2 performance counter providers via a Win32 (C/C++) API.</span></span>

<span data-ttu-id="07c3c-112">A interface PDH é recomendada para a maioria das tarefas de coleta de dados de desempenho do C/C++, pois é mais fácil de usar do que as interfaces do registro e do PerfLib.</span><span class="sxs-lookup"><span data-stu-id="07c3c-112">The PDH interface is recommended for most C/C++ performance data collection tasks because it is easier to use than the registry and PerfLib interfaces.</span></span>
