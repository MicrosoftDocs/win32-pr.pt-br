---
description: MmscPort
MS-HAID: WWAN\_profile\_v4.element\_MmscPort
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscPort
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08812a87b404cdec3caab43d56d4b9afdca9212b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296404"
---
# <a name="span-idwwan_profile_v4element_mmscportspanmmscport"></a><span data-ttu-id="1261b-103"><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort</span><span class="sxs-lookup"><span data-stu-id="1261b-103"><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort</span></span>

<span data-ttu-id="1261b-104">Especifica o número da porta do servidor MMSC para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1261b-104">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="1261b-105">Especifique 0 para indicar que nenhuma porta específica foi especificada.</span><span class="sxs-lookup"><span data-stu-id="1261b-105">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="1261b-106">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1261b-106">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1261b-107">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="1261b-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscPort>**

## <a name="syntax"></a><span data-ttu-id="1261b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1261b-108">Syntax</span></span>

``` syntax
<MmscPort>

  [TBD (missing description)]

</MmscPort>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1261b-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="1261b-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1261b-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="1261b-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1261b-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1261b-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1261b-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1261b-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1261b-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1261b-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1261b-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1261b-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1261b-115">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1261b-115">Parent Element</span></span></th>
<th><span data-ttu-id="1261b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1261b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1261b-117"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="1261b-117"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="1261b-118">Informações de configuração para MMS (serviço de mensagens de multimídia).</span><span class="sxs-lookup"><span data-stu-id="1261b-118">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="1261b-119">Além de definir os elementos de configuração dentro deste elemento, um perfil MMS deve ter as seguintes configurações.</span><span class="sxs-lookup"><span data-stu-id="1261b-119">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="1261b-120">Seu elemento <a href="element-name.md"><strong>Name</strong></a> deve conter um nome exclusivo em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="1261b-120">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="1261b-121">Seu <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve ser definido como <strong>userprovisionado</strong>.</span><span class="sxs-lookup"><span data-stu-id="1261b-121">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="1261b-122">Seu <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve conter o ICCID do sim para o qual esse perfil se destina.</span><span class="sxs-lookup"><span data-stu-id="1261b-122">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="1261b-123">Seu <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve ser definido como <strong>manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="1261b-123">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="1261b-124">Seu <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve conter o GUID para o grupo de finalidade de MMS.</span><span class="sxs-lookup"><span data-stu-id="1261b-124">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="1261b-125">Seu <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve ser definido como <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="1261b-125">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1261b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1261b-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1261b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1261b-127">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
