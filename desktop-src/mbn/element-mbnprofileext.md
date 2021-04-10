---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296405"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="bc20d-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span><span class="sxs-lookup"><span data-stu-id="bc20d-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="bc20d-104">O elemento **MBNProfileExt** é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="bc20d-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="bc20d-105">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="bc20d-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="bc20d-106">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="bc20d-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="bc20d-107">Use o elemento filho [**ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="bc20d-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="bc20d-108">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="bc20d-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="bc20d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc20d-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="bc20d-110">Chave</span><span class="sxs-lookup"><span data-stu-id="bc20d-110">Key</span></span>

<span data-ttu-id="bc20d-111">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="bc20d-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="bc20d-112">`*`   opcional (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="bc20d-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="bc20d-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="bc20d-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="bc20d-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="bc20d-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="bc20d-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="bc20d-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="bc20d-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bc20d-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc20d-117">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="bc20d-117">Child Element</span></span></th>
<th><span data-ttu-id="bc20d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc20d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc20d-119"><a href="element-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="bc20d-120">Especifica se o perfil está habilitado administrativamente. Este é um novo elemento para v4.</span><span class="sxs-lookup"><span data-stu-id="bc20d-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="bc20d-122">Especifica se o perfil é controlado por roaming de forma administrativa.</span><span class="sxs-lookup"><span data-stu-id="bc20d-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="bc20d-123">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="bc20d-123">This element is new for v4.</span></span> <span data-ttu-id="bc20d-124">O valor desse elemento é um valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="bc20d-125">Este é um elemento opcional; Se nenhum valor for especificado, <strong>AllRoamAllowed</strong> será o padrão.</span><span class="sxs-lookup"><span data-stu-id="bc20d-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-126"><a href="element-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="bc20d-127">Uma ID de APN associada a este perfil. Esse elemento é novo na V4 e é opcional.</span><span class="sxs-lookup"><span data-stu-id="bc20d-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="bc20d-129">Especifica se o dispositivo de banda larga móvel se conectará automaticamente a uma rede.</span><span class="sxs-lookup"><span data-stu-id="bc20d-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="bc20d-130">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="bc20d-132">Especifica a configuração de conexão automática a ser usada para um dispositivo de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="bc20d-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="bc20d-133">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-134"><a href="element-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="bc20d-135">Especifica os parâmetros necessários para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="bc20d-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="bc20d-137">Especifica uma lista de provedores de rede preferenciais durante o roaming.</span><span class="sxs-lookup"><span data-stu-id="bc20d-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="bc20d-138">Para obter detalhes, consulte a documentação do elemento v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-139"><a href="element-description.md">Descrição</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="bc20d-140">Uma descrição do perfil.</span><span class="sxs-lookup"><span data-stu-id="bc20d-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="bc20d-142">O nome do provedor de início para o cartão SIM/dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="bc20d-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="bc20d-143">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-144"><a href="element-iconfilepath.md">ICONFilePath</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="bc20d-145">O caminho para o arquivo de ícone da conexão.</span><span class="sxs-lookup"><span data-stu-id="bc20d-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="bc20d-146">A interface do usuário conexão do sistema operacional exibe o ícone quando uma conexão é feita usando esse perfil.</span><span class="sxs-lookup"><span data-stu-id="bc20d-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="bc20d-147">Para obter mais detalhes sobre como usar esse elemento, consulte a documentação v1 para <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bc20d-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="bc20d-149">Especifica se esse perfil é o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="bc20d-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="bc20d-150">Para obter mais detalhes sobre esse elemento, consulte a documentação v1 para <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bc20d-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="bc20d-152">Especifica que este perfil é exclusivo para outros perfis do mesmo (s) conjunto (es) de perfis. Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="bc20d-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="bc20d-154">Especifica que esse perfil é um perfil de contexto PDP adicional muito duradouro. Se o valor desse elemento for <strong>true</strong>, <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> também deverá ser definido como <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc20d-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="bc20d-155">Este é um novo elemento para v4.</span><span class="sxs-lookup"><span data-stu-id="bc20d-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="bc20d-157">Especifica que este perfil deve ser usado somente para provisionamento. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="bc20d-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="bc20d-158">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="bc20d-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="bc20d-159">Se <strong>IsProvisioningProfile</strong> for true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> deverá ser false e <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> deverá ser manual.</span><span class="sxs-lookup"><span data-stu-id="bc20d-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="bc20d-161">Informações de configuração para MMS (serviço de mensagens de multimídia).</span><span class="sxs-lookup"><span data-stu-id="bc20d-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="bc20d-162">Além de definir os elementos de configuração dentro deste elemento, um perfil MMS deve ter as seguintes configurações.</span><span class="sxs-lookup"><span data-stu-id="bc20d-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="bc20d-163">Seu elemento <a href="element-name.md"><strong>Name</strong></a> deve conter um nome exclusivo em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="bc20d-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="bc20d-164">Seu <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve ser definido como <strong>userprovisionado</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc20d-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="bc20d-165">Seu <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve conter o ICCID do sim para o qual esse perfil se destina.</span><span class="sxs-lookup"><span data-stu-id="bc20d-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="bc20d-166">Seu <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve ser definido como <strong>manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc20d-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="bc20d-167">Seu <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve conter o GUID para o grupo de finalidade de MMS.</span><span class="sxs-lookup"><span data-stu-id="bc20d-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="bc20d-168">Seu <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve ser definido como <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc20d-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-169"><a href="element-name.md">Nome</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="bc20d-170">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="bc20d-170">The name of the profile.</span></span> <span data-ttu-id="bc20d-171">Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="bc20d-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="bc20d-173">Especifica as condições que devem ser satisfeitas para que um perfil seja aplicável.</span><span class="sxs-lookup"><span data-stu-id="bc20d-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="bc20d-174">Este elemento é novo para v4.</span><span class="sxs-lookup"><span data-stu-id="bc20d-174">This element is new for v4.</span></span> <span data-ttu-id="bc20d-175">Ele permite que você especifique vários perfis que se aplicam em diferentes condições e para que o perfil apropriado seja usado automaticamente quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="bc20d-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="bc20d-176">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="bc20d-176">This element is optional.</span></span> <span data-ttu-id="bc20d-177">Se você não especificá-lo, o perfil sempre será aplicável em relação às condições listadas.</span><span class="sxs-lookup"><span data-stu-id="bc20d-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-178"><a href="element-profilecreationtype.md">ProfileCreationType (em MBNProfileExt)</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="bc20d-179">Especifica o criador do perfil.</span><span class="sxs-lookup"><span data-stu-id="bc20d-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="bc20d-180">Para obter mais informações sobre esse elemento, consulte a documentação do elemento v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-181"><a href="element-purposegroups.md">PurposeGroups</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="bc20d-182">Uma lista opcional de grupos de perfis, onde cada grupo inclui perfis usados para uma finalidade comum.</span><span class="sxs-lookup"><span data-stu-id="bc20d-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="bc20d-183">Este elemento é novo para v4 do esquema.</span><span class="sxs-lookup"><span data-stu-id="bc20d-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="bc20d-184">Um perfil pode ser listado em vários grupos.</span><span class="sxs-lookup"><span data-stu-id="bc20d-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc20d-185"><a href="element-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="bc20d-186">O número de Identifcation do SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="bc20d-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="bc20d-187">Para obter mais detalhes, consulte a documentação do elemento v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bc20d-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc20d-188"><a href="element-subscriberid.md">Subscriberid</a></span><span class="sxs-lookup"><span data-stu-id="bc20d-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="bc20d-189">Identifica o identificador exclusivo do perfil.</span><span class="sxs-lookup"><span data-stu-id="bc20d-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="bc20d-190">Para uma rede GSM, isso deve conter a IMSI (identidade do assinante internacional móvel) do SIM e para dispositivos CDMA que ele deve conter o mínimo (número de identificação móvel) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc20d-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="bc20d-191">Para obter mais informações, consulte a documentação para o elemento <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>subscriberid</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="bc20d-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="bc20d-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bc20d-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="bc20d-193">Esse elemento mais externo (documento) pode não estar contido em outros elementos.</span><span class="sxs-lookup"><span data-stu-id="bc20d-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc20d-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc20d-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc20d-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc20d-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
