---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319146573e4782365b7db67c453a0866f198d61b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920894"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span data-ttu-id="2dcc1-103"><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl</span><span class="sxs-lookup"><span data-stu-id="2dcc1-103"><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl</span></span>

<span data-ttu-id="2dcc1-104">Especifica a URL do servidor MMSC para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-104">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="2dcc1-105">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="2dcc1-106">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="2dcc1-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscUrl>**

## <a name="syntax"></a><span data-ttu-id="2dcc1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dcc1-107">Syntax</span></span>

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="2dcc1-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="2dcc1-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="2dcc1-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="2dcc1-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="2dcc1-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="2dcc1-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2dcc1-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="2dcc1-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="2dcc1-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2dcc1-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2dcc1-114">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="2dcc1-114">Parent Element</span></span></th>
<th><span data-ttu-id="2dcc1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2dcc1-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2dcc1-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="2dcc1-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="2dcc1-117">Informações de configuração para MMS (serviço de mensagens de multimídia).</span><span class="sxs-lookup"><span data-stu-id="2dcc1-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="2dcc1-118">Além de definir os elementos de configuração dentro deste elemento, um perfil MMS deve ter as seguintes configurações.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="2dcc1-119">Seu elemento <a href="element-name.md"><strong>Name</strong></a> deve conter um nome exclusivo em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="2dcc1-120">Seu <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve ser definido como <strong>userprovisionado</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="2dcc1-121">Seu <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve conter o ICCID do sim para o qual esse perfil se destina.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="2dcc1-122">Seu <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve ser definido como <strong>manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="2dcc1-123">Seu <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve conter o GUID para o grupo de finalidade de MMS.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="2dcc1-124">Seu <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve ser definido como <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dcc1-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="2dcc1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dcc1-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dcc1-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="2dcc1-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
