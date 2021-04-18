---
description: ICONFilePath
MS-HAID: WWAN\_profile\_v4.element\_ICONFilePath
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICONFilePath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273f8a48cb099c95aaa0b54d438e06b3e1f0bb63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793728"
---
# <a name="span-idwwan_profile_v4element_iconfilepathspaniconfilepath"></a><span data-ttu-id="8d293-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span><span class="sxs-lookup"><span data-stu-id="8d293-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span></span>

<span data-ttu-id="8d293-104">O caminho para o arquivo de ícone da conexão.</span><span class="sxs-lookup"><span data-stu-id="8d293-104">The path to the icon file for the connection.</span></span> <span data-ttu-id="8d293-105">A interface do usuário conexão do sistema operacional exibe o ícone quando uma conexão é feita usando esse perfil.</span><span class="sxs-lookup"><span data-stu-id="8d293-105">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span>

<span data-ttu-id="8d293-106">Para obter mais detalhes sobre como usar esse elemento, consulte a documentação v1 para [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="8d293-106">For more details on using this element, see the v1 documentation for [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="8d293-107">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="8d293-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ICONFilePath>**

## <a name="syntax"></a><span data-ttu-id="8d293-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d293-108">Syntax</span></span>

``` syntax
<ICONFilePath>

  iconFileType

</ICONFilePath>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="8d293-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="8d293-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="8d293-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="8d293-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="8d293-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8d293-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="8d293-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8d293-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="8d293-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8d293-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="8d293-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8d293-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d293-115">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8d293-115">Parent Element</span></span></th>
<th><span data-ttu-id="8d293-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d293-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d293-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="8d293-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="8d293-118">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="8d293-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="8d293-119">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="8d293-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="8d293-120">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="8d293-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="8d293-121">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="8d293-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="8d293-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d293-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d293-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d293-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
