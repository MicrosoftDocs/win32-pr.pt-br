---
description: Suprimentos calculados (&\# 0034; cooked&\# 0034;) dados do contador de desempenho. Fornece dados dinâmicos para as classes WMI derivadas do Win32 \_ PerfFormattedData. Também conhecido como o provedor de contador de cooked.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Provedor de Dados de desempenho formatado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760614"
---
# <a name="formatted-performance-data-provider"></a><span data-ttu-id="4fc59-105">Provedor de Dados de desempenho formatado</span><span class="sxs-lookup"><span data-stu-id="4fc59-105">Formatted Performance Data Provider</span></span>

<span data-ttu-id="4fc59-106">\[O Provedor de Dados de desempenho formatado, também conhecido como "provedor de contador de cooked", não está mais disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="4fc59-106">\[The Formatted Performance Data Provider, also known as the "Cooked Counter Provider," is no longer available for use.</span></span> <span data-ttu-id="4fc59-107">Em vez disso, use o provedor [WMIPerfInst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="4fc59-107">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="4fc59-108">O provedor de dados de desempenho formatado de alto desempenho fornece dados de contador de desempenho calculados ("cooked"), como a porcentagem de tempo que um disco gasta gravando dados.</span><span class="sxs-lookup"><span data-stu-id="4fc59-108">The high-performance Formatted Performance Data provider supplies calculated ("cooked") performance counter data, such as the percentage of time a disk spends writing data.</span></span> <span data-ttu-id="4fc59-109">Esse provedor fornece dados dinâmicos para as classes WMI derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="4fc59-109">This provider supplies dynamic data to the WMI classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="4fc59-110">A diferença entre esse provedor e o [provedor](performance-counter-provider.md) de contador de desempenho é que o provedor de contador de desempenho fornece dados brutos e o provedor de contador de cooked fornece dados de desempenho que aparecem exatamente como no [*Monitor do sistema*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="4fc59-110">The difference between this provider and the [Performance Counter provider](performance-counter-provider.md) is that the Performance Counter provider supplies raw data and the Cooked Counter provider supplies performance data that appears exactly as in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="4fc59-111">O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) é "HiPerfCooker \_ v1".</span><span class="sxs-lookup"><span data-stu-id="4fc59-111">The [**\_\_Win32Provider**](--win32provider.md) instance name is "HiPerfCooker\_v1".</span></span>

<span data-ttu-id="4fc59-112">O nome da classe formatada pelo WMI para um objeto de contador é do formato " \_ nome do objeto do nome do serviço Win32 PerfFormattedData \_ *\_* \_ ".*\_*</span><span class="sxs-lookup"><span data-stu-id="4fc59-112">The WMI formatted class name for a counter object is of the form "Win32\_PerfFormattedData\_*service\_name*\_*object\_name*".</span></span> <span data-ttu-id="4fc59-113">Por exemplo, o nome da classe WMI que contém os contadores de disco lógico é o **\_ PerfFormattedData de \_ perfdisk \_ do Win32**.</span><span class="sxs-lookup"><span data-stu-id="4fc59-113">For example, the WMI class name that contains the logical disk counters is **Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**.</span></span> <span data-ttu-id="4fc59-114">Essas classes estão localizadas no namespace "raiz \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="4fc59-114">These classes are located in the "Root\\CIMv2" namespace.</span></span>

<span data-ttu-id="4fc59-115">Como as classes de dados de desempenho são adicionadas e modificadas dinamicamente em um determinado sistema, não é possível documentar formalmente as propriedades de todos os objetos de desempenho conhecidos.</span><span class="sxs-lookup"><span data-stu-id="4fc59-115">Because performance data classes are added and modified dynamically on a given system, it is not possible to formally document the properties of all known performance objects.</span></span> <span data-ttu-id="4fc59-116">Para determinar quais classes estão disponíveis para você e identificar quais membros essas classes têm, consulte [recuperando a documentação para objetos de dados de desempenho brutos e formatados](retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="4fc59-116">To determine what classes are available to you, and to identify what members those classes have, see [Retrieving Documentation for Raw and Formatted Performance Data Objects](retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="4fc59-117">As classes [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) usam o qualificador de **culináriatype** nos [tipos de contador de desempenho WMI](wmi-performance-counter-types.md) para especificar a fórmula para calcular dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="4fc59-117">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes use the **CookingType** qualifier in [WMI Performance Counter Types](wmi-performance-counter-types.md) to specify the formula for calculating performance data.</span></span> <span data-ttu-id="4fc59-118">Esse qualificador é o mesmo que o qualificador de **tipo** em classes [**\_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="4fc59-118">This qualifier is the same as the **CounterType** qualifier in the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span>

<span data-ttu-id="4fc59-119">Como um provedor de alto desempenho, o provedor de contador cooked implementa a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como o método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e os seguintes métodos [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :</span><span class="sxs-lookup"><span data-stu-id="4fc59-119">As a high-performance provider, the Cooked Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="4fc59-120">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="4fc59-120">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="4fc59-121">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="4fc59-121">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="4fc59-122">**Createrefresher**</span><span class="sxs-lookup"><span data-stu-id="4fc59-122">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="4fc59-123">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="4fc59-123">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="4fc59-124">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="4fc59-124">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="4fc59-125">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="4fc59-125">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="4fc59-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4fc59-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fc59-127">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="4fc59-127">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
