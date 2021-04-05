---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165276"
---
# <a name="datetimeformat"></a>dateTimeFormat

Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType="DateTime"> . Deve haver apenas um elemento [DateTimeFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [DateTimeFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Syntax


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
<td>formato de</td>
<td>Público. Opcional. O padrão é &quot; geral &quot; . Os seguintes valores são válidos: 
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
<td>Padrão. Formata o valor de data e hora usando <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>. Use os atributos <em>formatTimeAs</em> e <em>formatDateAs</em> para especificar como a hora e a data são formatadas. Requer que o tipo de propriedade seja DateTime.</td>
</tr>
<tr class="even">
<td>Mês</td>
<td>Formata o valor como um dos meses do ano. Requer que o tipo de propriedade seja Int32. O valor deve ser armazenado como um valor numérico com 1 representando o primeiro mês do ano.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Formata o valor como &quot; ano-mês &quot; . Requer que o tipo de propriedade seja Int32. O valor deve ser armazenado de modo que os dois bytes mais altos especifiquem o ano e os dois bytes inferiores especifiquem o mês.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>Formata o valor como uma cadeia de caracteres simples.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>Público. Opcional. O padrão é &quot; curtotime &quot; . Especifica o formato no qual exibir a hora. Aplica-se quando <strong>formatas = &quot; geral &quot; </strong>. Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Curtotime</td>
<td>Padrão. Mostre o tempo como &quot; 7:48 PM &quot; .</td>
</tr>
<tr class="even">
<td>Desenvolvedor</td>
<td>Mostre o tempo como &quot; 7:48:33 PM &quot; .</td>
</tr>
<tr class="odd">
<td>Ocultartime</td>
<td>Não exibir a parte de hora da data.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Público. Opcional. O padrão é &quot; ShortDate &quot; . Especifica o formato no qual exibir a data. Aplica-se quando <strong>formatas = &quot; geral &quot; </strong>. Os seguintes valores são válidos: 
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
<td>Padrão. Mostre a data como &quot; 5/13/59 &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Mostre a data como &quot; quarta-feira, 13 de maio de 1959 &quot; .</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>Não exibir a parte de data.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Mostre a data como &quot; ShortDate &quot; , mas use descrições relativas, como &quot; ontem &quot; , sempre que possível.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Mostre a data como &quot; LongDate &quot; , mas use descrições relativas, como &quot; ontem &quot; , sempre que possível.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
