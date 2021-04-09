---
description: Os qualificadores de propriedade especificam informações sobre o contador de desempenho para o qual a propriedade é mapeada.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Qualificadores de propriedade para classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171660"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="00e5e-103">Qualificadores de propriedade para classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="00e5e-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="00e5e-104">Os qualificadores de propriedade especificam informações sobre o contador de desempenho para o qual a propriedade é mapeada.</span><span class="sxs-lookup"><span data-stu-id="00e5e-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="00e5e-105">Qualificadores de propriedade para classes de desempenho RAW e formatadas</span><span class="sxs-lookup"><span data-stu-id="00e5e-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="00e5e-106">Qualificadores de propriedade para classes de desempenho brutos</span><span class="sxs-lookup"><span data-stu-id="00e5e-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="00e5e-107">Qualificadores de propriedade para classes de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="00e5e-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="00e5e-108">Como interpretar qualificadores de propriedade</span><span class="sxs-lookup"><span data-stu-id="00e5e-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="00e5e-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00e5e-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="00e5e-110">O contador de desempenho faz parte de um objeto de desempenho representado por um contador de desempenho de [classe de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI – qualificadores específicos são automaticamente anexados pelo provedor WbemPerfClass às classes e propriedades do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) na raiz \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="00e5e-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="00e5e-111">Essas informações se aplicam a todas as instâncias da classe de desempenho.</span><span class="sxs-lookup"><span data-stu-id="00e5e-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="00e5e-112">Alguns qualificadores com valores **boolianos** que são sempre falsos podem não estar presentes em classes específicas.</span><span class="sxs-lookup"><span data-stu-id="00e5e-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="00e5e-113">Qualificadores de propriedade para classes de desempenho RAW e formatadas</span><span class="sxs-lookup"><span data-stu-id="00e5e-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="00e5e-114">A lista a seguir lista os qualificadores que se aplicam a propriedades em classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) ou [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="00e5e-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="00e5e-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="00e5e-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="00e5e-116">**sint32**</span></span>

<span data-ttu-id="00e5e-117">Valor inteiro na enumeração de tipo de contador, conforme definido em WINPERF. h ou Perflib. h.</span><span class="sxs-lookup"><span data-stu-id="00e5e-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="00e5e-118">O qualificador de [**tipo**](countertype-qualifier.md)de referenda indica a fórmula ou o algoritmo usado para calcular o valor mostrado no monitor do sistema para o contador que a propriedade representa.</span><span class="sxs-lookup"><span data-stu-id="00e5e-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="00e5e-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-120">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00e5e-120">**string**</span></span>

<span data-ttu-id="00e5e-121">O nome do contador de desempenho, conforme especificado pelo PDH (auxiliar de dados de desempenho).</span><span class="sxs-lookup"><span data-stu-id="00e5e-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="00e5e-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="00e5e-123">**sint32**</span></span>

<span data-ttu-id="00e5e-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="00e5e-124">Not used.</span></span> <span data-ttu-id="00e5e-125">Sempre contém 0.</span><span class="sxs-lookup"><span data-stu-id="00e5e-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="00e5e-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="00e5e-127">**sint32**</span></span>

<span data-ttu-id="00e5e-128">Não usado.</span><span class="sxs-lookup"><span data-stu-id="00e5e-128">Not used.</span></span> <span data-ttu-id="00e5e-129">Sempre contém 0.</span><span class="sxs-lookup"><span data-stu-id="00e5e-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="00e5e-130">Qualificadores de propriedade para classes de desempenho brutos</span><span class="sxs-lookup"><span data-stu-id="00e5e-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="00e5e-131">A lista a seguir lista os qualificadores que se aplicam a todas as propriedades de classes derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="00e5e-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="00e5e-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="00e5e-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-133">**booleano**</span><span class="sxs-lookup"><span data-stu-id="00e5e-133">**boolean**</span></span>

<span data-ttu-id="00e5e-134">Indica se essa propriedade é o contador padrão a ser usado em caixas de listagem.</span><span class="sxs-lookup"><span data-stu-id="00e5e-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="00e5e-135">Esse qualificador assume como padrão o **falso** para os contadores de desempenho versão 6,0 porque eles não fornecem dados para ele.</span><span class="sxs-lookup"><span data-stu-id="00e5e-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="00e5e-136">Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="00e5e-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="00e5e-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="00e5e-138">**sint32**</span></span>

<span data-ttu-id="00e5e-139">A potência de 10 a ser usada para exibição do contador.</span><span class="sxs-lookup"><span data-stu-id="00e5e-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="00e5e-140">Para zero, o máximo estimado é 10 ^ 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="00e5e-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="00e5e-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="00e5e-142">**sint32**</span></span>

<span data-ttu-id="00e5e-143">Nível de conhecimento do público.</span><span class="sxs-lookup"><span data-stu-id="00e5e-143">Audience level of knowledge.</span></span> <span data-ttu-id="00e5e-144">Não usado.</span><span class="sxs-lookup"><span data-stu-id="00e5e-144">Not used.</span></span> <span data-ttu-id="00e5e-145">O valor é sempre 100.</span><span class="sxs-lookup"><span data-stu-id="00e5e-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="00e5e-146">Qualificadores de propriedade para classes de desempenho formatadas</span><span class="sxs-lookup"><span data-stu-id="00e5e-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="00e5e-147">A lista a seguir lista os qualificadores que se aplicam a todas as propriedades de classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="00e5e-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="00e5e-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**Culináriatype**</span><span class="sxs-lookup"><span data-stu-id="00e5e-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-149">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00e5e-149">**string**</span></span>

<span data-ttu-id="00e5e-150">Tipo de fórmula usado para produzir o resultado.</span><span class="sxs-lookup"><span data-stu-id="00e5e-150">Formula type used to produce the result.</span></span> <span data-ttu-id="00e5e-151">Cada tipo de contador usa os outros qualificadores de propriedade para calcular o resultado mostrado como o valor da propriedade atual.</span><span class="sxs-lookup"><span data-stu-id="00e5e-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="00e5e-152">Os qualificadores **Counter**, **PerfTimeStamp** e **PerfTimeFreq** são mapeados para propriedades em uma classe RAW que fornece os dados.</span><span class="sxs-lookup"><span data-stu-id="00e5e-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="00e5e-153">Para obter mais informações, consulte [qualificador de tipo](countertype-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="00e5e-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Neutraliza**</span><span class="sxs-lookup"><span data-stu-id="00e5e-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-155">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00e5e-155">**string**</span></span>

<span data-ttu-id="00e5e-156">Nome de uma propriedade necessária na classe bruta correspondente a ser usada como o valor do contador na fórmula de culinária.</span><span class="sxs-lookup"><span data-stu-id="00e5e-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="00e5e-157">O valor deve ser o nome da propriedade da propriedade da fonte de dados na classe bruta correspondente.</span><span class="sxs-lookup"><span data-stu-id="00e5e-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="00e5e-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-159">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00e5e-159">**string**</span></span>

<span data-ttu-id="00e5e-160">Nome de uma propriedade em uma classe bruta a ser usada como uma frequência na fórmula de culinária.</span><span class="sxs-lookup"><span data-stu-id="00e5e-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="00e5e-161">O valor padrão apropriado no nível de classe será usado se esse qualificador não estiver presente para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="00e5e-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="00e5e-162">A frequência representa as tiques por segundo do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="00e5e-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="00e5e-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="00e5e-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="00e5e-164">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00e5e-164">**string**</span></span>

<span data-ttu-id="00e5e-165">Nome de uma propriedade em uma classe bruta a ser usada como um carimbo de data/hora na fórmula de culinária.</span><span class="sxs-lookup"><span data-stu-id="00e5e-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="00e5e-166">O valor padrão apropriado no nível de classe será usado se esse qualificador não estiver presente para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="00e5e-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="00e5e-167">Um carimbo de data/hora gerado automaticamente pode introduzir um erro em um cálculo porque o carimbo de data/hora é uma aproximação e não conta a sobrecarga incorrida pelo marshaling e pela coleta de dados real.</span><span class="sxs-lookup"><span data-stu-id="00e5e-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="00e5e-168">Como interpretar qualificadores de propriedade</span><span class="sxs-lookup"><span data-stu-id="00e5e-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="00e5e-169">As propriedades nas [**classes \_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contêm os dados calculados fornecidos pelo [provedor de dados de desempenho formatado](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="00e5e-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="00e5e-170">O valor da propriedade é o resultado calculado final.</span><span class="sxs-lookup"><span data-stu-id="00e5e-170">The property value is the final calculated result.</span></span> <span data-ttu-id="00e5e-171">Os qualificadores fornecem uma receita.</span><span class="sxs-lookup"><span data-stu-id="00e5e-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="00e5e-172">O **contador** e os qualificadores de **base** apontam para as fontes de dados e o **culináriatype** especifica a fórmula usada para produzir o resultado.</span><span class="sxs-lookup"><span data-stu-id="00e5e-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="00e5e-173">O carimbo de data e hora e a frequência de exemplo também vêm da classe bruta correspondente e são nomeados em **PerfTimeStamp** e **PerfTimeFreq**.</span><span class="sxs-lookup"><span data-stu-id="00e5e-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="00e5e-174">Por exemplo, uma das classes formatadas fornecida pelo WMI, [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contém uma propriedade chamada **AvgDiskBytesPerRead**.</span><span class="sxs-lookup"><span data-stu-id="00e5e-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="00e5e-175">O nome da propriedade na classe formatada deve ser igual à propriedade na classe RAW.</span><span class="sxs-lookup"><span data-stu-id="00e5e-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="00e5e-176">A propriedade **AvgDiskBytesPerRead** tem os qualificadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="00e5e-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="00e5e-177">A lista a seguir lista os qualificadores de propriedade disponíveis para propriedades de todas as classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="00e5e-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="00e5e-178">Qualificador</span><span class="sxs-lookup"><span data-stu-id="00e5e-178">Qualifier</span></span>         | <span data-ttu-id="00e5e-179">Valor</span><span class="sxs-lookup"><span data-stu-id="00e5e-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="00e5e-180">**Culináriatype**</span><span class="sxs-lookup"><span data-stu-id="00e5e-180">**CookingType**</span></span>   | <span data-ttu-id="00e5e-181">\_massa média de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="00e5e-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="00e5e-182">**Contador**</span><span class="sxs-lookup"><span data-stu-id="00e5e-182">**Counter**</span></span>       | <span data-ttu-id="00e5e-183">AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="00e5e-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="00e5e-184">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="00e5e-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="00e5e-185">Carimbo de data/hora \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="00e5e-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="00e5e-186">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="00e5e-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="00e5e-187">Frequência \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="00e5e-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="00e5e-188">**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="00e5e-188">**PerfIndex**</span></span>     | <span data-ttu-id="00e5e-189">408</span><span class="sxs-lookup"><span data-stu-id="00e5e-189">408</span></span>                       |
| <span data-ttu-id="00e5e-190">**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="00e5e-190">**HelpIndex**</span></span>     | <span data-ttu-id="00e5e-191">409</span><span class="sxs-lookup"><span data-stu-id="00e5e-191">409</span></span>                       |
| <span data-ttu-id="00e5e-192">**Polybase**</span><span class="sxs-lookup"><span data-stu-id="00e5e-192">**Base**</span></span>          | <span data-ttu-id="00e5e-193">\_Base AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="00e5e-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="00e5e-194">A propriedade **AvgDiskBytesPerRead** relata o número médio de bytes transferidos do disco durante operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="00e5e-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="00e5e-195">A fórmula para a \_ quantidade média de desempenho \_ é:</span><span class="sxs-lookup"><span data-stu-id="00e5e-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="00e5e-196">(Sample2-Sample1)/(base Sample2-base Sample1)</span><span class="sxs-lookup"><span data-stu-id="00e5e-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="00e5e-197">A operação de leitura é amostrada na frequência especificada por **PerfTimeFreq** com o valor **PerfTimeStamp** indicando o exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="00e5e-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="00e5e-198">Os dados brutos do contador em bytes são extraídos da propriedade **AvgDiskBytesPerRead** na classe do [**\_ PerfRawData de \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md) do uso do Win32.</span><span class="sxs-lookup"><span data-stu-id="00e5e-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="00e5e-199">O número base de dados de operações é obtido da **propriedade \_ base AvgDiskBytesPerRead** na mesma classe.</span><span class="sxs-lookup"><span data-stu-id="00e5e-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="00e5e-200">Para obter mais informações, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md) e [monitorando dados de desempenho](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="00e5e-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00e5e-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00e5e-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e5e-202">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="00e5e-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="00e5e-203">Qualificadores específicos para classes de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="00e5e-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="00e5e-204">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="00e5e-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="00e5e-205">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="00e5e-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="00e5e-206">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="00e5e-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
