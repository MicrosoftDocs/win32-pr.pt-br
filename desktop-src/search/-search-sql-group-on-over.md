---
description: O GROUP ON...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: GROUP ON ... SOBRE... Declaração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df21bb53babd25ae3e407032c6cf9d3774323e85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882017"
---
# <a name="group-on--over--statement"></a>GROUP ON ... SOBRE... Declaração

O GROUP ON... SOBRE... A instrução retorna um conjunto de linhas hierárquico no qual os resultados da pesquisa são divididos em grupos com base em uma coluna especificada e em intervalos de agrupação opcionais. Se você agrupar na [coluna System.Kind,](../properties/props-system-kind.md) o conjunto de resultados será dividido em vários grupos: um para documentos, outro para comunicações e assim por diante. Se você agrupar [System.Size](../properties/props-system-size.md) e o intervalo de grupos de 100 KB, o conjunto de resultados será dividido em três grupos: itens de tamanho < 100 KB, itens de tamanho >= 100 KB e itens sem valor de tamanho. Você também pode agregar grupos com funções.

Este tópico aborda os seguintes assuntos:

-   [Sintaxe](#syntax)
-   [Intervalos de grupo](#group-ranges)
-   [Rotulando grupos](#labeling-groups)
-   [Ordenando grupos](#ordering-groups)
-   [Aninhando grupos](#nesting-groups)
-   [Agrupando em propriedades de vetor](#grouping-on-vector-properties)
-   [Mais exemplos](#more-examples)
-   [Tópicos relacionados](#related-topics)

## <a name="syntax"></a>Syntax

O GROUP ON ... SOBRE... A instrução tem a seguinte sintaxe:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



em que os intervalos de agrupação são definidos da seguinte forma:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



A coluna GROUP ON pode ser um identificador regular ou &lt; &gt; [delimitado](-search-sql-identifiers.md) para uma propriedade no armazenamento de propriedades.

O opcional é uma lista de um ou mais valores (número, data ou cadeia de caracteres) usados para dividir <group ranges> os resultados em grupos. O identifica um ponto de divisão no conjunto de resultados retornado e o identifica um rótulo amigável <range limit> <label> para um grupo. Você pode dividir o conjunto de resultados em quantos grupos você precisar.

O primeiro grupo de resultados inclui itens com o valor mínimo possível para a propriedade especificada até , mas não incluindo o primeiro limite de intervalo. Esse grupo pode ser referenciado com a palavra-chave MINVALUE. O segundo grupo pode ser referenciado com o próprio especificador de limite de intervalo e inclui itens cujo valor para a propriedade especificada é igual ou maior que o limite de intervalo. Todos os itens que não têm um valor para a propriedade especificada são retornados por último e podem ser referenciados com a palavra-chave **NULL.**

Por exemplo, um limite de intervalo de '2006-01-01' para a propriedade [System.DateCreated](../properties/props-system-datecreated.md) divide o conjunto de resultados em itens com datas anteriores a 2006-01-01 (grupo MINVALUE), itens com datas em ou após 2006-01-01 (grupo 2006-01-01) e itens sem data (grupo **NULL).**

Dentro de cada grupo, os resultados são classificação pelos valores na coluna GROUP ON por padrão. A cláusula [ORDER BY](-search-sql-orderby.md) opcional pode conter um especificador de direção de ASC para crescente (baixo para alto) ou DESC para decrescente (de alto a baixo) e a cláusula ORDER IN [GROUP BY](-search-sql-orderingroup.md) pode ordenar cada grupo usando regras diferentes. Confira a [seção Grupos de Pedidos](#ordering-groups) abaixo para obter mais informações.

## <a name="group-ranges"></a>Intervalos de grupo

A tabela a seguir demonstra como os resultados são divididos em grupos com base nos limites de intervalo:



| Exemplo ( &lt; &gt; \[ intervalos de grupo de colunas \] )        | Result                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System.Size \[ 1000, 5000\]                       | Os resultados são agrupados em quatro buckets: **MINVALUE:** tamanho < 1000<br/> **1000:** 1000 <= Tamanho < 5000<br/> **5000:** Tamanho >= 5000<br/> **NULL:** Nenhum valor para Tamanho<br/>                                                                      |
| System.Author \[ BEFORE('m'),AFTER('r')\]         | Os resultados são agrupados em quatro buckets: **MINVALUE: <** caractere antes de "m"<br/> **m:** character before "m" <= Author < character after "r"<br/> **r:** caractere após "r" <= Autor<br/> **NULL:** Nenhum valor para Autor<br/>      |
| System.Author \[ MINVALUE/'a to l',"m"/'m to z'\] | Os resultados são agrupados em três buckets: **a a l:** Author < "m"<br/> **m a z:** "m" <= Autor <br/> **NULL:** Nenhum valor para Autor<br/>                                                                                                               |
| System.DateCreated \[ '2005-1-01','2006-6-01'\]   | Os resultados são agrupados em quatro buckets:<br/> **MINVALUE:** DateCreated < 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated >= 2006-6-01<br/> **NULL:** Nenhum valor para DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Incorreto: `GROUP ON System.Author['m','z','a']`
>
> Correto: `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Rotulando grupos

Para melhorar a leitura, você pode rotular grupos usando a seguinte sintaxe:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



O rótulo é separado do limite de intervalo com uma barra e é entre aspas simples. Se você não especificar um rótulo, o nome do grupo será a cadeia de caracteres de limite de intervalo.

Veja a seguir um exemplo de rotulagem de grupos:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



No Windows 7 ou posterior, você também pode usar um rótulo OTHER genérico \[ \] para combinar vários intervalos de grupo. Os resultados de todos os grupos identificados com esse rótulo serão combinados em um grupo com esse rótulo. Esse grupo de resultados é retornado após todos os outros grupos, exceto pelo **grupo NULL.** O **grupo NULL** contém resultados para itens que não têm um valor para a propriedade especificada. Antes de Windows 7, \[ o rótulo OTHER é tratado como qualquer outro rótulo de \] grupo.

O código a seguir é um exemplo de uso do rótulo OTHER para grupos que seriam criados \[ \] no Windows 7 ou posterior:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



A tabela a seguir mostra os grupos que seriam criados pelo código de grupo anterior no Windows 7 ou posterior.



| Grupo     | System.Author | System.FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Rainha         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| S         | Zara          | amet.docx       |
| \[OUTROS\] | Abner         | nonummy.docx    |
|           | Roberto           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Ordenando grupos

Há três maneiras de ordenar itens em grupos:

-   Ordenação padrão: se você não especificar o contrário, os resultados serão ordenados pelos valores na coluna GROUP ON, em ordem crescente.
-   ORDER BY: você pode especificar a ordem decrescente em uma cláusula ORDER BY. Você deve ordenar os resultados pela coluna GROUP ON.
-   ORDER IN GROUP BY: você pode especificar uma ordem diferente para cada grupo. Se você agrupar [em System.Kind](../properties/props-system-kind.md), poderá solicitar documentos por [System.Author](../properties/props-system-author.md) e música por [System.Music.Artist.](../properties/props-system-music-artist.md)

Para obter mais informações sobre como ordenar resultados, consulte as [páginas de referência Cláusula ORDER BY](-search-sql-orderby.md) e ORDER IN GROUP [Clause.](-search-sql-orderingroup.md)

## <a name="nesting-groups"></a>Aninhando grupos

Você pode aninhar grupos com várias cláusulas GROUP ON. A ordem especificada na consulta é refletida diretamente na hierarquia do grupo de saída, conforme mostrado no exemplo a seguir.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System.Kind    | System.Author | System.DateCreated |
|----------------|---------------|--------------------|
| documentos      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| comunicações | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Agrupando em propriedades de vetor

Agrupar em propriedades de vetor, propriedades que podem conter um ou mais valores simultaneamente, compara os valores de vetor individualmente por padrão. Por exemplo, se houver um documento, Lorem.docx, com a propriedade System.Author como "Protocol; E outro documento, Ipsum.docx, com a propriedade System.Author como "Euclid", a consulta retorna o conjunto de resultados em dois grupos, conforme mostrado aqui:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System.FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Como você pode ver, o agrupamento em propriedades de vetor retorna linhas duplicadas. Lorem.docx aparece duas vezes porque tem dois autores.

 

## <a name="more-examples"></a>Mais exemplos


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de agregação](-search-sql-aggregates.md)
</dt> <dt>

[Cláusula ORDER BY](-search-sql-orderby.md)
</dt> <dt>

[Cláusula ORDER IN GROUP](-search-sql-orderingroup.md)
</dt> </dl>

 

 
