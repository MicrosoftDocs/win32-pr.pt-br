---
description: ModemDMConfigProfile \/ AdminRoamControl (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AdminRoamControl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AdminRoamControl (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92ba97fd2657b28d1c845598825aae648124d36
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388867"
---
# <a name="span-idwwan_profile_v4element_1_adminroamcontrolspanmodemdmconfigprofileadminroamcontrol-v4"></a><span data-ttu-id="0258c-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile \/ AdminRoamControl (v4)</span><span class="sxs-lookup"><span data-stu-id="0258c-103"><span id="WWAN_profile_v4.element_1_AdminRoamControl"></span>ModemDMConfigProfile\/AdminRoamControl (v4)</span></span>

<span data-ttu-id="0258c-104">Especifica se o perfil é controlado por roaming de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="0258c-104">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="0258c-105">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="0258c-105">This element is new for v4.</span></span> <span data-ttu-id="0258c-106">O valor desse elemento é um valor de [**roamControlType**](simpletype-roamcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="0258c-106">The value of this element is a [**roamControlType**](simpletype-roamcontroltype.md) value.</span></span> <span data-ttu-id="0258c-107">Este é um elemento opcional; Se nenhum valor for especificado, **AllRoamAllowed** será o padrão.</span><span class="sxs-lookup"><span data-stu-id="0258c-107">This is an optional element; if no value is specified, then **AllRoamAllowed** is the default.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0258c-108">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="0258c-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

## <a name="syntax"></a><span data-ttu-id="0258c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0258c-109">Syntax</span></span>

``` syntax
<AdminRoamControl>

  "AllRoamAllowed" | "PartnerRoamAllowed" | "NoRoamAllowed"

</AdminRoamControl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0258c-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="0258c-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0258c-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="0258c-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0258c-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0258c-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0258c-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0258c-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0258c-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0258c-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0258c-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0258c-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0258c-116">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0258c-116">Parent Element</span></span></th>
<th><span data-ttu-id="0258c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0258c-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0258c-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="0258c-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="0258c-119">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="0258c-119">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="0258c-120">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="0258c-120">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="0258c-121">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="0258c-121">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="0258c-122">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="0258c-122">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0258c-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="0258c-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="0258c-124">Perfil de configuração de DM de modem.</span><span class="sxs-lookup"><span data-stu-id="0258c-124">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="0258c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0258c-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0258c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="0258c-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



