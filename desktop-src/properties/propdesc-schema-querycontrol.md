---
description: sem suporte no Windows 7 e posterior. Especifica o controle a ser usado no construtor de consultas.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3652a46d403bc258226de5a48f34ae16960ff517
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626312"
---
# <a name="querycontrol"></a>queryControl

sem suporte no Windows 7 e posterior. Especifica o controle a ser usado no construtor de consultas. Deve haver apenas um elemento [queryControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [queryControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Sintaxe


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
<td>Público. Opcional. O padrão é &quot; Default &quot; . Os seguintes valores são válidos: 
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
<td>Padrão. Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo. Os tipos padrão são listados abaixo. Qualquer outro tipo resulta no uso do &quot; controle de texto &quot; . 
<table>
<thead>
<tr class="header">
<th>ConditionType</th>
<th>Control</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Texto</td>
</tr>
<tr class="even">
<td>Cadeia de caracteres (valores múltiplos)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>Número ou tamanho</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Número ou tamanho (enum)</td>
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
<td>Usa o controle booliano.</td>
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
<td>Lista suspensa</td>
<td>Usa o controle lista suspensa.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa o controle de edição de texto de valores múltiplos.</td>
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



 

 

 
