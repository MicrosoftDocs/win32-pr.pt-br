---
description: Especifica o controle a ser usado ao exibir apenas a propriedade.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a330854f19005f7f2863c337451b1dcc56cea3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632044"
---
# <a name="drawcontrol"></a>drawControl

Especifica o controle a ser usado ao exibir apenas a propriedade. Deve haver apenas um elemento [drawControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [drawControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

Essa forma do controle não permite a edição de propriedade.

## <a name="syntax"></a>Sintaxe


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
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
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
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
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Padrão</td>
<td>Padrão. Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo. O tipo padrão é &quot; cadeia de caracteres &quot; (valores múltiplos) e o controle padrão é &quot; MultiValueText &quot; . Qualquer outro tipo resulta no uso do &quot; &quot; controle staticText.</td>
</tr>
<tr class="even">
<td>MultiLineText</td>
<td>Usa o controle de texto de várias linhas.</td>
</tr>
<tr class="odd">
<td>MultiValueText</td>
<td>Usa o controle de texto de valores múltiplos.</td>
</tr>
<tr class="even">
<td>PercentBar</td>
<td>Usa o controle de barra de porcentagem.</td>
</tr>
<tr class="odd">
<td>ProgressBar</td>
<td>Usa o controle da barra de progresso.</td>
</tr>
<tr class="even">
<td>Classificação</td>
<td>Usa o controle de classificação de 5 estrelas.</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>Usa <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription:: FormatForDisplay</strong></a> para exibir o valor da propriedade.</td>
</tr>
<tr class="even">
<td>Íconelist</td>
<td><strong>Windows 7 e posterior.</strong> Uma enumeração de ícones.</td>
</tr>
<tr class="odd">
<td>BooleanCheckMark</td>
<td><strong>Windows 7 e posterior.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
