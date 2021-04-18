---
description: '\/Contexto de MBNProfileExt (v4)'
MS-HAID: WWAN\_profile\_v4.element\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contexto
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eff61884-1d37-4e1a-85f0-2fadf14227ac
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8ec231b5d7e2769d86262864e0b9a53621c36a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785954"
---
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span data-ttu-id="e8daa-103"><span id="WWAN_profile_v4.element_Context"></span>\/Contexto de MBNProfileExt (v4)</span><span class="sxs-lookup"><span data-stu-id="e8daa-103"><span id="WWAN_profile_v4.element_Context"></span>MBNProfileExt\/Context (v4)</span></span>

<span data-ttu-id="e8daa-104">Especifica os parâmetros necessários para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="e8daa-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e8daa-105">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="e8daa-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="e8daa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8daa-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="e8daa-107">Chave</span><span class="sxs-lookup"><span data-stu-id="e8daa-107">Key</span></span>

<span data-ttu-id="e8daa-108">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="e8daa-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e8daa-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="e8daa-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e8daa-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="e8daa-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e8daa-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e8daa-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e8daa-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e8daa-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8daa-113">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="e8daa-113">Child Element</span></span></th>
<th><span data-ttu-id="e8daa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8daa-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8daa-115"><a href="element-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-115"><a href="element-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="e8daa-116">Identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="e8daa-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="e8daa-117">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>accessstring</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e8daa-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8daa-118"><a href="element-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-118"><a href="element-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="e8daa-119">>Especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="e8daa-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="e8daa-120">Observe que no v4, um novo valor de enumeração está disponível para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="e8daa-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="e8daa-121"><strong>Seleção</strong> configurada significa que um protocolo de autenticação deve ser escolhido por camadas inferiores.</span><span class="sxs-lookup"><span data-stu-id="e8daa-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="e8daa-122">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e8daa-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8daa-123"><a href="element-compression.md">Compactação</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-123"><a href="element-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="e8daa-124">Especifica se a compactação será usada no link de dados para a transferência de dados e de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="e8daa-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="e8daa-125">Para obter mais informações, consulte a documentação do elemento de <a href="../mbn/schema-compression-contexttype-element.md"><strong>compactação</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="e8daa-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8daa-126"><a href="element-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-126"><a href="element-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="e8daa-127">Especifica o tipo de IP a ser usado nessa conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="e8daa-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="e8daa-128">Esse elemento é novo no v4 do esquema.</span><span class="sxs-lookup"><span data-stu-id="e8daa-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="e8daa-129">O elemento pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8daa-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e8daa-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e8daa-130">Value</span></span></th>
<th><span data-ttu-id="e8daa-131">Significado</span><span class="sxs-lookup"><span data-stu-id="e8daa-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8daa-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="e8daa-132">Default</span></span></td>
<td><span data-ttu-id="e8daa-133">O tipo de IP deve ser escolhido por camadas inferiores</span><span class="sxs-lookup"><span data-stu-id="e8daa-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8daa-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="e8daa-134">IPv4</span></span></td>
<td><span data-ttu-id="e8daa-135">Usar IPv4</span><span class="sxs-lookup"><span data-stu-id="e8daa-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8daa-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="e8daa-136">IPv6</span></span></td>
<td><span data-ttu-id="e8daa-137">Use IPv6</span><span class="sxs-lookup"><span data-stu-id="e8daa-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8daa-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="e8daa-138">IPv4v6</span></span></td>
<td><span data-ttu-id="e8daa-139">Use IPv4 e/ou IPv6, como disponível.</span><span class="sxs-lookup"><span data-stu-id="e8daa-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8daa-140">XLAT</span><span class="sxs-lookup"><span data-stu-id="e8daa-140">XLAT</span></span></td>
<td><span data-ttu-id="e8daa-141">Usar o 464XLAT para encapsular IPv4 em redes IPv6</span><span class="sxs-lookup"><span data-stu-id="e8daa-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8daa-142"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-142"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="e8daa-143">Credenciais de logon para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="e8daa-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e8daa-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e8daa-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8daa-145">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e8daa-145">Parent Element</span></span></th>
<th><span data-ttu-id="e8daa-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8daa-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8daa-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="e8daa-148">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="e8daa-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="e8daa-149">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="e8daa-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="e8daa-150">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="e8daa-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="e8daa-151">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="e8daa-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8daa-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="e8daa-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="e8daa-153">Perfil de configuração de DM de modem.</span><span class="sxs-lookup"><span data-stu-id="e8daa-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e8daa-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8daa-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8daa-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8daa-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



