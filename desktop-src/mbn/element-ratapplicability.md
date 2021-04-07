---
description: RATApplicability
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RATApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155f8e216b6ec00f123d0fe0f378fd9db2e4d75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827213"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span data-ttu-id="987cb-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span><span class="sxs-lookup"><span data-stu-id="987cb-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span></span>

<span data-ttu-id="987cb-104">Especifica que esse perfil está ativo somente quando o tipo RAT é aquele especificado.</span><span class="sxs-lookup"><span data-stu-id="987cb-104">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="987cb-105">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="987cb-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="987cb-106">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="987cb-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<RATApplicability>**

## <a name="syntax"></a><span data-ttu-id="987cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="987cb-107">Syntax</span></span>

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="987cb-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="987cb-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="987cb-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="987cb-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="987cb-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="987cb-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="987cb-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="987cb-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="987cb-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="987cb-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="987cb-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="987cb-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="987cb-114">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="987cb-114">Parent Element</span></span></th>
<th><span data-ttu-id="987cb-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="987cb-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987cb-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="987cb-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="987cb-117">Especifica as condições que devem ser satisfeitas para que um perfil seja aplicável.</span><span class="sxs-lookup"><span data-stu-id="987cb-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="987cb-118">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="987cb-118">This element is new for v4.</span></span> <span data-ttu-id="987cb-119">Ele permite que você especifique vários perfis que se aplicam em diferentes condições e para que o perfil apropriado seja usado automaticamente quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="987cb-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="987cb-120">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="987cb-120">This element is optional.</span></span> <span data-ttu-id="987cb-121">Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</span><span class="sxs-lookup"><span data-stu-id="987cb-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="987cb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="987cb-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="987cb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="987cb-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



