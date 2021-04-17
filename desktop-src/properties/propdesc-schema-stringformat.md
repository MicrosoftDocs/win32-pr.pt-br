---
description: 'Especifica como IPropertyDescription:: FormatForDisplay deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755141"
---
# <a name="stringformat"></a>stringFormat

Especifica como [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) deve formatar o valor da propriedade como uma cadeia de caracteres. Isso é aplicável somente se <displayInfo displayType="String"> . Deve haver apenas um elemento [StringFormat]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [StringFormat]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Syntax


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
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
<td>Padrão. Retorna o valor como uma cadeia de caracteres não formatada.</td>
</tr>
<tr class="even">
<td>FileName</td>
<td>Formata o valor como um nome de arquivo. Oculta a extensão de acordo com as configurações do usuário. Requer que o tipo de propriedade seja cadeia de caracteres.</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>Formata o valor como um caminho de arquivo. Oculta a extensão de acordo com as configurações do usuário. Requer que o tipo de propriedade seja cadeia de caracteres.</td>
</tr>
<tr class="even">
<td>Hyperlink</td>
<td>Formata o valor como um hiperlink.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
