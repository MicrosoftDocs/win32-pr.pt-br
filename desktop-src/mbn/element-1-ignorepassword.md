---
description: ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IgnorePassword (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0286fcc7a025bc565916e68b817c6a79f378f26d
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388787"
---
# <a name="span-idwwan_profile_v4element_1_ignorepasswordspanmodemdmconfigprofileignorepassword-v4"></a><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)

Especifica como as senhas são tratadas durante a atualização de perfis.

Se definido como **true** e um perfil com o mesmo nome existir no momento da operação de atualização, a senha desse perfil será executada e armazenada no novo perfil.

Para obter mais detalhes, consulte a documentação do elemento v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) .

## <a name="element-hierarchy"></a>Hierarquia de elementos

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a>Sintaxe

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento pai</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-1-userlogoncred.md">UserLogonCred</a></td>
<td><p>Credenciais de logon para uma conexão.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
