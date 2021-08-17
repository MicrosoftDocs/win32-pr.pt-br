---
description: Não há suporte no Windows 7 e posteriores. Especifica qual controle usar no construtor de consultas.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f05800fc026c61a4ea50098fb1d8f4deb98d971c9eecfed478d71bd3c01033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823556"
---
# <a name="querycontrol"></a>queryControl

Não há suporte no Windows 7 e posteriores. Especifica qual controle usar no construtor de consultas. Deve haver apenas um [elemento queryControl]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se houver vários elementos, o último será usado. Se nenhum [elemento queryControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Syntax


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
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
<col style="width: 50%" />
<col style="width: 50%" />
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
<col style="width: 50%" />
<col style="width: 50%" />
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
<th>Conditiontype</th>
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
<td>Número ou tamanho</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Número ou Tamanho (enum)</td>
<td>Lista</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Calendário</td>
</tr>
<tr class="even">
<td>Booliano</td>
<td>Booliano</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Usa o controle booliana.</td>
</tr>
<tr class="odd">
<td>Calendário</td>
<td>Usa o controle de calendário suspenso.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Usa o controle de lista com caixas de seleção.</td>
</tr>
<tr class="odd">
<td>DropList</td>
<td>Usa o controle de lista suspenso.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa o controle de edição de texto de vários valores.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Usa o controle de edição de texto numérico.</td>
</tr>
<tr class="even">
<td>Classificação</td>
<td>Usa o controle de classificação de 5 estrelas.</td>
</tr>
<tr class="odd">
<td>Texto</td>
<td>Usa o controle de edição de texto.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
