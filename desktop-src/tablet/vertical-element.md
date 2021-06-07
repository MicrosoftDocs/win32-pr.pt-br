---
description: Contém as informações que descrevem o componente vertical das linhas no papel de carta usado pela anotação do diário. Usado, por exemplo, quando a observação tem linhas de grade.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432118"
---
# <a name="vertical-element"></a>Elemento vertical

Contém as informações que descrevem o componente vertical das linhas no papel de carta usado pela anotação do diário. Usado, por exemplo, quando a observação tem linhas de grade.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

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
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcional</td>
<td>Espaçamento antes do elemento.</td>
<td>Qualquer inteiro não negativo.</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcional</td>
<td>Espaçamento entre este elemento e elementos circundantes.</td>
<td>Qualquer inteiro não negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                         |
|--------------|---------------------------------------------------------------|
| Tipo de elemento | ComplexType de [**verticaltype**](verticaltype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                    |
| Nome do esquema  | Leitor de diário                                                |



 

 

 




