---
description: Uma classe de exibição de junção contém propriedades de instâncias de classe de origem que são conectadas por um valor de propriedade comum, como Class1. Prop1 = class2. Prop2. Cada instância em uma classe de exibição de junção consiste em partes de instâncias de classe diferentes.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Criando uma nova instância de propriedades antigas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922596"
---
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="58046-104">Criando uma nova instância de propriedades antigas</span><span class="sxs-lookup"><span data-stu-id="58046-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="58046-105">Uma classe de exibição de junção contém propriedades de instâncias de classe de origem que são conectadas por um valor de propriedade comum, como **Class1. Prop1**  =  **class2. Prop2**.</span><span class="sxs-lookup"><span data-stu-id="58046-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="58046-106">Cada instância em uma classe de exibição de junção consiste em partes de instâncias de classe diferentes.</span><span class="sxs-lookup"><span data-stu-id="58046-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="58046-107">Você pode basear uma classe de exibição de junção em desigualdade de valores de propriedade, como **Class1. Prop1**  <>  **class2. Prop2** , em que **Prop1** e **Prop2** não são mapeados para a mesma propriedade na classe View.</span><span class="sxs-lookup"><span data-stu-id="58046-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="58046-108">Uma classe de exibição de junção é útil quando as informações que você está procurando estão contidas em classes separadas, mas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="58046-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="58046-109">Por exemplo, se você quiser obter informações sobre uma impressora e sobre a configuração da impressora, poderá criar uma classe de exibição de junção que contenha algumas das propriedades da classe de [**\_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e algumas das propriedades da classe [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="58046-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="58046-110">Sem o provedor de exibição, você deve recuperar e mesclar as propriedades das instâncias separadas para obter as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="58046-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="58046-111">O procedimento a seguir descreve como criar uma classe de exibição de junção.</span><span class="sxs-lookup"><span data-stu-id="58046-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="58046-112">**Para criar uma classe de exibição de junção**</span><span class="sxs-lookup"><span data-stu-id="58046-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="58046-113">Inicie uma definição de classe com o qualificador de cadeia de [**junção**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="58046-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="58046-114">Os qualificadores [**junção**](qualifiers-specific-to-the-view-provider.md), **Associação** e **União** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="58046-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="58046-115">Se necessário, filtre as instâncias desejadas na classe Join aplicando o qualificador [**PostJoinFilter**](postjoinfilter-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="58046-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="58046-116">O provedor [**PostJoinFilter**](postjoinfilter-qualifier.md) permite restringir as instâncias de uma classe de exibição para instâncias que atendem a condições específicas.</span><span class="sxs-lookup"><span data-stu-id="58046-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="58046-117">Crie as consultas que definem instâncias de origem da classe View com o qualificador [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="58046-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="58046-118">Defina os nomes e locais dos namespaces onde as instâncias de origem estão localizadas com o qualificador [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="58046-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="58046-119">Defina as propriedades desejadas em uma classe de exibição de junção com o qualificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="58046-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="58046-120">Quando as propriedades são adicionadas à exibição de junção com base na igualdade, as duas propriedades de origem devem ser mapeadas em um qualificador de [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="58046-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="58046-121">O exemplo de código a seguir mostra duas propriedades mapeadas em um qualificador **PropertySources** .</span><span class="sxs-lookup"><span data-stu-id="58046-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="58046-122">Usando o qualificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , você pode marcar as propriedades que pertencem a uma classe de origem.</span><span class="sxs-lookup"><span data-stu-id="58046-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="58046-123">O exemplo de código a seguir mostra uma classe de exibição de junção criada a partir das classes do provedor do monitor de desempenho [**Win32 \_ PerfRawData \_ PerfProc \_ process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) e [**Win32 \_ PerfRawData \_ PerfProc \_ thread**](/previous-versions//aa394325(v=vs.85)) com propriedades de ambas as classes Unidas pela propriedade **ProcessId** .</span><span class="sxs-lookup"><span data-stu-id="58046-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
