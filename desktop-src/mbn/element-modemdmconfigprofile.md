---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748881"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="2e042-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span><span class="sxs-lookup"><span data-stu-id="2e042-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="2e042-104">Perfil de configuração de DM de modem.</span><span class="sxs-lookup"><span data-stu-id="2e042-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="2e042-105">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="2e042-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="2e042-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e042-106">Syntax</span></span>

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a><span data-ttu-id="2e042-107">Chave</span><span class="sxs-lookup"><span data-stu-id="2e042-107">Key</span></span>

<span data-ttu-id="2e042-108">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="2e042-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="2e042-109">`*`   opcional (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="2e042-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="2e042-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="2e042-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="2e042-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="2e042-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="2e042-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2e042-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="2e042-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2e042-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e042-114">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="2e042-114">Child Element</span></span></th>
<th><span data-ttu-id="2e042-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e042-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e042-116"><a href="element-1-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="2e042-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="2e042-117">Especifica se o perfil está habilitado administrativamente. Este é um novo elemento para v4.</span><span class="sxs-lookup"><span data-stu-id="2e042-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e042-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="2e042-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="2e042-119">Especifica se o perfil é controlado por roaming de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="2e042-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="2e042-120">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="2e042-120">This element is new for v4.</span></span> <span data-ttu-id="2e042-121">O valor desse elemento é um valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2e042-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="2e042-122">Este é um elemento opcional; Se nenhum valor for especificado, <strong>AllRoamAllowed</strong> será o padrão.</span><span class="sxs-lookup"><span data-stu-id="2e042-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e042-123"><a href="element-1-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="2e042-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="2e042-124">Uma ID de APN associada a este perfil. Esse elemento é novo na V4 e é opcional.</span><span class="sxs-lookup"><span data-stu-id="2e042-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e042-125"><a href="element-1-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="2e042-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="2e042-126">Especifica os parâmetros necessários para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="2e042-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e042-127"><a href="element-1-name.md">Nome</a></span><span class="sxs-lookup"><span data-stu-id="2e042-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="2e042-128">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="2e042-128">The name of the profile.</span></span> <span data-ttu-id="2e042-129">Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="2e042-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e042-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span><span class="sxs-lookup"><span data-stu-id="2e042-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="2e042-131">A ID de conexão do OEM para a configuração de DM do modem.</span><span class="sxs-lookup"><span data-stu-id="2e042-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e042-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (em ModemDMConfigProfile)</a></span><span class="sxs-lookup"><span data-stu-id="2e042-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="2e042-133">Especifica como este perfil DM de modem foi criado.</span><span class="sxs-lookup"><span data-stu-id="2e042-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="2e042-134">Esse valor é usado para decidir se um usuário pode excluir o perfil.</span><span class="sxs-lookup"><span data-stu-id="2e042-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="2e042-135">Os usuários só podem excluir perfis do <strong>Userprovisionados</strong> .</span><span class="sxs-lookup"><span data-stu-id="2e042-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e042-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="2e042-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="2e042-137">Especifica que esse perfil está ativo somente quando a condição de roaming atual é a especificada.</span><span class="sxs-lookup"><span data-stu-id="2e042-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="2e042-138">Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="2e042-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="2e042-139">O valor desse elemento deve ser um valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</span><span class="sxs-lookup"><span data-stu-id="2e042-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e042-140"><a href="element-1-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="2e042-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="2e042-141">O número de Identifcation do SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="2e042-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="2e042-142">Para obter mais detalhes, consulte a documentação do elemento v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2e042-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="2e042-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2e042-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="2e042-144">Esse elemento mais externo (documento) pode não estar contido em outros elementos.</span><span class="sxs-lookup"><span data-stu-id="2e042-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e042-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e042-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e042-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e042-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



