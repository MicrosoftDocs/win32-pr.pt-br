---
description: O WMI define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes, além de propriedades específicas de classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Propriedades do sistema CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780305"
---
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="504bc-103">Propriedades do sistema CIM para objetos MIB</span><span class="sxs-lookup"><span data-stu-id="504bc-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="504bc-104">O WMI define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes, além de propriedades específicas de classe.</span><span class="sxs-lookup"><span data-stu-id="504bc-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="504bc-105">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="504bc-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="504bc-106">O provedor SNMP usa as seguintes propriedades do sistema CIM ao mapear definições de objeto MIB para definições de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="504bc-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="504bc-107">As propriedades obrigatórias devem estar presentes para que o provedor SNMP resolva completamente um objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="504bc-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="504bc-108">Falha ao definir uma propriedade obrigatória retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="504bc-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="504bc-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="504bc-109">Property</span></span></th>
<th><span data-ttu-id="504bc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="504bc-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="504bc-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="504bc-112"><strong>cadeia de caracteres</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-113">Para instâncias, a classe à qual o objeto pertence.</span><span class="sxs-lookup"><span data-stu-id="504bc-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="504bc-114">Para classes, esse é o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="504bc-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="504bc-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="504bc-116"><strong>cadeia de caracteres</strong> Adicional</span><span class="sxs-lookup"><span data-stu-id="504bc-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="504bc-117">Nome da classe que é a classe base definitiva para o objeto atual (não sua classe pai imediata).</span><span class="sxs-lookup"><span data-stu-id="504bc-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="504bc-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="504bc-119"><strong>UInt32</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-120">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="504bc-120">Type of object.</span></span> <span data-ttu-id="504bc-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="504bc-121">Values are:</span></span><br/> <dl> <span data-ttu-id="504bc-122">1 = classe</span><span class="sxs-lookup"><span data-stu-id="504bc-122">1 = class</span></span><br />
<span data-ttu-id="504bc-123">2 = instância</span><span class="sxs-lookup"><span data-stu-id="504bc-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="504bc-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="504bc-125"><strong>cadeia de caracteres</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-126">Namespace onde o objeto está localizado.</span><span class="sxs-lookup"><span data-stu-id="504bc-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="504bc-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="504bc-128"><strong>cadeia de caracteres</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-129">Caminho absoluto para o objeto.</span><span class="sxs-lookup"><span data-stu-id="504bc-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="504bc-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="504bc-131"><strong>UInt32</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-132">Número de propriedades que não são do sistema definidas para o objeto.</span><span class="sxs-lookup"><span data-stu-id="504bc-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="504bc-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="504bc-134"><strong>cadeia de caracteres</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-135">Caminho relativo para o objeto.</span><span class="sxs-lookup"><span data-stu-id="504bc-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="504bc-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="504bc-137"><strong>cadeia de caracteres</strong> Obrigatório</span><span class="sxs-lookup"><span data-stu-id="504bc-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="504bc-138">Servidor fornecendo o objeto.</span><span class="sxs-lookup"><span data-stu-id="504bc-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="504bc-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="504bc-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="504bc-140"><strong>cadeia de caracteres</strong> Adicional</span><span class="sxs-lookup"><span data-stu-id="504bc-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="504bc-141">Classe pai imediata do objeto.</span><span class="sxs-lookup"><span data-stu-id="504bc-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




