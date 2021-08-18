---
description: O termo ISABOUT corresponde a colunas em um grupo de um ou mais termos de pesquisa.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: '@ SOBRE o termo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5665e7bf62da4858cf2e7d68e65d0f42771903d55e3189db12f19cdd5414530d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969605"
---
# <a name="isabout-term"></a>@ SOBRE o termo

**Preterido**

Este recurso foi removido a partir de Windows 8. Se você escrever novos aplicativos, evite usar esse recurso preterido. Se você modificar os aplicativos existentes, será altamente recomendável remover qualquer dependência desse recurso.

O termo ISABOUT corresponde a colunas em um grupo de um ou mais termos de pesquisa. Ele tem a seguinte sintaxe:


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



O Termo RANKMETHOD opcional especifica o método de cálculo usado para classificar os documentos que correspondem a um ou mais dos componentes. Se nenhum RANKMETHOD for especificado, o método de classificação de coeficiente Jaccard padrão será usado.

O termo ISABOUT pode ter um ou mais componentes. As colunas especificadas no predicado [Contains](-search-sql-contains.md) são testadas em relação a cada componente. O documento será incluído nos resultados se pelo menos um dos componentes corresponder. Vírgulas separam vários componentes.

A parte do componente tem a seguinte sintaxe:


```
<match_term> [<weight_term>]
```



Você pode usar a condição de peso opcional para alterar a importância relativa de cada termo dentro do termo ISABOUT. Se nenhum termo de peso for aplicado, o peso de 1,0 padrão será implícito.

A tabela a seguir descreve os tipos de termo de correspondência possíveis.



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
<td>Uma única palavra sem espaços ou outra Pontuação.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<col style="width: 100%" />
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



 

## <a name="isabout-column-weighting"></a>Issobre o peso da coluna

O termo ISABOUT classifica os documentos correspondentes com base no quão próximo cada documento corresponde ao conjunto de termos de correspondência na consulta. Você pode usar o peso de coluna para posicionar mais importância na correspondência de alguns termos de correspondência do que outros. Cada termo de correspondência no termo ISABOUT pode ter um valor de peso aplicado. O peso é aplicado a um único termo de correspondência e é indicado pela palavra-chave "WEIGHT". O termo de peso tem duas sintaxes alternativas:


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



O valor de peso deve estar entre 0 e 1,0, com no máximo três casas decimais. A especificação de um valor de peso fora desse intervalo resulta em uma mensagem de erro. O valor de classificação não ponderada para um termo é multiplicado pelo valor de peso do termo.

Se nenhum peso for especificado para um termo de correspondência, o valor padrão, 1,0, será implícito.

### <a name="example"></a>Exemplo

O exemplo a seguir aplica pesos aos dois termos de correspondência, usando a sintaxe longa e curta para valores de peso.


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

 

 



