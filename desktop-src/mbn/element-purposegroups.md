---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3b158938e1a41f6ab8d3f1df0cae6a2166bc21c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630932"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups

Uma lista opcional de grupos de perfis, em que cada grupo inclui perfis usados para uma finalidade comum.

Esse elemento é novo para v4 do esquema.

Um perfil pode ser listado em vários grupos.

## <a name="element-hierarchy"></a>Hierarquia de elementos

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a>Sintaxe

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a>Chave

`{}`   intervalo específico de ocorrências

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento filho</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-purposegroupguid.md">PurposeGroupGuid</a></td>
<td><p>Representa um perfil em um PurposeGroup de perfis.</p>
<p>Os perfis são especificados por seu <a href="simpletype-guidtype.md"><strong>valor guidType.</strong></a></p>
<p>Quatro valores de GUID são definidos, conforme listado na tabela a seguir.</p>
<table>
<thead>
<tr class="header">
<th>Grupo de finalidades</th>
<th>GUID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Internet</td>
<td>3E5545D2-1137-4DC8-A198-33F1C657515F</td>
</tr>
<tr class="even">
<td>mms</td>
<td>53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</td>
</tr>
<tr class="odd">
<td>IMS</td>
<td>474D66ED-0E4B-476B-A455-19BB1239ED13</td>
</tr>
<tr class="even">
<td>SUPL</td>
<td>6D42669F-52A9-408E-9493-1071DCC437BD</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

<table>
<colgroup>
<col  />
<col  />
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
<td><p>O <strong>elemento MBNProfileExt</strong> é uma extensão do elemento MBNProfile anterior. Ele identifica um perfil de Banda Larga Móvel com um conjunto mais avançado de opções do que o elemento MBNProfile.</p>
<p>Pode haver mais de um elemento MbnProfileExt em um perfil, descrevendo as configurações de perfil para um conjunto específico de condições operacionais. Use o <a href="element-profileconditionedon.md"><strong>elemento filho ProfileConditionedOn</strong></a> <strong>de MBNProfileExt</strong> para especificar quais condições operacionais fazem de um perfil específico o perfil ativo.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



