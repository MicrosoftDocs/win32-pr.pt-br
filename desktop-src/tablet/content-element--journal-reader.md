---
description: Contém o conteúdo de uma página de diário.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [leitor de diário]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813347"
---
# <a name="content-element-journal-reader"></a>Leitor de diário de elementos de conteúdo \[\]

Contém o conteúdo de uma página de diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos pai

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementos filho

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Senha**](drawing-element.md)

[**Texto**](text-element.md)

[**Imagem**](image-element.md)

[**Sinalizador**](flag-element.md)

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
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tipo</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></td>
<td>Obrigatório</td>
<td>Se o tipo for &quot; Inert &quot; , o conteúdo não poderá ser modificado.<br/></td>
<td><ul>
<li>Normal</li>
<li>Inert</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | ComplexType [**ContentType**](contenttype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                  |
| Nome do esquema  | Leitor de diário                                              |



 

 

 




