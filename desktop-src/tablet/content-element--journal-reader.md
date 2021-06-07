---
description: Contém o conteúdo de uma página De diário.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [Leitor de Diário]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432148"
---
# <a name="content-element-journal-reader"></a>Leitor de Diário \[ do Elemento de Conteúdo\]

Contém o conteúdo de uma página De diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos pai

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementos filho

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Desenho**](drawing-element.md)

[**Text**](text-element.md)

[**Imagem**](image-element.md)

[**Bandeira**](flag-element.md)

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
<li>Inerte</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**ComplexType ContentType**](contenttype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nome do esquema  | Leitor de Diário                                              |



 

 

 




