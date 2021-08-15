---
description: O predicado CONTAINS faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c821431bb5f00319fe47414dcce5240775f2ce78335998c1bb30b84dc9fe17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863709"
---
# <a name="contains-predicate"></a>Predicado CONTAINS

O predicado CONTAINS faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto. O predicado CONTAINS tem recursos para palavras correspondentes, correspondência de formas de palavras informativas, pesquisa usando caracteres curinga e pesquisa usando a proximidade. Você também pode aplicar pesos em um predicado CONTAINS para definir a importância das colunas em que o termo de pesquisa é encontrado. O predicado CONTAINS é mais adequado para correspondências exatas, em contraste com o predicado [FREETEXT](-search-sql-freetext.md) , que é mais adequado para localizar documentos que contenham combinações das palavras de pesquisa espalhadas por toda a coluna. As pesquisas não diferenciam letras maiúsculas de minúsculas.

Veja a seguir a sintaxe básica do predicado CONTAINS:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

A referência de coluna de texto completo \_ é opcional. Com ele, você pode limitar a pesquisa a uma única coluna ou a um grupo de colunas no qual o predicado CONTAINS é testado. Quando a coluna FULLTEXT é especificada como "ALL" ou " \* ", todas as propriedades de texto indexado são pesquisadas. Embora a coluna não precise ser uma propriedade de texto, os resultados poderão ser insignificantes se a coluna for outro tipo de dados. O nome da coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado, e você deve separá-lo da condição por uma vírgula. Se nenhuma coluna de texto completo for especificada, a coluna System. Search. Content, que é o corpo do documento, será usada.

A parte LCID do predicado especifica a localidade de pesquisa. Isso instrui o mecanismo de pesquisa a usar o separador de palavras apropriado e formulários de inflexão para a consulta de pesquisa. para especificar a localidade, forneça o Windows identificador de código de idioma padrão (LCID). Por exemplo, 1033 é o LCID para o Estados Unidos-Inglês. Coloque o LCID como o último item dentro dos parênteses da cláusula CONTAINS. Para obter informações importantes sobre a pesquisa e os idiomas, consulte [usando pesquisas localizadas](-search-sql-usinglocsearches.md).

> [!NOTE]  
> A localidade de pesquisa padrão é a localidade padrão do sistema.

A \_ parte da condição Contains deve ser colocada entre aspas simples por palavras únicas ou aspas duplas para frases e consiste em um ou mais termos de pesquisa de conteúdo que são combinados usando os operadores lógicos  **e** ou. Você pode usar o operador unário opcional **não** após um operador **and** para negar o valor lógico de um termo de pesquisa de conteúdo.

> [!NOTE]  
> O operador **not** só pode ocorrer depois **de e**. Você não poderá usar o operador **not** se houver apenas uma condição de correspondência ou depois do operador **or** .

Você pode usar parênteses para agrupar e aninhar termos de pesquisa de conteúdo. A tabela a seguir descreve a ordem de precedência para os operadores lógicos.

| Ordem (precedência) | Operador lógico |
|--------------------|------------------|
| Primeiro (mais alto)    | **NOT**          |
| Segundo             | **AND**          |
| Terceiro (mais baixo)     | **OR**           |

Os operadores lógicos do mesmo tipo são associativos e não há nenhuma ordem de cálculo especificada. Por exemplo, (A **e** B) **e** (C **e** d) podem ser calculados (B **e** C) **e** (a **e** d) sem alteração no resultado lógico.

A tabela a seguir descreve os tipos de termos de pesquisa de conteúdo.

<!-- markdownlint-disable MD033 -->
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
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
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
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Coluna de texto completo</td>
<td>Um nome de coluna de propriedade no qual corresponder à consulta restante.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Boolean</td>
<td>Palavras, frases e cadeias de caracteres curinga combinadas usando os operadores boolianos <strong>and</strong>, <strong>or</strong>ou <strong>not</strong>. Coloque os termos boolianos entre aspas duplas.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Near</td>
<td>Palavras, frases ou caracteres curinga separados pela função perto de. Para obter mais informações, consulte a <a href="-search-sql-near.md">curto prazo</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>FormsOf</td>
<td>Corresponde a uma palavra e as versões de inflexão dessa palavra. Para obter mais informações, consulte <a href="-search-sql-formsof.md">FORMSOF Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>IsAbout</td>
<td>Combina os resultados correspondentes em vários termos de pesquisa de palavras, frases ou caracteres curinga. Cada termo de pesquisa pode, opcionalmente, ser ponderado. Opcionalmente, você pode especificar o método de cálculo de classificação, que combina os pesos e quantos itens o documento corresponde. Para obter mais informações, consulte o <a href="-search-sql-isabout.md">termo ISABOUT</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

Esta seção inclui os tópicos a seguir:

- [Usando curingas no predicado CONTAINS](-search-sql-wildcards.md)
- [FORMSOF termo](-search-sql-formsof.md)
- [@ SOBRE o termo](-search-sql-isabout.md)
- [CURTO prazo](-search-sql-near.md)

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[Cláusula WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Conceitual

[Predicados de texto completo](-search-sql-fulltextpredicates.md)

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
