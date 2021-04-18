---
description: O termo NEAR é usado para especificar que dois termos de pesquisa de conteúdo devem ser relativamente próximos um do outro para serem reconhecidos como correspondência para o predicado CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: CURTO prazo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296240"
---
# <a name="near-term"></a>CURTO prazo

O termo NEAR é usado para especificar que dois termos de pesquisa de conteúdo devem ser relativamente próximos um do outro para serem reconhecidos como correspondência para o predicado [Contains](-search-sql-contains.md) .

A sintaxe para o termo NEAR é:


```
<content_search_term> NEAR | ~ <content_search_term>
```



O termo NEAR pode ser representado pela palavra-chave "NEAR" ou por um til (~).

Quando as palavras Unidas perto da consulta são encontradas em aproximadamente 50 palavras umas das outras dentro da coluna que está sendo pesquisada, o próximo termo retorna uma correspondência. Quanto mais próximas forem as duas palavras, maior será a classificação calculada para o termo próximo. Quanto mais distante forem as duas palavras, menor será a classificação.

> [!Note]  
> O número de palavras entre os termos de pesquisa encontrados é aproximado e depende da aparência de palavras de ruído, como "a" ou "a", e como separadores o token de texto. Pode ser menor que 50.

 


A tabela a seguir descreve os tipos de termo de pesquisa de conteúdo que podem ser usados com um termo próximo em um predicado CONTAINS.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrição</th>
<th>Exemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Uma única palavra sem espaços ou outra Pontuação. Aspas duplas não são necessárias.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Frase</td>
<td>Várias palavras ou espaços incluídos.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Curinga</td>
<td>Palavras ou frases com o asterisco (*) adicionado ao final. Para obter mais informações, consulte <a href="-search-sql-wildcards.md">usando curingas no predicado CONTAINS</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> Se as palavras de correspondência especificadas com o termo NEAR forem encontradas na coluna que está sendo pesquisada, mas estiverem mais distantes de 50 palavras, o resultado ainda será retornado, mas terá uma [classificação](-search-sql-understandingrelevancevalues.md) de 0.

 

### <a name="example"></a>Exemplo

O exemplo a seguir mostra o encadeamento de termos próximos, usando as formas curta e longa do termo:


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Usando curingas no predicado CONTAINS](-search-sql-wildcards.md)
</dt> </dl>

 

 



