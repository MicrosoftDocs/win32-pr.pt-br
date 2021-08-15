---
description: Especifica como IPropertyDescription::FormatForDisplay deve formatar o valor da propriedade booleanFormat como uma cadeia de caracteres.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df8c7d2a72f7229c99fb13244aae2b6bc1d4ec63c272f10aa2d35a81740f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460046"
---
# <a name="booleanformat"></a>booleanFormat

Especifica como [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso será aplicável somente se <displayInfo displayType="String"> . Deve haver apenas um elemento [booleanFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se houver vários elementos, o último será usado. Se nenhum [elemento booleanFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Sintaxe


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
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
<td>Público. Opcional. O padrão é &quot; &quot; SimNo. Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yesno</td>
<td>Padrão. Formatar o valor como &quot; Sim &quot; ou &quot; &quot; Não. Requer que o tipo de propriedade seja booliana.</td>
</tr>
<tr class="even">
<td>Onoff</td>
<td>Formatar o valor como &quot; On &quot; ou &quot; &quot; Off. Requer que o tipo de propriedade seja booliana.</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>Formatar o valor como &quot; True &quot; ou &quot; &quot; False. Requer que o tipo de propriedade seja booliana.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
