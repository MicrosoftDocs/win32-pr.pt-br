---
description: Especifique as informações sobre o objeto de desempenho para o qual a classe do contador de desempenho WMI está mapeada.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Qualificadores de classe para classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788728"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="9013b-103">Qualificadores de classe para classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="9013b-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="9013b-104">Os qualificadores de classe especificam informações sobre o objeto de desempenho para o qual a [classe do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI é mapeada.</span><span class="sxs-lookup"><span data-stu-id="9013b-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="9013b-105">Para obter mais informações, consulte [monitorando dados de desempenho](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="9013b-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="9013b-106">Qualificadores para PerformanceClasses brutos e formatados</span><span class="sxs-lookup"><span data-stu-id="9013b-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="9013b-107">Qualificadores para classes de desempenho brutos</span><span class="sxs-lookup"><span data-stu-id="9013b-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="9013b-108">Qualificadores para classes de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="9013b-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="9013b-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9013b-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="9013b-110">O contador de desempenho – qualificadores específicos são automaticamente anexados pelo provedor "WbemPerfClass" às classes e propriedades do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) na raiz \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="9013b-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="9013b-111">Essas informações se aplicam a todas as instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="9013b-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="9013b-112">Alguns qualificadores com valores **boolianos** que são sempre **falsos** podem não estar presentes em classes específicas.</span><span class="sxs-lookup"><span data-stu-id="9013b-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="9013b-113">Qualificadores para PerformanceClasses brutos e formatados</span><span class="sxs-lookup"><span data-stu-id="9013b-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="9013b-114">Os qualificadores a seguir se aplicam a todas as classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="9013b-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="9013b-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span><span class="sxs-lookup"><span data-stu-id="9013b-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-116">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-116">**boolean**</span></span>

<span data-ttu-id="9013b-117">Indica se a classe contém dados cooked.</span><span class="sxs-lookup"><span data-stu-id="9013b-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="9013b-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-119">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9013b-119">**string**</span></span>

<span data-ttu-id="9013b-120">Nome do objeto de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9013b-120">Performance object name.</span></span> <span data-ttu-id="9013b-121">Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="9013b-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="9013b-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="9013b-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="9013b-123">**sint32**</span></span>

<span data-ttu-id="9013b-124">Não fornece dados detalhados.</span><span class="sxs-lookup"><span data-stu-id="9013b-124">Does not provide detail data.</span></span> <span data-ttu-id="9013b-125">Sempre contém o valor de 100.</span><span class="sxs-lookup"><span data-stu-id="9013b-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dinâmico**</span><span class="sxs-lookup"><span data-stu-id="9013b-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-127">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-127">**boolean**</span></span>

<span data-ttu-id="9013b-128">Sempre definido como **true** porque as instâncias são sempre dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="9013b-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span><span class="sxs-lookup"><span data-stu-id="9013b-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-130">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-130">**boolean**</span></span>

<span data-ttu-id="9013b-131">Indica se a classe é proveniente de uma biblioteca de desempenho herdada.</span><span class="sxs-lookup"><span data-stu-id="9013b-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="9013b-132">Sempre definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="9013b-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="9013b-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="9013b-134">**sint32**</span></span>

<span data-ttu-id="9013b-135">Os índices não são mais válidos.</span><span class="sxs-lookup"><span data-stu-id="9013b-135">Indexes are no longer valid.</span></span> <span data-ttu-id="9013b-136">Esse qualificador é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="9013b-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="9013b-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="9013b-138">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-138">**boolean**</span></span>

<span data-ttu-id="9013b-139">Indica que a classe é uma classe de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="9013b-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="9013b-140">Sempre definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="9013b-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Localidade**</span><span class="sxs-lookup"><span data-stu-id="9013b-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="9013b-142">**sint32**</span></span>

<span data-ttu-id="9013b-143">Identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="9013b-143">Locale identifier.</span></span> <span data-ttu-id="9013b-144">O valor é sempre 1033 (inglês americano).</span><span class="sxs-lookup"><span data-stu-id="9013b-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="9013b-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="9013b-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="9013b-146">**int32**</span></span>

<span data-ttu-id="9013b-147">Os índices não são mais válidos.</span><span class="sxs-lookup"><span data-stu-id="9013b-147">Indexes are no longer valid.</span></span> <span data-ttu-id="9013b-148">Esse qualificador é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="9013b-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Operador**</span><span class="sxs-lookup"><span data-stu-id="9013b-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-150">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9013b-150">**string**</span></span>

<span data-ttu-id="9013b-151">Nome do provedor de instância.</span><span class="sxs-lookup"><span data-stu-id="9013b-151">Name of the instance provider.</span></span> <span data-ttu-id="9013b-152">O valor é "WbemPerfV2".</span><span class="sxs-lookup"><span data-stu-id="9013b-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="9013b-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span><span class="sxs-lookup"><span data-stu-id="9013b-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-154">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9013b-154">**string**</span></span>

<span data-ttu-id="9013b-155">Nome do driver na chave **HKEY \_ local de \_ \\ \\ Serviços CurrentControlSet** , sob a qual a chave de desempenho pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="9013b-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="9013b-156">Esse nome também é o nome do serviço que fornece o contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9013b-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Único**</span><span class="sxs-lookup"><span data-stu-id="9013b-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-158">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-158">**boolean**</span></span>

<span data-ttu-id="9013b-159">Se **for true**, indicará que existe apenas uma única instância da classe.</span><span class="sxs-lookup"><span data-stu-id="9013b-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="9013b-160">Qualificadores para classes de desempenho brutos</span><span class="sxs-lookup"><span data-stu-id="9013b-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="9013b-161">Os qualificadores a seguir se aplicam a todas as classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="9013b-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="9013b-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Dispendiosa**</span><span class="sxs-lookup"><span data-stu-id="9013b-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-163">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-163">**boolean**</span></span>

<span data-ttu-id="9013b-164">Indica se a obtenção de instâncias dessa classe é uma operação dispendiosa.</span><span class="sxs-lookup"><span data-stu-id="9013b-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="9013b-165">Sempre definido como **true** para classes com " \_ dispendioso" acrescentado ao final do nome da classe.</span><span class="sxs-lookup"><span data-stu-id="9013b-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="9013b-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9013b-167">**uint32**</span></span>

<span data-ttu-id="9013b-168">Não fornece dados detalhados.</span><span class="sxs-lookup"><span data-stu-id="9013b-168">Does not provide detail data.</span></span> <span data-ttu-id="9013b-169">Sempre contém o valor de 100.</span><span class="sxs-lookup"><span data-stu-id="9013b-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="9013b-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-171">**booleano**</span><span class="sxs-lookup"><span data-stu-id="9013b-171">**boolean**</span></span>

<span data-ttu-id="9013b-172">O valor é sempre **false**.</span><span class="sxs-lookup"><span data-stu-id="9013b-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="9013b-173">Qualificadores para classes de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="9013b-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="9013b-174">Os qualificadores a seguir se aplicam a todas as classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="9013b-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="9013b-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Autocookie**</span><span class="sxs-lookup"><span data-stu-id="9013b-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="9013b-176">**int32**</span></span>

<span data-ttu-id="9013b-177">Indica que os valores nas instâncias de classe são calculados automaticamente a partir da classe de dados brutos correspondente.</span><span class="sxs-lookup"><span data-stu-id="9013b-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="9013b-178">O valor é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="9013b-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="9013b-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass de autocookie \_**</span><span class="sxs-lookup"><span data-stu-id="9013b-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="9013b-180">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9013b-180">**string**</span></span>

<span data-ttu-id="9013b-181">Nome da classe bruta a ser usada para cálculo para a classe formatada.</span><span class="sxs-lookup"><span data-stu-id="9013b-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="9013b-182">Esse qualificador é necessário.</span><span class="sxs-lookup"><span data-stu-id="9013b-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9013b-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9013b-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9013b-184">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="9013b-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="9013b-185">Qualificadores específicos para classes de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="9013b-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="9013b-186">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="9013b-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="9013b-187">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="9013b-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="9013b-188">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="9013b-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
