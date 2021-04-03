---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922714"
---
# <a name="p-wmi"></a><span data-ttu-id="0114f-103">P (WMI)</span><span class="sxs-lookup"><span data-stu-id="0114f-103">P (WMI)</span></span>

<span data-ttu-id="0114f-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="0114f-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0114f-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contador de desempenho**</span><span class="sxs-lookup"><span data-stu-id="0114f-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-106">Uma propriedade em uma classe de desempenho que é derivada [**de \_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) que armazena dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="0114f-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="0114f-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objeto de desempenho**</span><span class="sxs-lookup"><span data-stu-id="0114f-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-108">Um objeto em uma biblioteca de desempenho que armazena dados em contadores.</span><span class="sxs-lookup"><span data-stu-id="0114f-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="0114f-109">Esses objetos são visíveis no utilitário [*Monitor do sistema*](gloss-s.md) .</span><span class="sxs-lookup"><span data-stu-id="0114f-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="0114f-110">Os exemplos são objetos de cache e disco lógico.</span><span class="sxs-lookup"><span data-stu-id="0114f-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="0114f-111">Quando transferido para o WMI pelo processo do [*ADAP*](gloss-a.md) , cada objeto se torna duas classes de desempenho do WMI.</span><span class="sxs-lookup"><span data-stu-id="0114f-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="0114f-112">Uma classe, que contém dados brutos, deriva do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="0114f-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="0114f-113">A outra classe deriva do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e contém os mesmos dados visíveis no monitor do sistema, conforme calculado pelo provedor de contador do cooked.</span><span class="sxs-lookup"><span data-stu-id="0114f-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="0114f-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumidor permanente**</span><span class="sxs-lookup"><span data-stu-id="0114f-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-115">Um [*consumidor de eventos*](gloss-e.md) cujo registro dura até que seja explicitamente cancelado.</span><span class="sxs-lookup"><span data-stu-id="0114f-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="0114f-116">Consulte também [*consumidor temporário*](gloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="0114f-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="0114f-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumidor físico**</span><span class="sxs-lookup"><span data-stu-id="0114f-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-118">Um objeto COM que é implementado por um [*provedor de consumidor de eventos*](gloss-e.md) que inclui um [*coletor*](gloss-s.md) para receber notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="0114f-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="0114f-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="0114f-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-120">Um par de nome/valor que descreve uma unidade de dados para uma classe.</span><span class="sxs-lookup"><span data-stu-id="0114f-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="0114f-121">Os valores de propriedade devem ter um tipo de dados [*formato MOF (MOF)*](gloss-m.md) válido.</span><span class="sxs-lookup"><span data-stu-id="0114f-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="0114f-122">Consulte também a [*propriedade de referência*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="0114f-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="0114f-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**provedor de propriedades**</span><span class="sxs-lookup"><span data-stu-id="0114f-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-124">Um servidor COM que dá suporte à recuperação e à modificação de propriedades WMI.</span><span class="sxs-lookup"><span data-stu-id="0114f-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="0114f-125">Os provedores de propriedades implementam as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .</span><span class="sxs-lookup"><span data-stu-id="0114f-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0114f-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**operador**</span><span class="sxs-lookup"><span data-stu-id="0114f-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-127">Um servidor COM que se comunica com objetos gerenciados para acessar dados e notificações de eventos, como o registro ou um dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="0114f-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="0114f-128">Os provedores encaminham esses dados para a [*Gerenciador de objetos CIM*](gloss-c.md) para integração e interpretação.</span><span class="sxs-lookup"><span data-stu-id="0114f-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="0114f-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**método de provedor**</span><span class="sxs-lookup"><span data-stu-id="0114f-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="0114f-130">Um método que um *provedor* de WMI implementa.</span><span class="sxs-lookup"><span data-stu-id="0114f-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
