---
description: ModemDMConfigProfile \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d78618598b758d4c2654f0f2911637e638aacf
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388792"
---
# <a name="span-idwwan_profile_v4element_1_roamapplicabilityspanmodemdmconfigprofileroamapplicability-v4"></a><span data-ttu-id="17b9b-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>ModemDMConfigProfile \/ RoamApplicability (v4)</span><span class="sxs-lookup"><span data-stu-id="17b9b-103"><span id="WWAN_profile_v4.element_1_RoamApplicability"></span>ModemDMConfigProfile\/RoamApplicability (v4)</span></span>

<span data-ttu-id="17b9b-104">Especifica que esse perfil está ativo somente quando a condição de roaming atual é a especificada.</span><span class="sxs-lookup"><span data-stu-id="17b9b-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="17b9b-105">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="17b9b-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="17b9b-106">O valor desse elemento deve ser um valor [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) válido.</span><span class="sxs-lookup"><span data-stu-id="17b9b-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="17b9b-107">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="17b9b-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="17b9b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b9b-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="17b9b-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="17b9b-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="17b9b-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="17b9b-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="17b9b-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="17b9b-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="17b9b-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="17b9b-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="17b9b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="17b9b-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="17b9b-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="17b9b-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17b9b-115">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="17b9b-115">Parent Element</span></span></th>
<th><span data-ttu-id="17b9b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="17b9b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17b9b-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="17b9b-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="17b9b-118">Perfil de configuração de DM de modem.</span><span class="sxs-lookup"><span data-stu-id="17b9b-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17b9b-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="17b9b-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="17b9b-120">Especifica as condições que devem ser satisfeitas para que um perfil seja aplicável.</span><span class="sxs-lookup"><span data-stu-id="17b9b-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="17b9b-121">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="17b9b-121">This element is new for v4.</span></span> <span data-ttu-id="17b9b-122">Ele permite que você especifique vários perfis que se aplicam em diferentes condições e para que o perfil apropriado seja usado automaticamente quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="17b9b-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="17b9b-123">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="17b9b-123">This element is optional.</span></span> <span data-ttu-id="17b9b-124">Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</span><span class="sxs-lookup"><span data-stu-id="17b9b-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="17b9b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b9b-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="17b9b-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



