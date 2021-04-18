---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763817"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="987f3-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span><span class="sxs-lookup"><span data-stu-id="987f3-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="987f3-104">Uma lista opcional de grupos de perfis, onde cada grupo inclui perfis usados para uma finalidade comum.</span><span class="sxs-lookup"><span data-stu-id="987f3-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="987f3-105">Este elemento é novo para v4 do esquema.</span><span class="sxs-lookup"><span data-stu-id="987f3-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="987f3-106">Um perfil pode ser listado em vários grupos.</span><span class="sxs-lookup"><span data-stu-id="987f3-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="987f3-107">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="987f3-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="987f3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="987f3-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="987f3-109">Chave</span><span class="sxs-lookup"><span data-stu-id="987f3-109">Key</span></span>

<span data-ttu-id="987f3-110">`{}`   intervalo específico de ocorrências</span><span class="sxs-lookup"><span data-stu-id="987f3-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="987f3-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="987f3-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="987f3-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="987f3-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="987f3-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="987f3-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="987f3-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="987f3-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="987f3-115">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="987f3-115">Child Element</span></span></th>
<th><span data-ttu-id="987f3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="987f3-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987f3-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span><span class="sxs-lookup"><span data-stu-id="987f3-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="987f3-118">Representa um perfil em um dos perfis.</span><span class="sxs-lookup"><span data-stu-id="987f3-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="987f3-119">Os perfis são especificados pelo valor de <a href="simpletype-guidtype.md"><strong>guidtype</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="987f3-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="987f3-120">Quatro valores GUID são definidos, conforme listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="987f3-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="987f3-121">Grupo de finalidade</span><span class="sxs-lookup"><span data-stu-id="987f3-121">Purpose group</span></span></th>
<th><span data-ttu-id="987f3-122">GUID</span><span class="sxs-lookup"><span data-stu-id="987f3-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987f3-123">Internet</span><span class="sxs-lookup"><span data-stu-id="987f3-123">Internet</span></span></td>
<td><span data-ttu-id="987f3-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="987f3-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="987f3-125">mms</span><span class="sxs-lookup"><span data-stu-id="987f3-125">MMS</span></span></td>
<td><span data-ttu-id="987f3-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="987f3-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="987f3-127">IMS</span><span class="sxs-lookup"><span data-stu-id="987f3-127">IMS</span></span></td>
<td><span data-ttu-id="987f3-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="987f3-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="987f3-129">SUPL</span><span class="sxs-lookup"><span data-stu-id="987f3-129">SUPL</span></span></td>
<td><span data-ttu-id="987f3-130">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="987f3-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="987f3-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="987f3-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="987f3-132">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="987f3-132">Parent Element</span></span></th>
<th><span data-ttu-id="987f3-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="987f3-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987f3-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="987f3-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="987f3-135">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="987f3-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="987f3-136">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="987f3-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="987f3-137">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="987f3-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="987f3-138">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="987f3-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="987f3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="987f3-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="987f3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="987f3-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



