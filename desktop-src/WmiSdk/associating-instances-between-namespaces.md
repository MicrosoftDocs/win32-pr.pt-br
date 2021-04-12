---
description: Uma classe de exibição de associação permite que você use ASSOCIAdores de consultas em classes que residem em namespaces diferentes.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associando instâncias entre namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296894"
---
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="55381-103">Associando instâncias entre namespaces</span><span class="sxs-lookup"><span data-stu-id="55381-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="55381-104">Uma classe de exibição de associação permite que você use [ASSOCIADORES de](associators-of-statement.md) consultas em classes que residem em namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="55381-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="55381-105">O procedimento a seguir descreve como associar instâncias entre namespaces.</span><span class="sxs-lookup"><span data-stu-id="55381-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="55381-106">**Para associar instâncias entre namespaces**</span><span class="sxs-lookup"><span data-stu-id="55381-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="55381-107">Comece sua definição de classe com o qualificador de cadeia de [**Associação**](meta-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="55381-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="55381-108">Os qualificadores **junção**, [**Associação**](meta-qualifiers.md)e **União** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="55381-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="55381-109">Crie as consultas que definem as instâncias de origem usadas na classe View com o qualificador [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="55381-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="55381-110">Defina os nomes e o local dos namespaces nos quais as instâncias de origem estão localizadas com o qualificador [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="55381-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="55381-111">Defina as propriedades desejadas em sua classe de exibição de associação com o qualificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="55381-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="55381-112">Se necessário, você pode marcar qualquer uma das propriedades como pertencente a uma classe de origem usando o qualificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="55381-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="55381-113">Marque todas as propriedades relevantes com o qualificador **direto** .</span><span class="sxs-lookup"><span data-stu-id="55381-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="55381-114">O qualificador **direto** impede que o provedor de exibição mapeie a referência de associação marcada para uma referência de exibição.</span><span class="sxs-lookup"><span data-stu-id="55381-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="55381-115">Os exemplos de código a seguir mostram como criar classes de exibição de associação.</span><span class="sxs-lookup"><span data-stu-id="55381-115">The following code examples show how to create association view classes.</span></span>

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



