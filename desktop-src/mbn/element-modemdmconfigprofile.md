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
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Perfil de configuração de DM de modem.

## <a name="element-hierarchy"></a>Hierarquia de elementos

**<ModemDMConfigProfile>**

## <a name="syntax"></a>Syntax

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

### <a name="key"></a>Chave

`?`   opcional (zero ou um)

`*`   opcional (zero ou mais)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento filho</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-1-adminenable.md">AdminEnable</a></td>
<td><p>Especifica se o perfil está habilitado administrativamente. Este é um novo elemento para v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Especifica se o perfil é controlado por roaming de forma administrativa. Este elemento é novo para v4. O valor desse elemento é um valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Este é um elemento opcional; Se nenhum valor for especificado, <strong>AllRoamAllowed</strong> será o padrão.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">ApnID</a></td>
<td><p>Uma ID de APN associada a este perfil. Esse elemento é novo na V4 e é opcional.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Contexto</a></td>
<td><p>Especifica os parâmetros necessários para estabelecer uma conexão de dados.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Nome</a></td>
<td><p>O nome do perfil. Para obter mais informações, consulte a documentação do elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">OemConnectionId</a></td>
<td><p>A ID de conexão do OEM para a configuração de DM do modem.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">ProfileCreationType (em ModemDMConfigProfile)</a></td>
<td><p>Especifica como este perfil DM de modem foi criado.</p>
<p>Esse valor é usado para decidir se um usuário pode excluir o perfil. Os usuários só podem excluir perfis do <strong>Userprovisionados</strong> .</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">RoamApplicability</a></td>
<td><p>Especifica que esse perfil está ativo somente quando a condição de roaming atual é a especificada. Caso contrário, o perfil não será aplicável e não poderá ser usado para ativar um contexto de protocolo de dados de pacote (PDP). O valor desse elemento deve ser um valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">SimIccID</a></td>
<td><p>O número de Identifcation do SIM para dispositivos GSM. Para obter mais detalhes, consulte a documentação do elemento v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> .</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

Esse elemento mais externo (documento) pode não estar contido em outros elementos.

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

 

 



