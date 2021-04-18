---
description: Contém informações de título sobre a nota do diário.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781133"
---
# <a name="title-element"></a>Elemento Title

Contém informações de título sobre a nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**Telas**](stationery-element.md)

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
<td>Especifica o tipo de borda ao redor do título da nota.</td>
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
<td><strong>Datastyle</strong></td>
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
<td><a href="colortype-simple-type.md"><strong>SimpleType de ColorType</strong></a></td>
<td>Opcional</td>
<td>Especifica a cor do plano de fundo.</td>
<td>Confira <a href="colortype-simple-type.md"><strong>simpleType de ColorType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|              |                                                         |
|--------------|---------------------------------------------------------|
| Tipo de elemento | ComplexType de [**títulotype**](titletype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk              |
| Nome do esquema  | Leitor de diário                                          |



 

 

 



