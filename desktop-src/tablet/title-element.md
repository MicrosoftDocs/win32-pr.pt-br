---
description: Contém informações de título sobre a nota Do diário.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432218"
---
# <a name="title-element"></a>Elemento Title

Contém informações de título sobre a nota Do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**Papelaria**](stationery-element.md)

## <a name="child-elements"></a>Elementos filho

[**TitleArea**](titlearea-element.md)

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
<td><strong>xs:string</strong></td>
<td>Obrigatório</td>
<td>Especifica o tipo de borda em torno do título da nota.</td>
<td><ul>
<li>Nenhum</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Obrigatório</td>
<td>Define se o título inclui uma data ou não.</td>
<td><ul>
<li>Nenhum</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Cor</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></td>
<td>Opcional</td>
<td>Especifica a cor do plano de fundo.</td>
<td>Consulte <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



| Elemento      | Valor                                                   |
|--------------|---------------------------------------------------------|
| Tipo de elemento | [**ComplexType TitleType**](titletype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink              |
| Nome do esquema  | Leitor de Diário                                          |



 

 

 



