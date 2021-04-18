---
description: Ao escrever um provedor de alto desempenho que deriva classes do Win32 \_ PerfRawData, você deve seguir convenções específicas para que o WMI possa fornecer dados aos valores de propriedade.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Dando suporte à classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752002"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="8466f-103">Dando suporte à \_ classe Win32 PerfRawData</span><span class="sxs-lookup"><span data-stu-id="8466f-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="8466f-104">Ao escrever um provedor de alto desempenho que deriva classes do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), você deve seguir convenções específicas para que o WMI possa fornecer dados aos valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8466f-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="8466f-105">Não é recomendável gravar um provedor WMI de alto desempenho para criar contadores de desempenho em nenhuma versão do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="8466f-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="8466f-106">Para obter mais informações, consulte [tornando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)e [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="8466f-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="8466f-107">O procedimento a seguir descreve como dar suporte à classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) com seu provedor de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="8466f-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="8466f-108">**Para dar suporte à \_ classe Win32 PerfRawData**</span><span class="sxs-lookup"><span data-stu-id="8466f-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="8466f-109">Crie sua classe no namespace raiz \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="8466f-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="8466f-110">A classe deve ser derivada do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e ter o qualificador de **Hiperf** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="8466f-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="8466f-111">Você também pode adicionar classes de dados de desempenho WDM (driver) ao \\ namespace WMI raiz.</span><span class="sxs-lookup"><span data-stu-id="8466f-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="8466f-112">Para obter mais informações sobre como criar sua própria classe para o WMI, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="8466f-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="8466f-113">Especifique o provedor como "os nt5 \_ GenericPerfProvider \_ v1" no qualificador do **provedor** .</span><span class="sxs-lookup"><span data-stu-id="8466f-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="8466f-114">Especifique os seguintes qualificadores de nível de classe:</span><span class="sxs-lookup"><span data-stu-id="8466f-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="8466f-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="8466f-115">**HiPerf**</span></span>
    -   <span data-ttu-id="8466f-116">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="8466f-116">**Locale**</span></span>
    -   <span data-ttu-id="8466f-117">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="8466f-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="8466f-118">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="8466f-118">**Provider**</span></span>

    <span data-ttu-id="8466f-119">Para obter mais informações, consulte [**qualificadores de classe para classes de contador de desempenho**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8466f-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="8466f-120">Não defina o qualificador **GenericPerfCtr** porque ele está reservado para o processo ADAP que transfere dados da biblioteca de desempenho para classes WMI.</span><span class="sxs-lookup"><span data-stu-id="8466f-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="8466f-121">Preencha as propriedades apropriadas de carimbo de data/hora e frequência usadas para computar fórmulas de tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="8466f-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="8466f-122">Essas propriedades são herdadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e, se você estiver escrevendo um provedor de alto desempenho, deverá preenchê-las para a classe a ser exibida no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="8466f-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="8466f-123">Inclua uma propriedade de chave chamada **Name** em sua classe (essa propriedade não é necessária para classes singleton).</span><span class="sxs-lookup"><span data-stu-id="8466f-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="8466f-124">Você não deve usar nenhuma propriedade de chave que não seja **nome** em sua classe.</span><span class="sxs-lookup"><span data-stu-id="8466f-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="8466f-125">Crie Propriedades dados-tipados como **DWORD** (**UInt32**) ou **QWORD** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="8466f-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="8466f-126">Essas propriedades se tornam contadores de desempenho quando transferidas para as bibliotecas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8466f-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="8466f-127">Especifique os seguintes qualificadores de nível de propriedade para todas as propriedades em sua classe:</span><span class="sxs-lookup"><span data-stu-id="8466f-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="8466f-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="8466f-128">**DisplayName**</span></span>
    -   <span data-ttu-id="8466f-129">**CounterType**</span><span class="sxs-lookup"><span data-stu-id="8466f-129">**CounterType**</span></span>
    -   <span data-ttu-id="8466f-130">**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="8466f-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="8466f-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8466f-131">**Description**</span></span>
    -   <span data-ttu-id="8466f-132">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="8466f-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="8466f-133">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="8466f-133">**PerfDetail**</span></span>

    <span data-ttu-id="8466f-134">Para obter mais informações, consulte [**qualificadores de propriedade para classes de contador de desempenho**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8466f-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="8466f-135">Além disso, o arquivo de cabeçalho WINPERF. h contém valores que você pode especificar para **PerfDetail** e **MyType**.</span><span class="sxs-lookup"><span data-stu-id="8466f-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="8466f-136">O WMI usa os qualificadores **DisplayName**, **locale** e **Description** para localização.</span><span class="sxs-lookup"><span data-stu-id="8466f-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="8466f-137">Você deve adicionar qualificadores corrigidos ao \_ namespace MS 409 (inglês) para que o monitor do sistema possa exibir corretamente os dados da classe.</span><span class="sxs-lookup"><span data-stu-id="8466f-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="8466f-138">Isso significa que você altera a definição de propriedade adicionando um qualificador de **Descrição** com texto explicativo e preenchendo o valor **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="8466f-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="8466f-139">Você também deve adicionar qualificadores corrigidos a qualquer outro namespace de localidade ao qual sua classe dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8466f-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="8466f-140">Se um usuário solicitar dados de uma localidade para a qual você não fornece qualificadores corrigidos, o WMI usa as definições especificadas no namespace do MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="8466f-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="8466f-141">Crie uma propriedade base para qualquer propriedade que tenha um tipo de contador esperando um valor base.</span><span class="sxs-lookup"><span data-stu-id="8466f-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="8466f-142">Essa propriedade segue imediatamente a propriedade e é nomeada \* PropertyName \***\_ base**.</span><span class="sxs-lookup"><span data-stu-id="8466f-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="8466f-143">Por exemplo, a propriedade média **AvgDiskBytesPerRead** na classe [**do \_ PerfRawData de \_ Perfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) de AvgDiskBytesPerRead de entrada requer uma propriedade de base denominada base de **\_ dados** para o número de amostras, a contagem de um e-</span><span class="sxs-lookup"><span data-stu-id="8466f-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="8466f-144">Para determinar se o tipo de contador que você deseja usar requer uma propriedade base, localize o tipo de contador por nome ou valor decimal nos [tipos de contador de desempenho WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="8466f-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="8466f-145">Verifique se seu provedor atende aos [requisitos de desempenho](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="8466f-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8466f-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8466f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8466f-147">Criando um provedor de instância em um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="8466f-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
