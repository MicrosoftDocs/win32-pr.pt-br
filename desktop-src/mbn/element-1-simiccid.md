---
description: ModemDMConfigProfile \/ SimIccID (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_SimIccID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SimIccID (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74a93e9fef6ad41ef4056c0a813c71d98e2ff6e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388783"
---
# <a name="span-idwwan_profile_v4element_1_simiccidspanmodemdmconfigprofilesimiccid-v4"></a><span data-ttu-id="7b613-103"><span id="WWAN_profile_v4.element_1_SimIccID"></span>ModemDMConfigProfile \/ SimIccID (v4)</span><span class="sxs-lookup"><span data-stu-id="7b613-103"><span id="WWAN_profile_v4.element_1_SimIccID"></span>ModemDMConfigProfile\/SimIccID (v4)</span></span>

<span data-ttu-id="7b613-104">O número de Identifcation do SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="7b613-104">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="7b613-105">Para obter mais detalhes, consulte a documentação do elemento v1 [**SimIccID**](./schema-simiccid-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7b613-105">For more details , see the documentation for the v1 [**SimIccID**](./schema-simiccid-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="7b613-106">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="7b613-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<SimIccID\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<SimIccID\>**

## <a name="syntax"></a><span data-ttu-id="7b613-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b613-107">Syntax</span></span>

``` syntax
<SimIccID>

  simIccIDType

</SimIccID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="7b613-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="7b613-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="7b613-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="7b613-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="7b613-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7b613-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="7b613-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7b613-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="7b613-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7b613-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="7b613-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7b613-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b613-114">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="7b613-114">Parent Element</span></span></th>
<th><span data-ttu-id="7b613-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b613-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b613-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="7b613-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="7b613-117">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="7b613-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="7b613-118">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="7b613-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="7b613-119">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="7b613-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="7b613-120">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="7b613-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b613-121"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="7b613-121"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="7b613-122">Perfil de configuração de DM de modem.</span><span class="sxs-lookup"><span data-stu-id="7b613-122">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="7b613-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b613-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b613-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b613-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
