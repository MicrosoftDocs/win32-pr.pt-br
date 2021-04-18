---
description: Subscriberid
MS-HAID: WWAN\_profile\_v4.element\_SubscriberID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Subscriberid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525cd75dbf1ab752ab17ea32d566e57977ab74a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760366"
---
# <a name="span-idwwan_profile_v4element_subscriberidspansubscriberid"></a><span data-ttu-id="d37ec-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>Subscriberid</span><span class="sxs-lookup"><span data-stu-id="d37ec-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span></span>

<span data-ttu-id="d37ec-104">Identifica o identificador exclusivo do perfil.</span><span class="sxs-lookup"><span data-stu-id="d37ec-104">Identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="d37ec-105">Para uma rede GSM, isso deve conter a IMSI (identidade do assinante internacional móvel) do SIM e para dispositivos CDMA que ele deve conter o mínimo (número de identificação móvel) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d37ec-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="d37ec-106">Para obter mais informações, consulte a documentação para o elemento [**subscriberid**](./schema-subscriberid-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="d37ec-106">For more information, see the documentation for the v1 [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d37ec-107">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="d37ec-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<SubscriberID>**

## <a name="syntax"></a><span data-ttu-id="d37ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d37ec-108">Syntax</span></span>

``` syntax
<SubscriberID>

  subscriberIdType

</SubscriberID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d37ec-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="d37ec-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d37ec-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="d37ec-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d37ec-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d37ec-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d37ec-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d37ec-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d37ec-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d37ec-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d37ec-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d37ec-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d37ec-115">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="d37ec-115">Parent Element</span></span></th>
<th><span data-ttu-id="d37ec-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d37ec-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d37ec-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="d37ec-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="d37ec-118">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="d37ec-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="d37ec-119">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="d37ec-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="d37ec-120">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="d37ec-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="d37ec-121">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="d37ec-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d37ec-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d37ec-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d37ec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d37ec-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
