---
description: Contém o plano de fundo de um elemento JournalDocument ou de um elemento JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Elemento background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46388d56c04fc24ecd578788eecf9926ef01a301
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436581"
---
# <a name="background-element"></a>Elemento background

Contém o plano de fundo de um elemento [**JournalDocument**](journaldocument-element.md) ou de um elemento [**JournalPage**](journalpage-element.md) .

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**Telas**](stationery-element.md)

## <a name="child-elements"></a>Elementos filho

[**Imagem**](image-element.md)

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
<td>Especifica o estilo do plano de fundo.</td>
<td><ul>
<li>Nenhum</li>
<li>Sólido</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Cor</strong></td>
<td>SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></td>
<td>Opcional</td>
<td>Especifica a cor do plano de fundo.</td>
<td>Confira simpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informações do elemento



|                  | Valor                                                             |
|------------------|-------------------------------------------------------------------|
| **Tipo de elemento** | ComplexType [**em segundo plano**](backgroundtype-complex-type.md) |
| **Namespace**    | urn: esquemas-Microsoft-com: Tablet: RichInk                        |
| **Nome do esquema**  | Leitor de diário                                                    |



 

 

 



