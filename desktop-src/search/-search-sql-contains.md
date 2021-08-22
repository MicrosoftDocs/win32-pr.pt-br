---
description: O predicado CONTAINS faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2885187d0dd25f38e6bbf40b3259164f0aa91e05
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625282"
---
# <a name="contains-predicate"></a>Predicado CONTAINS

O predicado CONTAINS faz parte da cláusula WHERE e dá suporte à pesquisa de palavras e frases em colunas de texto. O predicado CONTAINS tem recursos para correspondência de palavras, correspondência de formas de palavras inflexas, pesquisa usando caracteres curinga e pesquisa usando proximidade. Você também pode aplicar pesos em um predicado CONTAINS para definir a importância das colunas em que o termo de pesquisa é encontrado. O predicado CONTAINS é mais adequado para as correspondeções exatas, ao contrário do predicado [FREETEXT,](-search-sql-freetext.md) que é mais adequado para localizar documentos que contenham combinações das palavras de pesquisa distribuídas pela coluna. As pesquisas não diferenciam letras maiúsculas de minúsculas.

Veja a seguir a sintaxe básica do predicado CONTAINS:

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

A referência de \_ coluna de texto completo é opcional. Com ele, você pode limitar a pesquisa a uma única coluna ou um grupo de colunas no qual o predicado CONTAINS é testado. Quando a coluna de texto completo é especificada como "ALL" ou " ", todas \* as propriedades de texto indexadas são pesquisadas. Embora a coluna não seja necessária para ser uma propriedade de texto, os resultados poderão não ter sentido se a coluna for algum outro tipo de dados. O nome da coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado e você deve separá-lo da condição por uma vírgula. Se nenhuma coluna de texto completo for especificada, a coluna System.Search.Contents, que é o corpo do documento, será usada.

A parte LCID do predicado especifica a localidade de pesquisa. Isso instrui o mecanismo de pesquisa a usar o disjuntor de palavras e formulários flexicionais apropriados para a consulta de pesquisa. Para especificar a localidade, forneça o Windows LCID (identificador de código de idioma padrão). Por exemplo, 1033 é o LCID para Estados Unidos-inglês. Coloque o LCID como o último item dentro dos parênteses da cláusula CONTAINS. Para obter informações importantes sobre pesquisa e idiomas, consulte [Usando pesquisas localizadas.](-search-sql-usinglocsearches.md)

> [!NOTE]  
> A localidade de pesquisa padrão é a localidade padrão do sistema.

A parte de condição contém deve ser entre aspas simples para palavras simples ou aspas duplas para frases e consiste em um ou mais termos de pesquisa de conteúdo que são combinados usando os operadores lógicos \_ **AND** ou **OR**. Você pode usar o operador unário opcional **NOT** após um **operador AND** para negar o valor lógico de um termo de pesquisa de conteúdo.

> [!NOTE]  
> O **operador NOT** pode ocorrer somente após **AND.** Você não poderá usar **o operador NOT** se houver apenas uma condição de corresponder ou após o operador **OR.**

Você pode usar parênteses para agrupar e aninhar termos de pesquisa de conteúdo. A tabela a seguir descreve a ordem de precedência para os operadores lógicos.

| Ordem (precedência) | Operador lógico |
|--------------------|------------------|
| Primeiro (mais alto)    | **NOT**          |
| Segundo             | **AND**          |
| Terceiro (mais baixo)     | **OR**           |

Operadores lógicos do mesmo tipo são associativos e não há nenhuma ordem de cálculo especificada. Por exemplo, (A **AND** B) **AND** (C **AND** D) pode ser calculado (B **E** C) **AND** (A **AND** D) sem nenhuma alteração no resultado lógico.

A tabela a seguir descreve os tipos de termos de pesquisa de conteúdo.

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Type</th>
<th>Descrição</th>
<th>Exemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Uma única palavra sem espaços ou outra pontuação. Aspas duplas não são necessárias.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<col  />
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
<td>Palavras ou frases com o asterisco (*) adicionado ao final. Para obter mais informações, <a href="-search-sql-wildcards.md">consulte Using Wildcards in the CONTAINS Predicate</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Um nome de coluna de propriedade em relação ao qual corresponder à consulta restante.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Palavras, frases e cadeias de caracteres curinga combinadas usando os operadores boolianas <strong>AND</strong>, <strong>OR</strong>ou <strong>NOT</strong>. Coloque os termos boolianas entre aspas duplas.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Palavras, frases ou curingas separados pela função NEAR. Para obter mais informações, consulte <a href="-search-sql-near.md">NEAR Term</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Corresponde a uma palavra e às versões inflecionais dessa palavra. Para obter mais informações, consulte <a href="-search-sql-formsof.md">Termo FORMSOF</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td>Combina resultados correspondentes em vários termos de pesquisa de palavras, frases ou curingas. Opcionalmente, cada termo de pesquisa pode ser ponderado. Opcionalmente, você pode especificar o método de cálculo de classificação, que combina os pesos e quantos itens o documento corresponde. Para obter mais informações, consulte <a href="-search-sql-isabout.md">Termo ISABOUT</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
- [Termo FORMSOF](-search-sql-formsof.md)
- [Termo ISABOUT](-search-sql-isabout.md)
- [Curto prazo](-search-sql-near.md)

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[Cláusula WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Conceitual

[Predicados de texto completo](-search-sql-fulltextpredicates.md)

[Predicados que não são de texto completo](-search-sql-nonfulltextpredicates.md)
