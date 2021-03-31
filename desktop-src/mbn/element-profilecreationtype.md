---
description: ProfileCreationType (em MBNProfileExt)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (em MBNProfileExt)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56e09a18721bfa7d5f33d8e7511122f3d731f4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647263"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span data-ttu-id="f85da-103"><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (em MBNProfileExt)</span><span class="sxs-lookup"><span data-stu-id="f85da-103"><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (in MBNProfileExt)</span></span>

<span data-ttu-id="f85da-104">Especifica o criador do perfil.</span><span class="sxs-lookup"><span data-stu-id="f85da-104">Specifies the creator of the profile.</span></span>

<span data-ttu-id="f85da-105">Para obter mais informações sobre esse elemento, consulte a documentação do elemento v1 [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f85da-105">For more information about this element, see the documentation for the v1 [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f85da-106">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="f85da-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="f85da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f85da-107">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f85da-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="f85da-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f85da-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="f85da-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f85da-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f85da-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f85da-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f85da-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="f85da-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f85da-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f85da-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f85da-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f85da-114">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f85da-114">Parent Element</span></span></th>
<th><span data-ttu-id="f85da-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f85da-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f85da-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="f85da-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="f85da-117">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="f85da-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="f85da-118">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="f85da-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="f85da-119">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="f85da-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="f85da-120">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="f85da-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="f85da-121">Elementos relacionados</span><span class="sxs-lookup"><span data-stu-id="f85da-121">Related elements</span></span>

<span data-ttu-id="f85da-122">Os elementos a seguir têm o mesmo nome que este, mas um conteúdo ou atributos diferentes:</span><span class="sxs-lookup"><span data-stu-id="f85da-122">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="f85da-123">**[ProfileCreationType (em ModemDMConfigProfile)](element-1-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="f85da-123">**[ProfileCreationType (in ModemDMConfigProfile)](element-1-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="f85da-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f85da-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f85da-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f85da-125">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
