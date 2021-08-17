---
description: Define as linhas de margem desenhadas na página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ff764585919ff144ebc25ac568caf1af74410a2f337beb03d5ce484f7d1abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350436"
---
# <a name="margin-element"></a>Elemento Margin

Define as linhas de margem desenhadas na página.

## <a name="definition"></a>Definição

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Elementos pai

Nenhum.

## <a name="child-elements"></a>Elementos filho

Nenhum..

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
<th>Valores possíveis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Estilo</strong></td>
<td><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</td>
<td>Obrigatório</td>
<td>Especifica o tipo de linha a ser desenhada.</td>
<td><ul>
<li>Nenhum</li>
<li>Sólido</li>
<li>Traço</li>
<li>Ponto</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Cor</strong></td>
<td>SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></td>
<td>Opcional</td>
<td>Cor do elemento.</td>
<td>Um valor RGB hexadecimal. Corresponde à seguinte expressão regular: # [0-9A-zA-Z] {6} . Por exemplo, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>Tipo</strong></td>
<td><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</td>
<td>Opcional</td>
<td>Indica a margem esquerda ou direita.</td>
<td><ul>
<li>Esquerda</li>
<li>Direita</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Espaçamento</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcional</td>
<td>Espaçamento entre a borda da página e a margem.</td>
<td>Qualquer inteiro não negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-----------------------------------------------------------|
| Tipo de elemento | ComplexType de [**margintype**](margintype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                |
| Nome do esquema  | Leitor de diário                                            |



 

 

 




