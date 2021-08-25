---
description: Especifica como IPropertyDescription::FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso será aplicável somente se <displayInfo displayType=&\#0034;DateTime&\#0034;> .
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950f10106d7850f4a5b58aeb165e8cb4cc9ffcd4
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629168"
---
# <a name="datetimeformat"></a>dateTimeFormat

Especifica como [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso será aplicável somente se <displayInfo displayType="DateTime"> . Deve haver apenas um [elemento dateTimeFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se houver vários elementos, o último será usado. Se nenhum [elemento dateTimeFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Sintaxe


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
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
<td>formatAs</td>
<td>Público. Opcional. O padrão é &quot; &quot; Geral. Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Geral</td>
<td>Padrão. Formata o valor de data/hora <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>usando SHFormatDateTime.</strong></a> Use os <em>atributos formatTimeAs</em> e <em>formatDateAs</em> para especificar como a hora e a data são formatadas. Requer que o tipo de propriedade seja DateTime.</td>
</tr>
<tr class="even">
<td>Mês</td>
<td>Formatar o valor como um dos meses do ano. Requer que o tipo de propriedade seja Int32. O valor deve ser armazenado como um valor numérico com 1 que representa o primeiro mês do ano.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Formatar o valor como &quot; Ano – &quot; Mês. Requer que o tipo de propriedade seja Int32. O valor deve ser armazenado de forma que os dois bytes mais altos especifiquem o ano e os dois bytes inferiores especificam o mês.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>Formatar o valor como uma cadeia de caracteres simples.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>Público. Opcional. O padrão é &quot; &quot; ShortTime. Especifica o formato no qual a hora de exibição será exibida. Aplica-se <strong>quando formatAs= &quot; Geral. &quot; </strong> Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortTime</td>
<td>Padrão. Mostre a hora como &quot; 19h48. &quot;</td>
</tr>
<tr class="even">
<td>Longa data</td>
<td>Mostre a hora como &quot; 19:48:33 &quot; .</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>Não exibe a parte de hora da data.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Público. Opcional. O padrão é &quot; &quot; ShortDate. Especifica o formato no qual exibir a data. Aplica-se <strong>quando formatAs= &quot; Geral. &quot; </strong> Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortDate</td>
<td>Padrão. Mostrar a data como &quot; 13/5/59 &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Mostre a data como &quot; Quarta-feira, 13 de maio de 1959. &quot;</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>Não exibir a parte de data.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Mostre a data como &quot; ShortDate &quot; , mas use descrições relativas, como &quot; &quot; ontem, sempre que possível.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Mostre a data como &quot; LongDate &quot; , mas use descrições relativas, como &quot; &quot; ontem, sempre que possível.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
