---
description: A função OpenPerformanceData de DLLs de desempenho usa um argumento de cadeia de caracteres como entrada.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Criando outras entradas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921748"
---
# <a name="creating-other-registry-entries"></a><span data-ttu-id="987e5-103">Criando outras entradas do registro</span><span class="sxs-lookup"><span data-stu-id="987e5-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="987e5-104">A função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) da DLL de desempenho usa um argumento de cadeia de caracteres como entrada.</span><span class="sxs-lookup"><span data-stu-id="987e5-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="987e5-105">Para fornecer uma cadeia de caracteres de entrada para a função Open, inclua uma chave de **vinculação** em sua chave de **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="987e5-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="987e5-106">A chave de **vinculação** contém um valor de **exportação** .</span><span class="sxs-lookup"><span data-stu-id="987e5-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="987e5-107">Defina os dados do valor para **Exportar** para a cadeia de caracteres de entrada que você deseja passar para a função Open.</span><span class="sxs-lookup"><span data-stu-id="987e5-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="987e5-108">O tipo de dados de **exportação** é **reg \_ multi \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="987e5-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="987e5-109">Se a **exportação** não for definida (**Exportar** é opcional), o sistema passará **nulo** para sua função [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="987e5-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="987e5-110">Normalmente, se mais de um aplicativo compartilhar a mesma DLL de desempenho, cada aplicativo incluirá uma chave de **vinculação** e um valor de **exportação** para fornecer contexto sobre o aplicativo que está chamando a dll.</span><span class="sxs-lookup"><span data-stu-id="987e5-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="987e5-111">O seguinte mostra as entradas do registro:</span><span class="sxs-lookup"><span data-stu-id="987e5-111">The following shows the registry entries:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

<span data-ttu-id="987e5-112">Por padrão, as funções [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) e [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) da DLL de desempenho devem retornar dentro de 10.000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="987e5-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="987e5-113">Caso contrário, o sistema não usa os dados retornados pela DLL.</span><span class="sxs-lookup"><span data-stu-id="987e5-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="987e5-114">O aplicativo pode aumentar ou diminuir o valor de tempo limite especificando um valor de registro de tempo limite **aberto** ou **coletar tempo limite** em sua chave de **desempenho** , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="987e5-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

<span data-ttu-id="987e5-115">Para obter os dados de desempenho de alguns aplicativos (aqueles que retornam contadores usando a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), é necessário usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o dispositivo associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="987e5-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="987e5-116">Nesse caso, o nome especificado em **CreateFile** também deve ser instalado no nó dispositivos dos do registro, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="987e5-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
