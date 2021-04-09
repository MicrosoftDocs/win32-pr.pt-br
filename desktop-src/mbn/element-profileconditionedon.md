---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090310"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="a7af5-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span><span class="sxs-lookup"><span data-stu-id="a7af5-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="a7af5-104">Especifica as condições que devem ser satisfeitas para que um perfil seja aplicável.</span><span class="sxs-lookup"><span data-stu-id="a7af5-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="a7af5-105">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="a7af5-105">This element is new for v4.</span></span> <span data-ttu-id="a7af5-106">Ele permite que você especifique vários perfis que se aplicam em diferentes condições e para que o perfil apropriado seja usado automaticamente quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="a7af5-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="a7af5-107">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="a7af5-107">This element is optional.</span></span> <span data-ttu-id="a7af5-108">Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</span><span class="sxs-lookup"><span data-stu-id="a7af5-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a7af5-109">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="a7af5-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="a7af5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7af5-110">Syntax</span></span>

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a><span data-ttu-id="a7af5-111">Chave</span><span class="sxs-lookup"><span data-stu-id="a7af5-111">Key</span></span>

<span data-ttu-id="a7af5-112">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="a7af5-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a7af5-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="a7af5-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a7af5-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="a7af5-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a7af5-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a7af5-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a7af5-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a7af5-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7af5-117">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="a7af5-117">Child Element</span></span></th>
<th><span data-ttu-id="a7af5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7af5-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7af5-119"><a href="element-cellularclass.md">CellularClass</a></span><span class="sxs-lookup"><span data-stu-id="a7af5-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="a7af5-120">Especifica que esse perfil está ativo somente quando a classe celular atual é a especificada.</span><span class="sxs-lookup"><span data-stu-id="a7af5-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="a7af5-121">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="a7af5-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7af5-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="a7af5-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="a7af5-123">Especifica que esse perfil está ativo somente quando o IMSI atual que está sendo usado no ICCID é o especificado.</span><span class="sxs-lookup"><span data-stu-id="a7af5-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="a7af5-124">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="a7af5-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7af5-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span><span class="sxs-lookup"><span data-stu-id="a7af5-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="a7af5-126">Especifica que esse perfil está ativo somente quando conectado a uma rede IWLAN.</span><span class="sxs-lookup"><span data-stu-id="a7af5-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="a7af5-127">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="a7af5-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="a7af5-128">O valor desse elemento deve ser um valor <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> válido.</span><span class="sxs-lookup"><span data-stu-id="a7af5-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7af5-129"><a href="element-ratapplicability.md">RATApplicability</a></span><span class="sxs-lookup"><span data-stu-id="a7af5-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="a7af5-130">Especifica que esse perfil está ativo somente quando o tipo RAT é aquele especificado.</span><span class="sxs-lookup"><span data-stu-id="a7af5-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="a7af5-131">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="a7af5-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7af5-132"><a href="element-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="a7af5-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="a7af5-133">Especifica que esse perfil está ativo somente quando a condição de roaming atual é a especificada.</span><span class="sxs-lookup"><span data-stu-id="a7af5-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="a7af5-134">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="a7af5-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="a7af5-135">O valor desse elemento deve ser um valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</span><span class="sxs-lookup"><span data-stu-id="a7af5-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a7af5-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a7af5-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7af5-137">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a7af5-137">Parent Element</span></span></th>
<th><span data-ttu-id="a7af5-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7af5-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7af5-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="a7af5-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="a7af5-140">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="a7af5-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a7af5-141">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="a7af5-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="a7af5-142">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="a7af5-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a7af5-143">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="a7af5-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a7af5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7af5-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7af5-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7af5-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



