---
description: O provedor de contador de desempenho é um provedor de alto desempenho que fornece dados brutos do contador de desempenho para as classes do contador de desempenho WMI derivadas do Win32 \_ PerfRawData. O \_ \_ nome da instância win32provider é &\# 0034; OS nt5 \_ GenericPerfProvider \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Provedor de Contadores de Desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011709"
---
# <a name="performance-counter-provider"></a><span data-ttu-id="65ece-104">Provedor de Contadores de Desempenho</span><span class="sxs-lookup"><span data-stu-id="65ece-104">Performance Counter Provider</span></span>

<span data-ttu-id="65ece-105">\[O provedor do contador de desempenho não está mais disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="65ece-105">\[The Performance Counter Provider is no longer available for use.</span></span> <span data-ttu-id="65ece-106">Em vez disso, use o provedor [WMIPerfInst](wmiperfinst-provider.md) .\]</span><span class="sxs-lookup"><span data-stu-id="65ece-106">Instead, use the [WMIPerfInst](wmiperfinst-provider.md) provider.\]</span></span>

<span data-ttu-id="65ece-107">O provedor de contador de desempenho é um provedor de alto desempenho que fornece dados brutos do contador de desempenho para as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="65ece-107">The Performance Counter provider is a high-performance provider that provides raw performance counter data to the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="65ece-108">O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) é "os nt5 \_ GenericPerfProvider \_ v1".</span><span class="sxs-lookup"><span data-stu-id="65ece-108">The [**\_\_Win32Provider**](--win32provider.md) instance name is "NT5\_GenericPerfProvider\_V1".</span></span>

<span data-ttu-id="65ece-109">As [**classes \_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) estão localizadas no namespace "raiz \\ CIMv2" do WMI.</span><span class="sxs-lookup"><span data-stu-id="65ece-109">The [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes are located in the WMI "Root\\CIMv2" namespace.</span></span> <span data-ttu-id="65ece-110">Cada classe de desempenho WMI corresponde a um objeto de desempenho em uma biblioteca de desempenho.</span><span class="sxs-lookup"><span data-stu-id="65ece-110">Each WMI performance class corresponds to a performance object in a performance library.</span></span> <span data-ttu-id="65ece-111">As propriedades dessas classes representam os contadores para o objeto.</span><span class="sxs-lookup"><span data-stu-id="65ece-111">The properties of these classes represent the counters for the object.</span></span> <span data-ttu-id="65ece-112">O nome da classe WMI para um objeto de contador bruto é do formato \*\* \_ Win32 \_ \_ PerfRawData\* Service \_ name *\_* Object \_ Name \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="65ece-112">The WMI class name for a raw counter object is of the form \**Win32\_PerfRawData\_\_* service\_name *\_* object\_name\*\*\*.</span></span> <span data-ttu-id="65ece-113">Por exemplo, o nome da classe WMI que contém os contadores de disco lógico é o [**\_ PerfRawData de \_ perfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="65ece-113">For example, the WMI class name that contains the logical disk counters is [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span>

<span data-ttu-id="65ece-114">Você pode usar a classe [**\_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondente para obter os dados de desempenho previamente calculados mostrados no [*Monitor do sistema*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="65ece-114">You can use the corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class to get the pre-calculated performance data shown in [*System Monitor*](gloss-s.md).</span></span> <span data-ttu-id="65ece-115">Por exemplo, use a [**classe \_ PerfFormattedData \_ \_ de perfdisk do Win32**](./retrieving-raw-and-formatted-performance-data.md) para obter dados de disco previamente calculados.</span><span class="sxs-lookup"><span data-stu-id="65ece-115">For example, use the [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class to get pre-calculated disk data.</span></span>

<span data-ttu-id="65ece-116">Para obter mais informações sobre como escrever um cliente que pode acessar dados de desempenho brutos, consulte [acessando dados de desempenho em C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="65ece-116">For more information about how to write a client that can access raw performance data, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

<span data-ttu-id="65ece-117">Como um provedor de alto desempenho, o provedor de contador de desempenho implementa a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como o método [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) e os seguintes métodos de [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :</span><span class="sxs-lookup"><span data-stu-id="65ece-117">As a high-performance provider, the Performance Counter provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method and the following [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) methods:</span></span>

-   [<span data-ttu-id="65ece-118">**CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="65ece-118">**CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [<span data-ttu-id="65ece-119">**CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="65ece-119">**CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [<span data-ttu-id="65ece-120">**Createrefresher**</span><span class="sxs-lookup"><span data-stu-id="65ece-120">**CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [<span data-ttu-id="65ece-121">**GetObjects**</span><span class="sxs-lookup"><span data-stu-id="65ece-121">**GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [<span data-ttu-id="65ece-122">**QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="65ece-122">**QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [<span data-ttu-id="65ece-123">**StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="65ece-123">**StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a><span data-ttu-id="65ece-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65ece-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65ece-125">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="65ece-125">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
