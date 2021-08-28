---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9db77cc68dab7038a1b5b9c50d49f5381ee948
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883659"
---
# <a name="numberformat"></a>numberFormat

Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType="Number"> . Deve haver apenas um elemento [NumberFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [NumberFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Syntax


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
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
<td>formato de</td>
<td>Público. Opcional. O padrão é &quot; geral &quot; . Especifica o formato de exibição. Os seguintes valores são válidos: 
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
<td>Padrão. Exibe o valor como um número não formatado.</td>
</tr>
<tr class="even">
<td>Porcentagem</td>
<td>Formata o valor como uma porcentagem. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="odd">
<td>ByteS</td>
<td>Formata o valor como um byte, &quot; KB &quot; , &quot; MB &quot; ou &quot; GB, &quot; conforme apropriado. Requer que a propriedade seja UInt64.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Formata o valor como um &quot; KB &quot; , não importa qual é o valor. Requer que a propriedade seja UInt64.</td>
</tr>
<tr class="odd">
<td>Amostras</td>
<td>Formata o valor como um número de bits. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="even">
<td>Taxa de bits</td>
<td>Formata o valor em &quot; kbps &quot; . Requer que a propriedade seja UInt32. O valor deve ser armazenado em &quot; unidades de bits por segundo &quot; .</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>Formata o valor em &quot; kHz &quot; . Requer que a propriedade seja UInt32. O valor deve ser armazenado em &quot; &quot; unidades hertz.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Formata o valor em quadros/segundo. Requer que a propriedade seja UInt32. O valor deve ser armazenado em &quot; unidades de quilobytes de quadros por segundo &quot; .</td>
</tr>
<tr class="odd">
<td>Pixels</td>
<td>Formata o valor em unidades de pixel. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="even">
<td>EXIBI</td>
<td>Formata o valor em pontos por polegada. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="odd">
<td>Duração</td>
<td>Formata o valor como uma duração. Use &lt; formatDurationAs &gt; para especificar o formato de duração. Requer que a propriedade seja UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Público. Opcional. O padrão é &quot; hh: mm: SS &quot; . Aplica-se somente se <em>formatas = &quot; duração &quot; </em>. Requer que a propriedade seja UInt64. Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hh:mm</td>
<td>Formata o valor em horas e minutos.</td>
</tr>
<tr class="even">
<td>hh:mm:ss</td>
<td>Padrão. Formata o valor em horas, minutos e segundos.</td>
</tr>
<tr class="odd">
<td>hh: mm: SS. FFF</td>
<td>Formata o valor em horas, minutos, segundos e milissegundos.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
