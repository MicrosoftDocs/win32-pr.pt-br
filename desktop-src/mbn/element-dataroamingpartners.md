---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6df58bc0765b5254645c45270f8145f5d10d422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762140"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span data-ttu-id="208f0-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span><span class="sxs-lookup"><span data-stu-id="208f0-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span></span>

<span data-ttu-id="208f0-104">Especifica uma lista de provedores de rede preferenciais durante o roaming.</span><span class="sxs-lookup"><span data-stu-id="208f0-104">Specifies a list of preferred network providers when roaming.</span></span>

<span data-ttu-id="208f0-105">Para obter detalhes, consulte a documentação do elemento v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="208f0-105">For details, see the documentation for the v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="208f0-106">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="208f0-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a><span data-ttu-id="208f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="208f0-107">Syntax</span></span>

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a><span data-ttu-id="208f0-108">Chave</span><span class="sxs-lookup"><span data-stu-id="208f0-108">Key</span></span>

<span data-ttu-id="208f0-109">`+`   necessário (um ou mais)</span><span class="sxs-lookup"><span data-stu-id="208f0-109">`+`   required (one or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="208f0-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="208f0-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="208f0-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="208f0-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="208f0-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="208f0-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="208f0-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="208f0-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="208f0-114">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="208f0-114">Child Element</span></span></th>
<th><span data-ttu-id="208f0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="208f0-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="208f0-116"><a href="element-provider.md">Provedor</a></span><span class="sxs-lookup"><span data-stu-id="208f0-116"><a href="element-provider.md">Provider</a></span></span></td>
<td><p><span data-ttu-id="208f0-117">Especifica um provedor de rede preferencial em uma lista de provedores a serem usados durante o roaming.</span><span class="sxs-lookup"><span data-stu-id="208f0-117">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span></p>
<p><span data-ttu-id="208f0-118">O valor desse elemento é uma instância do tipo complexo v1 <a href="../mbn/schema-providertype-complextype.md"><strong>ProviderType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="208f0-118">The value of this element is an instance of the v1 <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> complex type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="208f0-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="208f0-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="208f0-120">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="208f0-120">Parent Element</span></span></th>
<th><span data-ttu-id="208f0-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="208f0-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="208f0-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="208f0-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="208f0-123">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="208f0-123">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="208f0-124">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="208f0-124">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="208f0-125">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="208f0-125">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="208f0-126">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="208f0-126">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="208f0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="208f0-127">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="208f0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="208f0-128">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
