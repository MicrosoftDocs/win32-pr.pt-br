---
description: MBNProfileExt \/ ... \/ UserLogonCred (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 12a65d91-1917-49d4-9b58-68c60464c857
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3f6999763e82051fa30af6109c3a04ae8dc65f77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813093"
---
# <a name="span-idwwan_profile_v4element_userlogoncredspanmbnprofileextuserlogoncred-v4"></a><span data-ttu-id="3d2b2-103"><span id="WWAN_profile_v4.element_UserLogonCred"></span>MBNProfileExt \/ ... \/ UserLogonCred (v4)</span><span class="sxs-lookup"><span data-stu-id="3d2b2-103"><span id="WWAN_profile_v4.element_UserLogonCred"></span>MBNProfileExt\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="3d2b2-104">Credenciais de logon para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3d2b2-105">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="3d2b2-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="3d2b2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d2b2-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="3d2b2-107">Chave</span><span class="sxs-lookup"><span data-stu-id="3d2b2-107">Key</span></span>

<span data-ttu-id="3d2b2-108">`?`   opcional (zero ou um)</span><span class="sxs-lookup"><span data-stu-id="3d2b2-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3d2b2-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="3d2b2-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3d2b2-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="3d2b2-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3d2b2-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3d2b2-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3d2b2-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d2b2-113">Elemento filho</span><span class="sxs-lookup"><span data-stu-id="3d2b2-113">Child Element</span></span></th>
<th><span data-ttu-id="3d2b2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d2b2-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d2b2-115"><a href="element-ignorepassword.md">IgnorePassword</a></span><span class="sxs-lookup"><span data-stu-id="3d2b2-115"><a href="element-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="3d2b2-116">Especifica como as senhas são tratadas durante a atualização de perfis.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="3d2b2-117">Se definido como <strong>true</strong> e um perfil com o mesmo nome existir no momento da operação de atualização, a senha desse perfil será executada e armazenada no novo perfil.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="3d2b2-118">Para obter mais detalhes, consulte a documentação do elemento v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3d2b2-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d2b2-119"><a href="element-password.md">Senha</a></span><span class="sxs-lookup"><span data-stu-id="3d2b2-119"><a href="element-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="3d2b2-120">Especifica a senha usada para autenticar um usuário.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="3d2b2-121">Para obter mais informações, consulte a documentação do elemento de <a href="../mbn/schema-password-userlogoncred-element.md"><strong>senha</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d2b2-122"><a href="element-username.md">UserName</a></span><span class="sxs-lookup"><span data-stu-id="3d2b2-122"><a href="element-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="3d2b2-123">O nome de usuário a ser usado para logon.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="3d2b2-124">Para obter mais detalhes, consulte a documentação do elemento de <a href="../mbn/schema-username-userlogoncred-element.md"><strong>nome de usuário</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3d2b2-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3d2b2-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d2b2-126">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="3d2b2-126">Parent Element</span></span></th>
<th><span data-ttu-id="3d2b2-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d2b2-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d2b2-128"><a href="element-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="3d2b2-128"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="3d2b2-129">Especifica os parâmetros necessários para estabelecer uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="3d2b2-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3d2b2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d2b2-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d2b2-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d2b2-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



