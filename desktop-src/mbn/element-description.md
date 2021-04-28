---
description: Descrição (banda larga móvel)-Descrição
MS-HAID: WWAN\_profile\_v4.element\_Description
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Descrição (banda larga móvel)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7adc4b26-1202-4f80-8b26-7879df687bb0
api_name:
- Description
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e72b2fca1df6ba76d933d289b5d73b717cb6af6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107014"
---
# <a name="description-mobile-broadband"></a><span data-ttu-id="9f5c4-103">Descrição (banda larga móvel)</span><span class="sxs-lookup"><span data-stu-id="9f5c4-103">Description (Mobile Broadband)</span></span>

<span data-ttu-id="9f5c4-104">Uma descrição do perfil.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-104">A description of the profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="9f5c4-105">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="9f5c4-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<Description>**

## <a name="syntax"></a><span data-ttu-id="9f5c4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f5c4-106">Syntax</span></span>

``` syntax
<Description>

  nameType

</Description>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="9f5c4-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="9f5c4-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="9f5c4-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="9f5c4-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="9f5c4-109">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="9f5c4-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9f5c4-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="9f5c4-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="9f5c4-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9f5c4-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f5c4-113">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="9f5c4-113">Parent Element</span></span></th>
<th><span data-ttu-id="9f5c4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f5c4-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f5c4-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="9f5c4-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="9f5c4-116">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="9f5c4-117">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="9f5c4-118">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="9f5c4-119">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="9f5c4-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="9f5c4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f5c4-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f5c4-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f5c4-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



