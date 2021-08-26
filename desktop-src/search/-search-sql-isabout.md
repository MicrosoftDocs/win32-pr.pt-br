---
description: O termo ISABOUT corresponde a colunas em um grupo de um ou mais termos de pesquisa.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Termo ISABOUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee772bbd3be1f9ef3924989dfbaa2a9afd77d4a6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627352"
---
# <a name="isabout-term"></a>Termo ISABOUT

**Preterido**

Esse recurso foi removido a partir Windows 8. Se você escrever novos aplicativos, evite usar esse recurso preterido. Se você modificar aplicativos existentes, será incentivado a remover qualquer dependência desse recurso.

O termo ISABOUT corresponde a colunas em um grupo de um ou mais termos de pesquisa. Ele tem a seguinte sintaxe:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



O termo opcional RANKMETHOD especifica o método de cálculo usado para classificar os documentos que corresponderem a um ou mais dos componentes. Se nenhum RANKMETHOD for especificado, o método de classificação padrão Coeficiente de Jaccard será usado.

O termo ISABOUT pode ter um ou mais componentes. As colunas especificadas no predicado [CONTAINS](-search-sql-contains.md) são testadas em relação a cada componente. O documento será incluído nos resultados se pelo menos um dos componentes corresponde. Vírgulas separam vários componentes.

A parte do componente tem a seguinte sintaxe:


```
<match_term> [<weight_term>]
```



Você pode usar o termo WEIGHT opcional para alterar a importância relativa de cada termo dentro do termo ISABOUT. Se nenhum termo de peso for aplicado, o peso padrão de 1,0 será implícito.

A tabela a seguir descreve possíveis tipos de termos de combinação.



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
<td>Uma única palavra sem espaços ou outra pontuação.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
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
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a>Ponderação de coluna ISABOUT

O termo ISABOUT classifica documentos correspondentes com base na proximidade com que cada documento corresponde ao conjunto de termos de correspondência na consulta. Você pode usar a ponderação de coluna para dar mais importância à correspondência de alguns termos de correspondência do que outros. Cada termo de combinação no termo ISABOUT pode ter um valor de peso aplicado. O peso é aplicado a um único termo de combinação e é indicado pela palavra-chave "WEIGHT". O termo WEIGHT tem duas sintaxes alternativas:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



O valor de peso deve estar entre 0 e 1,0, com no máximo três casas decimais. Especificar um valor de peso fora desse intervalo resulta em uma mensagem de erro. O valor de classificação sem peso para um termo é multiplicado pelo valor de peso para o termo.

Se nenhum peso for especificado para um termo de combinação, o valor padrão, 1,0, será implícito.

### <a name="example"></a>Exemplo

O exemplo a seguir aplica pesos aos dois termos de combinação ISABOUT, usando a sintaxe longa e curta para valores de peso.


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> </dl>

 

 



