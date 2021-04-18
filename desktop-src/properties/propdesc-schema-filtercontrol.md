---
description: Especifica o controle a ser usado no menu de filtro de cabeçalho.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756786"
---
# <a name="filtercontrol"></a>filterControl

Especifica o controle a ser usado no menu de filtro de cabeçalho. Deve haver apenas um elemento [filterControl]() para cada elemento [DisplayInfo](./propdesc-schema-displayinfo.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [filterControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax"></a>Syntax


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
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
<td>Padrão. Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo. O tipo padrão é &quot; DateTime &quot; e o controle padrão é &quot; Calendar &quot; . Qualquer outro tipo resulta em nenhum controle de filtro especial.</td>
</tr>
<tr class="even">
<td>Calendário</td>
<td>Usa o controle Calendar.</td>
</tr>
<tr class="odd">
<td>Classificação</td>
<td>Usa o controle de classificação de 5 estrelas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
