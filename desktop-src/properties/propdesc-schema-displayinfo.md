---
description: Especifica as informações de exibição de uma propriedade.
ms.assetid: 27c03ced-a5fa-4ab4-b88e-5b78701da878
title: displayInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0bbc3cf0f17d24672e30a110d95341c1cb902d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622082"
---
# <a name="displayinfo"></a>displayInfo

Especifica as informações de exibição de uma propriedade. Deve haver apenas um elemento [DisplayInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md).

Se houver vários elementos, o último será usado. Se nenhum elemento [DisplayInfo]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Sintaxe


```
<!-- displayInfo -->
<xs:element name="displayInfo">
    <xs:complexType>
        <xs:all>
            <xs:element name="stringFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="General"/>
                                <xs:enumeration value="FileName"/>
                                <xs:enumeration value="FilePath"/>
                                <xs:enumeration value="Hyperlink"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="booleanFormat" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="formatAs">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="YesNo"/>
                                <xs:enumeration value="OnOff"/>
                                <xs:enumeration value="TrueFalse"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="numberFormat" minOccurs="0" maxOccurs="1">
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
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="hh:mm"/>
                                <xs:enumeration value="hh:mm:ss"/>
                                <xs:enumeration value="hh:mm:ss.fff"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="dateTimeFormat" minOccurs="0" maxOccurs="1">
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
            <xs:element name="enumeratedList" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="value" type="xs:string" use="required"/>
                                <xs:attribute name="text" type="xs:string" use="required"/>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                            <xs:complexType>
                                <xs:attribute name="minValue" type="xs:string" use="required"/>
                                <xs:attribute name="setValue" type="xs:string"/>
                                <xs:attribute name="text" type="xs:string"/>
                            </xs:complexType>
                        </xs:element>
                    </xs:sequence>

                    <xs:attribute name="defaultText" type="xs:string"/>
                    <xs:attribute name="useValueForDefault" type="xs:boolean"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="drawControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="MultiLineText"/>
                                <xs:enumeration value="MultiValueText"/>
                                <xs:enumeration value="PercentBar"/>
                                <xs:enumeration value="ProgressBar"/>
                                <xs:enumeration value="Rating"/>
                                <xs:enumeration value="StaticText"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="editControl" minOccurs="0" maxOccurs="1">
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
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="filterControl" minOccurs="0" maxOccurs="1">
                <xs:complexType>
                    <xs:attribute name="control">
                        <xs:simpleType>
                            <xs:restriction base="xs:string">
                                <xs:enumeration value="Default"/>
                                <xs:enumeration value="Calendar"/>
                                <xs:enumeration value="Rating"/>
                            </xs:restriction>
                        </xs:simpleType>
                    </xs:attribute>
                </xs:complexType>
            </xs:element>
            <xs:element name="queryControl" minOccurs="0" maxOccurs="1">
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
        </xs:all>

        <xs:attribute name="defaultColumnWidth" type="xs:nonNegativeInteger" default="20"/>
        <xs:attribute name="displayType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        
        <xs:attribute name="alignment" default="Left">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Left"/>
                    <xs:enumeration value="Center"/>
                    <xs:enumeration value="Right"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="relativeDescriptionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Count"/>
                    <xs:enumeration value="Revision"/>
                    <xs:enumeration value="Length"/>
                    <xs:enumeration value="Duration"/>
                    <xs:enumeration value="Speed"/>
                    <xs:enumeration value="Rate"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Priority"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultSortDirection" default="Ascending">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                  <xs:enumeration value="Ascending"/>
                  <xs:enumeration value="Descending"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                   | Elementos filho                                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | [stringFormat](./propdesc-schema-stringformat.md)                                                             |
|                                                                  | [booleanFormat](./propdesc-schema-booleanformat.md)                                                           |
|                                                                  | [numberFormat](./propdesc-schema-numberformat.md)                                                             |
|                                                                  | [dateTimeFormat](./propdesc-schema-datetimeformat.md)                                                         |
|                                                                  | [enumeratedList](./propdesc-schema-enumeratedlist.md)                                                         |
|                                                                  | [drawControl](./propdesc-schema-drawcontrol.md)                                                               |
|                                                                  | [editControl](./propdesc-schema-editcontrol.md)                                                               |
|                                                                  | [filterControl](./propdesc-schema-filtercontrol.md)                                                           |
|                                                                  | [queryControl](./propdesc-schema-querycontrol.md) (somente Windows Vista. sem suporte no Windows 7 e posterior.) |



 

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
<td>defaultColumnWidth</td>
<td>Público. Opcional. O padrão é &quot; 20 &quot; .</td>
</tr>
<tr class="even">
<td>TipoDeExibição</td>
<td>Público. Opcional. O padrão é &quot; cadeia de caracteres &quot; . Especifica o tipo da cadeia de caracteres de exibição. Uma vez definido aqui, os valores de <strong>PROPDESC_DISPLAYTYPE</strong> associados são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplaytype"><strong>IPropertyDescription:: getdisplaytype</strong></a>. Os tipos a seguir são válidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Padrão. O valor é exibido como uma cadeia de caracteres. Use &quot; StringFormat &quot; para formatar. O método retorna PDDT_STRING.</td>
</tr>
<tr class="even">
<td>Número</td>
<td>Padrão para propriedades numéricas. O valor é exibido como um número. Use &quot; NumberFormat &quot; para formatar. O método retorna PDDT_NUMBER.</td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Padrão se <typeInfo type=&quot;Boolean&quot;> . O valor é exibido como um booliano. Use &quot; booleanFormat &quot; para formatar. O método retorna PDDT_BOOLEAN.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Padrão se <typeInfo type=&quot;DateTime&quot;> . O valor é exibido como uma data ou hora. Use &quot; DateTimeFormat &quot; para formatar. O método retorna PDDT_DATETIME.</td>
</tr>
<tr class="odd">
<td>Enumeração</td>
<td>O valor é exibido como um mapeamento de cadeia de caracteres de exibição fornecido pelo &quot; &quot; elemento enumeratedList. O método retorna PDDT_ENUMERATED.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>alinhamento</td>
<td>Opcional. O padrão é &quot; Left &quot; . 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Esquerda</td>
<td>Padrão. Alinhar à esquerda.</td>
</tr>
<tr class="even">
<td>Centro</td>
<td>Alinhar ao centro.</td>
</tr>
<tr class="odd">
<td>Direita</td>
<td>Alinhar à direita.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>relativeDescriptionType</td>
<td>Opcional. O padrão é &quot; geral &quot; . Especifica como dois valores dessa propriedade devem ser descritos quando eles são comparados entre si. No caso da equivalência, o &quot; mesmo &quot; sempre é usado. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescription"><strong>IPropertyDescription:: GetRelativeDescription</strong></a> e <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getrelativedescriptiontype"><strong>IPropertyDescription:: GetRelativeDescriptionType</strong></a> Use esse valor para determinar quais nomes de exibição de descrição relativa usar. 
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
<td>Padrão. Usa diferentes diferentes &quot; &quot;  /  &quot; &quot;  /  &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Data</td>
<td>Padrão se <typeInfo type=&quot;DateTime&quot;> . Usa &quot; o &quot;  /  &quot; mesmo &quot;  /  &quot; mais tarde &quot; , ou usa o &quot; mesmo mais &quot;  /  &quot; &quot;  /  &quot; recente &quot; , ou usa o &quot; mesmo mais cedo &quot;  /  &quot; &quot;  /  &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>Tamanho</td>
<td>Usa &quot; o &quot;  /  &quot; mesmo tamanho &quot;  /  &quot; maior&quot;</td>
</tr>
<tr class="even">
<td>Contagem</td>
<td>Usa &quot; o &quot;  /  &quot; mesmo tamanho &quot;  /  &quot; maior&quot;</td>
</tr>
<tr class="odd">
<td>Revisão</td>
<td>Usa o &quot; anterior &quot;  /  &quot; mesmo &quot;  /  &quot; mais tarde&quot;</td>
</tr>
<tr class="even">
<td>Comprimento</td>
<td>Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais curto&quot;</td>
</tr>
<tr class="odd">
<td>Duração</td>
<td>Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais curto&quot;</td>
</tr>
<tr class="even">
<td>Velocidade</td>
<td>Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais rápido&quot;</td>
</tr>
<tr class="odd">
<td>Tarifa</td>
<td>Usa o &quot; &quot;  /  &quot; mesmo &quot;  /  &quot; mais rápido&quot;</td>
</tr>
<tr class="even">
<td>Classificação</td>
<td>Usa &quot; o &quot;  /  &quot; mesmo &quot;  /  &quot; mais alto&quot;</td>
</tr>
<tr class="odd">
<td>Prioridade</td>
<td>Usa &quot; o &quot;  /  &quot; mesmo &quot;  /  &quot; mais alto&quot;</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>defaultSortDirection</td>
<td>Especifica a direção da classificação. O padrão é &quot; Ascending &quot; . 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crescente</td>
<td>Classifica em ordem crescente.</td>
</tr>
<tr class="even">
<td>Decrescente</td>
<td>Classifica decrescente.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
