---
description: ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IgnorePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3712bc93fe273732bf113be213b0d962adb9b35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164441"
---
# <a name="span-idwwan_profile_v4element_1_ignorepasswordspanmodemdmconfigprofileignorepassword-v4"></a><span data-ttu-id="5b38f-103"><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)</span><span class="sxs-lookup"><span data-stu-id="5b38f-103"><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile\/...\/IgnorePassword (v4)</span></span>

<span data-ttu-id="5b38f-104">Especifica como as senhas são tratadas durante a atualização de perfis.</span><span class="sxs-lookup"><span data-stu-id="5b38f-104">Specifies how passwords are handled when upgrading profiles.</span></span>

<span data-ttu-id="5b38f-105">Se definido como **true** e um perfil com o mesmo nome existir no momento da operação de atualização, a senha desse perfil será executada e armazenada no novo perfil.</span><span class="sxs-lookup"><span data-stu-id="5b38f-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span>

<span data-ttu-id="5b38f-106">Para obter mais detalhes, consulte a documentação do elemento v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5b38f-106">For more details, see the documentation for the v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="5b38f-107">Hierarquia de elementos</span><span class="sxs-lookup"><span data-stu-id="5b38f-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a><span data-ttu-id="5b38f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b38f-108">Syntax</span></span>

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="5b38f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos</span><span class="sxs-lookup"><span data-stu-id="5b38f-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="5b38f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="5b38f-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="5b38f-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5b38f-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="5b38f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5b38f-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="5b38f-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5b38f-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="5b38f-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5b38f-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b38f-115">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5b38f-115">Parent Element</span></span></th>
<th><span data-ttu-id="5b38f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b38f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b38f-117"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="5b38f-117"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="5b38f-118">Credenciais de logon para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5b38f-118">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="5b38f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b38f-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b38f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b38f-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
