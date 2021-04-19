---
description: '\/Contexto de ModemDMConfigProfile (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contexto (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388846"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="9de55-103"><span id="WWAN_profile_v4.element_1_Context"></span>\/Contexto de ModemDMConfigProfile (v4)</span><span class="sxs-lookup"><span data-stu-id="9de55-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="9de55-104">Especifica os parâmetros necessários para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="9de55-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="9de55-105">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="9de55-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="9de55-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9de55-106">Syntax</span></span>

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

### <a name="key"></a><span data-ttu-id="9de55-107">Chave</span><span class="sxs-lookup"><span data-stu-id="9de55-107">Key</span></span>

<span data-ttu-id="9de55-108">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="9de55-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="9de55-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="9de55-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="9de55-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="9de55-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="9de55-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9de55-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="9de55-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9de55-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9de55-113">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="9de55-113">Child Element</span></span></th>
<th><span data-ttu-id="9de55-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9de55-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9de55-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="9de55-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="9de55-116">Identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="9de55-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="9de55-117">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>accessstring</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9de55-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9de55-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="9de55-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="9de55-119">>Especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="9de55-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="9de55-120">Observe que no v4, um novo valor de enumeração está disponível para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="9de55-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="9de55-121"><strong>Seleção</strong> configurada significa que um protocolo de autenticação deve ser escolhido por camadas inferiores.</span><span class="sxs-lookup"><span data-stu-id="9de55-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="9de55-122">Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9de55-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9de55-123"><a href="element-1-compression.md">Compactação</a></span><span class="sxs-lookup"><span data-stu-id="9de55-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="9de55-124">Especifica se a compactação será usada no link de dados para a transferência de dados e de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9de55-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="9de55-125">Para obter mais informações, consulte a documentação do elemento de <a href="../mbn/schema-compression-contexttype-element.md"><strong>compactação</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="9de55-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9de55-126"><a href="element-1-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="9de55-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="9de55-127">Especifica o tipo de IP a ser usado nessa conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="9de55-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="9de55-128">Esse elemento é novo no v4 do esquema.</span><span class="sxs-lookup"><span data-stu-id="9de55-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="9de55-129">O elemento pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9de55-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9de55-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9de55-130">Value</span></span></th>
<th><span data-ttu-id="9de55-131">Significado</span><span class="sxs-lookup"><span data-stu-id="9de55-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9de55-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="9de55-132">Default</span></span></td>
<td><span data-ttu-id="9de55-133">O tipo de IP deve ser escolhido por camadas inferiores</span><span class="sxs-lookup"><span data-stu-id="9de55-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9de55-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="9de55-134">IPv4</span></span></td>
<td><span data-ttu-id="9de55-135">Usar IPv4</span><span class="sxs-lookup"><span data-stu-id="9de55-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9de55-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="9de55-136">IPv6</span></span></td>
<td><span data-ttu-id="9de55-137">Use IPv6</span><span class="sxs-lookup"><span data-stu-id="9de55-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9de55-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="9de55-138">IPv4v6</span></span></td>
<td><span data-ttu-id="9de55-139">Use IPv4 e/ou IPv6, como disponível.</span><span class="sxs-lookup"><span data-stu-id="9de55-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9de55-140">XLAT</span><span class="sxs-lookup"><span data-stu-id="9de55-140">XLAT</span></span></td>
<td><span data-ttu-id="9de55-141">Usar o 464XLAT para encapsular IPv4 em redes IPv6</span><span class="sxs-lookup"><span data-stu-id="9de55-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9de55-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="9de55-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="9de55-143">Credenciais de logon para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="9de55-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="9de55-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9de55-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9de55-145">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="9de55-145">Parent Element</span></span></th>
<th><span data-ttu-id="9de55-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="9de55-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9de55-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="9de55-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="9de55-148">O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="9de55-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="9de55-149">Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="9de55-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="9de55-150">Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais.</span><span class="sxs-lookup"><span data-stu-id="9de55-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="9de55-151">Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="9de55-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9de55-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="9de55-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="9de55-153">Perfil de configuração de DM de modem.</span><span class="sxs-lookup"><span data-stu-id="9de55-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="9de55-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9de55-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9de55-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="9de55-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



