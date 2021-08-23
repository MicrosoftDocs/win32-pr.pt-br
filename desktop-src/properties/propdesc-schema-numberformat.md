---
description: Especifica como IPropertyDescription::FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso será aplicável somente se <displayInfo displayType=&\#0034;Number&\#0034;> .
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: Numberformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1ad529b6f23191f4cfb703862a70164c4ce32d1bbb9c039fdc881e2f19cdc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718225"
---
# <a name="numberformat"></a>Numberformat

Especifica como [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso será aplicável somente se <displayInfo displayType="Number"> . Deve haver apenas um [elemento numberFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se houver vários elementos, o último será usado. Se nenhum [elemento numberFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

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
<td>formatAs</td>
<td>Público. Opcional. O padrão é &quot; &quot; Geral. Especifica o formato de exibição. Os seguintes valores são válidos: 
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
<td>Formatar o valor como um percentual. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>Formata o valor como um byte, &quot; &quot; KB, MB ou &quot; &quot; &quot; &quot; GB, conforme apropriado. Requer que a propriedade seja UInt64.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Formatar o valor como &quot; um &quot; KB, independentemente do valor. Requer que a propriedade seja UInt64.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Formatar o valor como um número de bits. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="even">
<td>Taxa de bits</td>
<td>Formatar o valor em &quot; &quot; Kbps. Requer que a propriedade seja UInt32. O valor deve ser armazenado em &quot; unidades bits por &quot; segundo.</td>
</tr>
<tr class="odd">
<td>Taxa de amostragem</td>
<td>Formatar o valor em &quot; &quot; KHz. Requer que a propriedade seja UInt32. O valor deve ser armazenado em unidades &quot; &quot; hertz.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Formatar o valor em quadros/segundo. Requer que a propriedade seja UInt32. O valor deve ser armazenado em unidades de quilo &quot; quadros por &quot; segundo.</td>
</tr>
<tr class="odd">
<td>Pixels</td>
<td>Formatar o valor em unidades de pixel. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="even">
<td>Dpi</td>
<td>Formatar o valor em pontos por polegada. Requer que a propriedade seja UInt32.</td>
</tr>
<tr class="odd">
<td>Duração</td>
<td>Formatar o valor como uma duração. Use <formatDurationAs> para especificar o formato de duração. Requer que a propriedade seja UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Público. Opcional. O padrão &quot; é hh:mm:ss. &quot; Aplica-se somente se <em>formatAs= &quot; Duration &quot; </em>. Requer que a propriedade seja UInt64. Os seguintes valores são válidos: 
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
<td>hh:mm:ss.fff</td>
<td>Formata o valor em horas, minutos, segundos e milissegundos.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
