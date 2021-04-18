---
description: Um aplicativo que dá suporte a contadores de desempenho deve ter uma chave de desempenho sob a chave de serviços. O exemplo a seguir mostra os valores que você deve incluir para essa chave.
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: Criando a chave de desempenho de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753242"
---
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="05c87-104">Criando a chave de desempenho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="05c87-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="05c87-105">Um aplicativo que dá suporte a contadores de desempenho deve ter uma chave de **desempenho** sob a chave de **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="05c87-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="05c87-106">O exemplo a seguir mostra os valores que você deve incluir para essa chave.</span><span class="sxs-lookup"><span data-stu-id="05c87-106">The following example shows the values that you must include for this key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

<span data-ttu-id="05c87-107">O valor da **biblioteca** fornece o nome da DLL de desempenho e os valores de **abrir**, **coletar** e **fechar** fornecem os nomes das funções exportadas da DLL de desempenho.</span><span class="sxs-lookup"><span data-stu-id="05c87-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="05c87-108">O tipo de dados desses valores é **reg \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="05c87-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="05c87-109">Quando um consumidor solicita dados de desempenho, o sistema usa esses valores para determinar quais DLLs de desempenho carregar e quais funções de DLL chamar.</span><span class="sxs-lookup"><span data-stu-id="05c87-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="05c87-110">O valor da **biblioteca** pode conter o nome da dll ou um caminho completo para a dll.</span><span class="sxs-lookup"><span data-stu-id="05c87-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="05c87-111">Se você usar o tipo de dados **reg \_ expande \_ sz** para a **biblioteca**, poderá especificar variáveis de ambiente em seu caminho.</span><span class="sxs-lookup"><span data-stu-id="05c87-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="05c87-112">A chave de serviço do aplicativo deve existir antes que você possa executar o **lodctr** para carregar os nomes de contadores e as cadeias de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="05c87-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="05c87-113">Para obter valores de registro adicionais que você pode criar, como especificar valores de tempo limite para as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , consulte [criando outras entradas de registro](creating-other-registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="05c87-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
