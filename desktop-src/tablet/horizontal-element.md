---
description: Contém informações de formatação para as linhas horizontais usadas para a papelaria em uma nota de Diário.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432368"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contém informações de formatação para as linhas horizontais usadas para a papelaria em uma nota de Diário.

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
<td><a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a></td>
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
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</td>
<td>Opcional</td>
<td>Cor do elemento.</td>
<td>Um valor RGB hexadecimal. Corresponde à seguinte expressão regular: #[0-9a-zA-Z] {6} . Por exemplo, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcional</td>
<td>Espaçamento antes do elemento .</td>
<td>Qualquer inteiro não negativo.</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcional</td>
<td>Espaçamento entre esse elemento e elementos ao redor.</td>
<td>Qualquer inteiro não negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nome do esquema  | Leitor de Diário                                                    |



 

 

 




