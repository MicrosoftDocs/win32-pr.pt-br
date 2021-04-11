---
description: O WMI tem vários tipos de qualificadores de classe e de propriedade. Os qualificadores também podem ter tipos de modificação.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Qualificadores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165182"
---
# <a name="wmi-qualifiers"></a><span data-ttu-id="1ff32-104">Qualificadores WMI</span><span class="sxs-lookup"><span data-stu-id="1ff32-104">WMI Qualifiers</span></span>

<span data-ttu-id="1ff32-105">O WMI tem vários tipos de [*qualificadores*](gloss-q.md)de classe e de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1ff32-105">WMI has several types of class and property [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="1ff32-106">Os qualificadores também podem ter [*tipos*](gloss-f.md)de modificação.</span><span class="sxs-lookup"><span data-stu-id="1ff32-106">Qualifiers can also have modifying [*flavors*](gloss-f.md).</span></span> <span data-ttu-id="1ff32-107">Os seguintes tipos de qualificadores e versões são usados no WMI.</span><span class="sxs-lookup"><span data-stu-id="1ff32-107">The following types of qualifiers and flavors are used in WMI.</span></span>

<span data-ttu-id="1ff32-108">O nome de cada qualificador é exibido com seu tipo de dados e um indicador de se o qualificador pode ser aplicado a uma classe, instância, propriedade ou método.</span><span class="sxs-lookup"><span data-stu-id="1ff32-108">The name of each qualifier appears with its data type and an indicator of whether the qualifier can be applied to a class, instance, property, or method.</span></span> <span data-ttu-id="1ff32-109">Para qualificadores como a **Associação** (discutida em [meta Qualifiers](meta-qualifiers.md)), há uma regra de uso implícita que o meta Qualifier também deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="1ff32-109">For qualifiers such as **Association** (discussed under [Meta Qualifiers](meta-qualifiers.md)), there is an implied usage rule that the meta qualifier must also be present.</span></span> <span data-ttu-id="1ff32-110">Por exemplo, a regra de uso implícito para os qualificadores de **agregação** é que o qualificador de **Associação** também deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="1ff32-110">For example, the implicit usage rule for the **Aggregation** qualifiers is that the **Association** qualifier must also be present.</span></span>



| <span data-ttu-id="1ff32-111">Tipo de qualificador</span><span class="sxs-lookup"><span data-stu-id="1ff32-111">Qualifier type</span></span>                              | <span data-ttu-id="1ff32-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ff32-112">Description</span></span>                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ff32-113">Volume</span><span class="sxs-lookup"><span data-stu-id="1ff32-113">Meta</span></span>](meta-qualifiers.md)                 | <span data-ttu-id="1ff32-114">Restringe a definição de metaconstruções esclarecendo o uso real de uma classe ou declaração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1ff32-114">Refines the definition of meta-constructs by clarifying the actual usage of a class or property declaration.</span></span>                          |
| [<span data-ttu-id="1ff32-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="1ff32-115">Optional</span></span>](optional-qualifiers.md)         | <span data-ttu-id="1ff32-116">As situações de endereços não são comuns a todas as implementações em conformidade com o CIM.</span><span class="sxs-lookup"><span data-stu-id="1ff32-116">Addresses situations not common to all CIM-compliant implementations.</span></span>                                                                 |
| [<span data-ttu-id="1ff32-117">Tipos de qualificadores</span><span class="sxs-lookup"><span data-stu-id="1ff32-117">Qualifier Flavors</span></span>](qualifier-flavors.md)  | <span data-ttu-id="1ff32-118">Fornece mais informações sobre um qualificador, como se uma classe ou instância derivada pode substituir o valor original do qualificador.</span><span class="sxs-lookup"><span data-stu-id="1ff32-118">Provides more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span> |
| [<span data-ttu-id="1ff32-119">Standard</span><span class="sxs-lookup"><span data-stu-id="1ff32-119">Standard</span></span>](standard-qualifiers.md)         | <span data-ttu-id="1ff32-120">Dá suporte às descrições que todas as implementações compatíveis com CIM devem manipular.</span><span class="sxs-lookup"><span data-stu-id="1ff32-120">Supports the descriptions that all CIM-compliant implementations must handle.</span></span>                                                         |
| [<span data-ttu-id="1ff32-121">Específico do WMI</span><span class="sxs-lookup"><span data-stu-id="1ff32-121">WMI-specific</span></span>](wmi-specific-qualifiers.md) | <span data-ttu-id="1ff32-122">Descreve os qualificadores específicos ao WMI, como qualificadores de classe de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="1ff32-122">Describes qualifiers specific to WMI, such as performance counter class qualifiers.</span></span>                                                   |



 

<span data-ttu-id="1ff32-123">Para obter mais informações sobre como aplicar qualificadores a suas classes WMI, consulte [adicionando um qualificador](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="1ff32-123">For more information on applying qualifiers to your WMI classes, see [Adding a Qualifier](adding-a-qualifier.md).</span></span> <span data-ttu-id="1ff32-124">Para ver como examinar qualificadores em classes WMI existentes, consulte o código de exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="1ff32-124">To see how to examine qualifiers on existing WMI classes, see the example code below.</span></span>

## <a name="example"></a><span data-ttu-id="1ff32-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1ff32-125">Example</span></span>

<span data-ttu-id="1ff32-126">O código do PowerShell a seguir, extraído da [Galeria do TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), descreve como recuperar qualificadores de uma classe WMI.</span><span class="sxs-lookup"><span data-stu-id="1ff32-126">The following PowerShell code, taken from the [TechNet gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describes how to retrieve qualifiers from a WMI class.</span></span>


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 



