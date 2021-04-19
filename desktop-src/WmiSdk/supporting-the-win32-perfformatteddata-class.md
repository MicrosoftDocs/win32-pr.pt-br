---
description: Ao escrever um provedor de alto desempenho que deriva classes do Win32 \_ PerfFormattedData, você deve seguir convenções específicas para que o WMI possa calcular os valores de propriedade.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Dando suporte à classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782508"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="ff134-103">Dando suporte à \_ classe Win32 PerfFormattedData</span><span class="sxs-lookup"><span data-stu-id="ff134-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="ff134-104">Ao escrever um provedor de alto desempenho que deriva classes do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), você deve seguir convenções específicas para que o WMI possa calcular os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ff134-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="ff134-105">Não é recomendável gravar um provedor WMI de alto desempenho para criar contadores de desempenho em nenhuma versão do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="ff134-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="ff134-106">Para obter mais informações, consulte [tornando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)e [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ff134-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="ff134-107">O procedimento a seguir descreve como dar suporte à \_ classe Win32 PerfFormattedData.</span><span class="sxs-lookup"><span data-stu-id="ff134-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="ff134-108">**Para dar suporte à \_ classe Win32 PerfFormattedData**</span><span class="sxs-lookup"><span data-stu-id="ff134-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="ff134-109">Crie sua classe no mesmo namespace que a classe RAW correspondente.</span><span class="sxs-lookup"><span data-stu-id="ff134-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="ff134-110">A classe deve ser derivada do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e ter o qualificador de **Hiperf** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="ff134-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="ff134-111">Para obter mais informações sobre como criar sua própria classe para o WMI, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ff134-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="ff134-112">Especifique "HiPerfCooker \_ v1" no qualificador do [**provedor**](class-qualifiers-for-performance-counter-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="ff134-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="ff134-113">Especifique os seguintes qualificadores de nível de classe, além dos qualificadores usados para as classes brutas:</span><span class="sxs-lookup"><span data-stu-id="ff134-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="ff134-114">**Autocookie**</span><span class="sxs-lookup"><span data-stu-id="ff134-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-115">**RawClass de autocookie \_**</span><span class="sxs-lookup"><span data-stu-id="ff134-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-116">**Cooked**</span><span class="sxs-lookup"><span data-stu-id="ff134-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-117">**Dispendiosa**</span><span class="sxs-lookup"><span data-stu-id="ff134-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-118">**Dinâmico**</span><span class="sxs-lookup"><span data-stu-id="ff134-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="ff134-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="ff134-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-120">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="ff134-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-121">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="ff134-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-122">**Provedor**</span><span class="sxs-lookup"><span data-stu-id="ff134-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-123">**Único**</span><span class="sxs-lookup"><span data-stu-id="ff134-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="ff134-124">Não defina nenhum valor para **GenericPerfCtr**, **PerfIndex** ou **HelpIndex** porque eles serão definidos pelo processo ADAP.</span><span class="sxs-lookup"><span data-stu-id="ff134-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="ff134-125">Para obter mais informações, consulte [**qualificadores de classe para classes de contador de desempenho**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ff134-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="ff134-126">Inclua uma propriedade de chave chamada **Name** em sua classe (essa propriedade não é necessária para classes singleton).</span><span class="sxs-lookup"><span data-stu-id="ff134-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="ff134-127">O valor da propriedade **Name** deve ser o mesmo que a classe RAW correspondente.</span><span class="sxs-lookup"><span data-stu-id="ff134-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="ff134-128">Você não deve usar nenhuma propriedade de chave que não seja **nome** em sua classe.</span><span class="sxs-lookup"><span data-stu-id="ff134-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="ff134-129">Crie Propriedades de dados digitadas como **DWORD** (**UInt32**) ou **QWORD** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="ff134-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="ff134-130">As propriedades devem corresponder a uma propriedade na classe RAW ou uma propriedade na classe que você está criando.</span><span class="sxs-lookup"><span data-stu-id="ff134-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="ff134-131">Especifique os seguintes qualificadores de nível de propriedade para todas as propriedades em sua classe, além dos qualificadores **PerfIndex** e **PerfDetail** usados para as propriedades de classe bruta:</span><span class="sxs-lookup"><span data-stu-id="ff134-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="ff134-132">**Polybase**</span><span class="sxs-lookup"><span data-stu-id="ff134-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-133">**Culináriatype**</span><span class="sxs-lookup"><span data-stu-id="ff134-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-134">**Contador**</span><span class="sxs-lookup"><span data-stu-id="ff134-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-135">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="ff134-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-136">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="ff134-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ff134-137">**SampleWindow**</span><span class="sxs-lookup"><span data-stu-id="ff134-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="ff134-138">Para obter mais informações, consulte [**qualificadores de propriedade para classes de contador de desempenho**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ff134-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="ff134-139">Além disso, o arquivo de cabeçalho WINPERF. h contém valores que você pode especificar para **PerfDetail** e **MyType**.</span><span class="sxs-lookup"><span data-stu-id="ff134-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="ff134-140">Verifique se seu provedor atende aos [requisitos de desempenho](#performance-requirements).</span><span class="sxs-lookup"><span data-stu-id="ff134-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="ff134-141">Requisitos de desempenho</span><span class="sxs-lookup"><span data-stu-id="ff134-141">Performance Requirements</span></span>

<span data-ttu-id="ff134-142">Quando você escreve um provedor de alto desempenho, seu desempenho deve atender aos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="ff134-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="ff134-143">Abrir o arquivo DLL de alto desempenho pode levar até 100 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ff134-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="ff134-144">De modo geral, a abertura de cada um dos provedores de alto desempenho e da biblioteca de desempenho não pode exceder 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="ff134-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="ff134-145">A atualização de dados pode levar até 10 milissegundos por coleta.</span><span class="sxs-lookup"><span data-stu-id="ff134-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="ff134-146">Em uma operação de atualização e coleta geral, todos os provedores de alto desempenho juntos não podem levar mais de 800 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ff134-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="ff134-147">A carga geral de CPU para todos os provedores de alto desempenho não pode exceder 6-7% de sobrecarga de CPU interativamente ou 5% para registro em log.</span><span class="sxs-lookup"><span data-stu-id="ff134-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff134-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff134-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff134-149">Criando um provedor de instância em um provedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="ff134-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
