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
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span id="WWAN_profile_v4.element_Context"></span>\/Contexto de MBNProfileExt (v4)

Especifica os parâmetros necessários para estabelecer uma conexão de dados.

## <a name="element-hierarchy"></a>Hierarquia de elementos

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Sintaxe

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

### <a name="key"></a>Chave

`?`   opcional (zero ou um)

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
<td><a href="element-accessstring.md">AccessString</a></td>
<td><p>Identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.</p>
<p>Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>accessstring</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-authprotocol.md">AuthProtocol</a></td>
<td><p>>Especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</p>
<p>Observe que no v4, um novo valor de enumeração está disponível para esse elemento. <strong>Seleção</strong> configurada significa que um protocolo de autenticação deve ser escolhido por camadas inferiores.</p>
<p>Para obter mais informações, consulte a documentação do elemento v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-compression.md">Compactação</a></td>
<td><p>Especifica se a compactação será usada no link de dados para a transferência de dados e de cabeçalho.</p>
<p>Para obter mais informações, consulte a documentação do elemento de <a href="../mbn/schema-compression-contexttype-element.md"><strong>compactação</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-iptype.md">IPType</a></td>
<td><p>Especifica o tipo de IP a ser usado nessa conexão de dados.</p>
<p>Esse elemento é novo no v4 do esquema. O elemento pode ter um dos valores a seguir.</p>
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Padrão</td>
<td>O tipo de IP deve ser escolhido por camadas inferiores</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>Usar IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>Use IPv6</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Use IPv4 e/ou IPv6, como disponível.</td>
</tr>
<tr class="odd">
<td>XLAT</td>
<td>Usar o 464XLAT para encapsular IPv4 em redes IPv6</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-userlogoncred.md">UserLogonCred</a></td>
<td><p>Credenciais de logon para uma conexão.</p></td>
</tr>
</tbody>
</table>

 

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
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>O elemento <strong>MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de banda larga móvel com um conjunto mais rico de opções do que o elemento MBNProfile.</p>
<p>Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um determinado conjunto de condições operacionais. Use o elemento filho <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar quais condições operacionais tornam um perfil específico o perfil ativo.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Perfil de configuração de DM de modem.</p></td>
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

 

 



