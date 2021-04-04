---
description: Contém informações de formatação para as linhas horizontais usadas para o papel de carta em uma nota do diário.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647248"
---
# <a name="horizontal-element"></a>Elemento horizontal

Contém informações de formatação para as linhas horizontais usadas para o papel de carta em uma nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
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



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**ComplexType de horizontaltype**](horizontaltype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                        |
| Nome do esquema  | Leitor de diário                                                    |



 

 

 




