---
description: Os scripts WMI podem acessar as classes de contador de desempenho do WMI pré-instalado, seja no computador local ou remotamente.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Acessando dados de desempenho no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810696"
---
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="c51f7-103">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="c51f7-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="c51f7-104">Os scripts WMI podem acessar as [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)do WMI pré-instalado, seja no computador local ou remotamente.</span><span class="sxs-lookup"><span data-stu-id="c51f7-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="c51f7-105">Embora os scripts possam obter dados de classes não calculadas, como [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)ou classes formatadas, [**a \_ \_ \_ memória Win32 PerfFormattedData PerfOS**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), as classes de dados formatadas podem ser mais fáceis de usar.</span><span class="sxs-lookup"><span data-stu-id="c51f7-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="c51f7-106">O monitoramento de dados de desempenho com as classes do contador de desempenho requer o uso de um [*atualizador*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="c51f7-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="c51f7-107">Use o objeto [**SWbemRefresher**](swbemrefresher.md) para armazenar um ou mais objetos de desempenho para atualizar ou atualizar um único objeto pela chamada [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="c51f7-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="c51f7-108">Para obter mais informações, consulte [atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c51f7-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="c51f7-109">Ao definir a propriedade [**SWbemRefresher. falha**](swbemrefresher-autoreconnect.md) como **true**, o WMI se reconectará automaticamente a um provedor remoto se a conexão for interrompida para que você não precise verificar o status da conexão.</span><span class="sxs-lookup"><span data-stu-id="c51f7-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="c51f7-110">Conforme mostrado no script de exemplo de código de script a seguir, você deve fazer uma chamada de atualização inicial para obter um valor inicial para o objeto que você está atualizando.</span><span class="sxs-lookup"><span data-stu-id="c51f7-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="c51f7-111">Em seguida, as chamadas de atualização subsequentes contêm dados.</span><span class="sxs-lookup"><span data-stu-id="c51f7-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="c51f7-112">Quando um script está acessando dados do contador de desempenho do WMI de um computador remoto, o script só pode ser executado sob a conta de usuário conectada no momento.</span><span class="sxs-lookup"><span data-stu-id="c51f7-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="c51f7-113">O WMI não dá suporte a uma chamada [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) que passa credenciais de usuário diferentes.</span><span class="sxs-lookup"><span data-stu-id="c51f7-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="c51f7-114">Portanto, a conta que está chamando o computador remoto já deve ter os privilégios apropriados no computador.</span><span class="sxs-lookup"><span data-stu-id="c51f7-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="c51f7-115">O exemplo de código de script a seguir mostra como usar um objeto [**SWbemRefresher**](swbemrefresher.md) para atualizar os dados em objetos de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c51f7-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="c51f7-116">Para obter mais informações sobre como usar contadores de desempenho no WMI, consulte [acessando classes de desempenho pré-instalado do WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c51f7-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a><span data-ttu-id="c51f7-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c51f7-117">Example</span></span>

<span data-ttu-id="c51f7-118">O exemplo de código de script a seguir mostra que você deve fazer uma chamada de atualização inicial para obter um valor inicial para o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="c51f7-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="c51f7-119">Em seguida, as chamadas de atualização subsequentes contêm dados.</span><span class="sxs-lookup"><span data-stu-id="c51f7-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="c51f7-120">O exemplo de código de script a seguir mostra como usar um objeto [**SWbemRefresher**](swbemrefresher.md) para atualizar os dados em objetos de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c51f7-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="c51f7-121">Para obter mais informações sobre como usar contadores de desempenho no WMI, consulte [acessando classes de desempenho pré-instalado do WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c51f7-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a><span data-ttu-id="c51f7-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c51f7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c51f7-123">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="c51f7-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="c51f7-124">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="c51f7-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="c51f7-125">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="c51f7-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
