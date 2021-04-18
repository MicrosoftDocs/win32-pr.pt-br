---
title: Elemento Argument
description: O elemento Argument contém uma parte de uma cadeia de caracteres de condição.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Elemento Argument Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813390"
---
# <a name="argument-element"></a>Elemento Argument

O elemento **Argument** contém uma parte de uma cadeia de caracteres de condição. Uma cadeia de caracteres de condição normalmente tem uma parte de condição e uma parte de valor. Por exemplo, na cadeia de caracteres de condição "artista é igual a Joe", a parte da condição é "Equals" e a parte do valor é "Joe".

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Atributos

**nome** (obrigatório)

O nome de uma parte da cadeia de caracteres da condição.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                         |
|-----------|----------------------------------|
| Pai    | [fragmento](fragment-element.md) |
| Filho     | Nenhum                             |



 

## <a name="remarks"></a>Comentários

Quando o atributo **Name** de um elemento **Fragment** é uma característica de item de mídia, como o artista do álbum, ou o gênero, o elemento **Fragment** deve conter dois elementos **Argument** : um que especifica uma condição e outro que especifica um valor. A tabela a seguir mostra dois valores possíveis para o atributo **Name** e como os elementos **Argument** são usados para especificar condições e valores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Condição</td>
<td>O conteúdo do elemento <strong>Argument</strong> é a parte da condição de uma cadeia de caracteres de condição. Por exemplo, no artista de cadeia de caracteres de condição &quot; igual a Joe &quot; , a parte da condição é &quot; igual a &quot; . A parte da condição de uma cadeia de caracteres de condição deve ser uma das seguintes: Equals, não é igual a, Contains, não contém, é menor que, é maior que, is, is, is, is, is before, é mais recente do que, no máximo, é necessário, no mínimo, o que é.</td>
</tr>
<tr class="even">
<td>Valor</td>
<td>O conteúdo do elemento <strong>Argument</strong> é a parte de valor de uma cadeia de caracteres de condição. Por exemplo, no artista de cadeia de caracteres de condição &quot; igual a Joe &quot; , a parte de valor é &quot; Joe &quot; . Exemplo<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Quando o atributo de **nome** de um elemento de **fragmento** é "limitar o tamanho total para" ou "limitar duração total a", o elemento de **fragmento** deve conter dois elementos de **argumento** : um que especifique um formato e um que especifique um número. A tabela a seguir mostra dois valores possíveis para o atributo **Name** e como os elementos **Argument** são usados para limitar o tamanho ou a duração de uma lista de reprodução.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Formatar</td>
<td>Quando o atributo <strong>Name</strong> do elemento <strong>Fragment</strong> é &quot; limitar o tamanho total a &quot; , o conteúdo do elemento <strong>Argument</strong> deve ser um dos seguintes: kilobytes, megabytes ou gigabytes. quando o atributo <strong>Name</strong> do elemento <strong>Fragment</strong> é &quot; limitar a duração total para &quot; , o conteúdo do elemento <strong>Argument</strong> deve ser um dos seguintes: segundos, minutos, horas ou dias.<br/></td>
</tr>
<tr class="even">
<td>Número</td>
<td>O conteúdo do elemento <strong>Argument</strong> é um número que limita o tamanho ou a duração da lista de reprodução. Disso<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Quando o atributo **Name** de um elemento **Fragment** é "limitar número de itens", o elemento **Fragment** deve conter um elemento **Argument** que especifica o número de itens. A tabela a seguir mostra como usar o valor numérico do atributo **Name** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Número</td>
<td>O conteúdo do elemento <strong>Argument</strong> é um número que limita o número de itens em uma lista de reprodução. Exemplo<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Referência de elementos da playlist do Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





