---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade booleanFormat como uma cadeia de caracteres.'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6ed13194fa18ba558c9c7fbac8fb7cd4317b67
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623712"
---
# <a name="booleanformat"></a>booleanFormat

Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType="String"> . Deve haver apenas um elemento [booleanFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [booleanFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

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
<td>Público. Opcional. O padrão é &quot; YesNo &quot; . Os seguintes valores são válidos: 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>YesNo</td>
<td>Padrão. Formata o valor como &quot; Sim &quot; ou &quot; não &quot; . Requer que o tipo de propriedade seja booliano.</td>
</tr>
<tr class="even">
<td>OnOff</td>
<td>Formata o valor como &quot; on &quot; ou &quot; off &quot; . Requer que o tipo de propriedade seja booliano.</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>Formata o valor como &quot; true &quot; ou &quot; false &quot; . Requer que o tipo de propriedade seja booliano.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
