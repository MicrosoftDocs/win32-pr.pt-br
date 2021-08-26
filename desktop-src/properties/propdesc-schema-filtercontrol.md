---
description: Especifica qual controle usar no menu de filtro de header.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: Filtercontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f002543b220347ba9aaba3659aa9a66f8aea7760b9d8a9177ef2980a823434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885956"
---
# <a name="filtercontrol"></a>Filtercontrol

Especifica qual controle usar no menu de filtro de header. Deve haver apenas um [elemento filterControl]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Se houver vários elementos, o último será usado. Se nenhum [elemento filterControl]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

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
<td>Público. Opcional. O padrão é &quot; &quot; Padrão. Os seguintes valores são válidos: 
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
<td>Padrão. Usa o controle padrão, com base no <typeInfo type=&quot;&quot;> atributo . O tipo padrão é &quot; DateTime &quot; e o controle padrão é Calendar &quot; &quot; . Qualquer outro tipo resulta em nenhum controle de filtro especial.</td>
</tr>
<tr class="even">
<td>Calendário</td>
<td>Usa o controle de calendário.</td>
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



 

 

 
