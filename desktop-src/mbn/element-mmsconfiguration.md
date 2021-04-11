---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164438"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="1e3d6-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e3d6-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="1e3d6-104">Informações de configuração para MMS (serviço de mensagens de multimídia).</span><span class="sxs-lookup"><span data-stu-id="1e3d6-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="1e3d6-105">Além de definir os elementos de configuração dentro deste elemento, um perfil MMS deve ter as seguintes configurações.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="1e3d6-106">Seu elemento [**Name**](element-name.md) deve conter um nome exclusivo em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="1e3d6-107">Seu [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) deve ser definido como **userprovisionado**.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="1e3d6-108">Seu [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) deve conter o ICCID do sim para o qual esse perfil se destina.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="1e3d6-109">Seu [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) deve ser definido como **manual**.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="1e3d6-110">Seu [**PurposeGroupGuid**](element-purposegroupguid.md) deve conter o GUID para o grupo de finalidade de MMS.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="1e3d6-111">Seu [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) deve ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1e3d6-112">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="1e3d6-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="1e3d6-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e3d6-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="1e3d6-114">Chave</span><span class="sxs-lookup"><span data-stu-id="1e3d6-114">Key</span></span>

<span data-ttu-id="1e3d6-115">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="1e3d6-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1e3d6-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="1e3d6-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1e3d6-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="1e3d6-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1e3d6-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1e3d6-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1e3d6-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e3d6-120">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="1e3d6-120">Child Element</span></span></th>
<th><span data-ttu-id="1e3d6-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e3d6-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e3d6-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="1e3d6-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="1e3d6-123">Especifica o tamanho máximo de mensagens MMS, em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="1e3d6-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e3d6-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="1e3d6-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="1e3d6-126">Especifica o número da porta do servidor MMSC para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="1e3d6-127">Especifique 0 para indicar que nenhuma porta específica foi especificada.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="1e3d6-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e3d6-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="1e3d6-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="1e3d6-130">Especifica a URL do servidor MMSC para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="1e3d6-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1e3d6-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1e3d6-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e3d6-133">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1e3d6-133">Parent Element</span></span></th>
<th><span data-ttu-id="1e3d6-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e3d6-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e3d6-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="1e3d6-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="1e3d6-136">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="1e3d6-137">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="1e3d6-138">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="1e3d6-139">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="1e3d6-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1e3d6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e3d6-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e3d6-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e3d6-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
