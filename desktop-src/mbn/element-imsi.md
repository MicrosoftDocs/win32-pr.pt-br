---
description: IMSI
MS-HAID: WWAN\_profile\_v4.element\_IMSI
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IMSI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d873cbc5634f78b8bcb802daea9c6dd0a667b32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501653"
---
# <a name="span-idwwan_profile_v4element_imsispanimsi"></a><span data-ttu-id="51f19-103"><span id="WWAN_profile_v4.element_IMSI"></span>IMSI</span><span class="sxs-lookup"><span data-stu-id="51f19-103"><span id="WWAN_profile_v4.element_IMSI"></span>IMSI</span></span>

<span data-ttu-id="51f19-104">Especifica que esse perfil está ativo somente quando o IMSI atual que está sendo usado no ICCID é o especificado.</span><span class="sxs-lookup"><span data-stu-id="51f19-104">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="51f19-105">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="51f19-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="51f19-106">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="51f19-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IMSI>**

## <a name="syntax"></a><span data-ttu-id="51f19-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="51f19-107">Syntax</span></span>

``` syntax
<IMSI>

  subscriberIdType

</IMSI>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="51f19-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="51f19-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="51f19-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="51f19-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="51f19-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="51f19-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="51f19-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="51f19-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="51f19-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="51f19-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="51f19-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="51f19-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51f19-114">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="51f19-114">Parent Element</span></span></th>
<th><span data-ttu-id="51f19-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="51f19-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51f19-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="51f19-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="51f19-117">Especifica as condições que devem ser satisfeitas para que um perfil seja aplicável.</span><span class="sxs-lookup"><span data-stu-id="51f19-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="51f19-118">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="51f19-118">This element is new for v4.</span></span> <span data-ttu-id="51f19-119">Ele permite que você especifique vários perfis que se aplicam em diferentes condições e para que o perfil apropriado seja usado automaticamente quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="51f19-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="51f19-120">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="51f19-120">This element is optional.</span></span> <span data-ttu-id="51f19-121">Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</span><span class="sxs-lookup"><span data-stu-id="51f19-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="51f19-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51f19-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51f19-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="51f19-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



