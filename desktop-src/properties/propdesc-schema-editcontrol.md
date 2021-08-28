---
description: Especifica qual controle usar ao editar a propriedade.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213d6fba3f03f90e0d5a2702226dd8596462b289
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626802"
---
# <a name="editcontrol"></a>editControl

Especifica qual controle usar ao editar a propriedade. Deve haver apenas um [elemento editControl]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se houver vários elementos, o último será usado. Se nenhum [elemento editControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

Se <typeInfo isInnate="true"> , esse elemento será ignorado porque uma propriedade inata não pode ser editada.

## <a name="syntax"></a>Sintaxe


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                   | Elementos filho |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Nenhum           |



 

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>controle</td>
<td>Público. Opcional. O padrão é &quot; &quot; Padrão. Os seguintes valores são válidos: 
<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Padrão</td>
<td>Padrão. Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo . Os tipos padrão são listados abaixo. Qualquer outro tipo resulta no uso do &quot; controle &quot; Texto. 
<table>
<thead>
<tr class="header">
<th>Type</th>
<th>Control</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Texto</td>
</tr>
<tr class="even">
<td>Cadeia de caracteres (vários valores)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Calendário</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Calendário</td>
<td>Usa o controle de calendário.</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>Usa o controle de lista com caixas de seleção.</td>
</tr>
<tr class="even">
<td>DropList</td>
<td>Usa o controle de lista suspenso.</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>Usa o controle de edição de texto de várias linhas.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa o controle de edição de texto de vários valores.</td>
</tr>
<tr class="odd">
<td>Classificação</td>
<td>Usa o controle de classificação de 5 estrelas.</td>
</tr>
<tr class="even">
<td>Texto</td>
<td>Usa o controle de edição de texto.</td>
</tr>
<tr class="odd">
<td>IconList</td>
<td><strong>Windows 7 e posterior.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
