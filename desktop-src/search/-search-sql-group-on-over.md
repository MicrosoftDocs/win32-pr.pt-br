---
description: O grupo em...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: AGRUPAR EM... SOBRE... Privacidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090067"
---
# <a name="group-on--over--statement"></a>AGRUPAR EM... SOBRE... Privacidade

O grupo em... SOBRE... a instrução retorna um conjunto de linhas hierárquico no qual os resultados da pesquisa são divididos em grupos com base em uma coluna especificada e intervalos de agrupamento opcionais. Se você agrupar na coluna [System. Kind](../properties/props-system-kind.md) , o conjunto de resultados será dividido em vários grupos: um para documentos, um para comunicações e assim por diante. Se você agrupar em [System. Size](../properties/props-system-size.md) e no intervalo de grupo 100 KB, o conjunto de resultados será dividido em três grupos: itens de tamanho < 100 KB, itens de tamanho >= 100 KB e itens sem valor de tamanho. Você também pode agregar agrupamentos com funções.

Este tópico aborda os seguintes assuntos:

-   [Sintaxe](#syntax)
-   [Intervalos de grupo](#group-ranges)
-   [Rotulando grupos](#labeling-groups)
-   [Grupos de pedidos](#ordering-groups)
-   [Aninhando grupos](#nesting-groups)
-   [Agrupamento em Propriedades de vetor](#grouping-on-vector-properties)
-   [Mais exemplos](#more-examples)
-   [Tópicos relacionados](#related-topics)

## <a name="syntax"></a>Syntax

O grupo em... SOBRE... a instrução tem a seguinte sintaxe:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



onde os intervalos de agrupamento são definidos da seguinte maneira:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



O grupo em <column> pode ser um [identificador](-search-sql-identifiers.md) regular ou delimitado para uma propriedade no repositório de propriedades.

O opcional <group ranges> é uma lista de um ou mais valores (número, data ou cadeia de caracteres) usados para dividir os resultados em grupos. O <range limit> identifica um ponto de divisão no conjunto de resultados retornado e <label> identifica um rótulo amigável para um grupo. Você pode dividir o conjunto de resultados em quantos grupos forem necessários.

O primeiro grupo de resultados inclui itens com o valor mínimo possível para a propriedade especificada até, mas não incluindo o primeiro limite de intervalo. Esse grupo pode ser referenciado com a palavra-chave MINVALUE. O segundo grupo pode ser referenciado com o especificador de limite de intervalo em si e inclui itens cujo valor da propriedade especificada é igual ou maior que o limite de intervalo. Todos os itens que não têm um valor para a propriedade especificada são retornados por último e podem ser referenciados com a palavra-chave **NULL** .

Por exemplo, um limite de intervalo de ' 2006-01-01 ' para a propriedade [System. DateCreated](../properties/props-system-datecreated.md) divide o conjunto de resultados em itens com datas anteriores a 2006-01-01 (grupo MinValue), itens com datas em ou após 2006-01-01 (grupo 2006-01-01) e itens sem data (grupo **nulo** ).

Dentro de cada grupo, os resultados são classificados pelos valores no grupo na coluna por padrão. A cláusula [order by](-search-sql-orderby.md) opcional pode conter um especificador de direção de ASC para crescente (baixo para alto) ou DESC para decrescente (alta para baixa) e a [ordem na cláusula Group by](-search-sql-orderingroup.md) pode ordenar cada grupo usando regras diferentes. Consulte a seção [grupos de pedidos](#ordering-groups) abaixo para obter mais informações.

## <a name="group-ranges"></a>Intervalos de grupo

A tabela a seguir demonstra como os resultados são divididos em grupos com base nos limites de intervalo:



| Exemplo ( <column> \[ intervalos de grupo \] )        | Resultado                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sistema. tamanho \[ 1000, 5000\]                       | Os resultados são agrupados em quatro buckets: **MinValue**: tamanho < 1000<br/> **1000:** 1000 <= tamanho < 5000<br/> **5000:** Tamanho >= 5000<br/> **Nulo:** Nenhum valor para o tamanho<br/>                                                                      |
| System. Author \[ antes (' M'), After (' r ')\]         | Os resultados são agrupados em quatro buckets: **MinValue:** autor < caractere antes de "m"<br/> **m:** caractere antes de "m" <= autor < caractere após "r"<br/> **r:** caractere após "r" <= autor<br/> **Nulo:** Nenhum valor para o autor<br/>      |
| System. Author \[ MinValue/' a para l ', "m"/m para z '\] | Os resultados são agrupados em três buckets: a **a l:** autor < "m"<br/> **m a z:** "m" <= autor <br/> **Nulo:** Nenhum valor para o autor<br/>                                                                                                               |
| System. DateCreated \[ ' 2005-1-01 ', ' 2006-6-01 '\]   | Os resultados são agrupados em quatro buckets:<br/> **MinValue:** DateCreated < 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated >= 2006-6-01<br/> **Nulo:** Nenhum valor para DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Incorreto `GROUP ON System.Author['m','z','a']`
>
> Corrigi `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Rotulando grupos

Para melhorar a legibilidade, você pode rotular grupos usando a seguinte sintaxe:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



O rótulo é separado do limite de intervalo com uma barra e é colocado entre aspas simples. Se você não especificar um rótulo, o nome do grupo será a cadeia de caracteres de limite de intervalo.

Veja a seguir um exemplo de como rotular grupos:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



No Windows 7 ou posterior, você também pode usar um \[ outro \] rótulo genérico para combinar vários intervalos de agrupamento. Os resultados de todos os grupos identificados com esse rótulo serão combinados em um grupo com este rótulo. Esse grupo de resultados é retornado após todos os outros grupos, exceto para o grupo **nulo** . O grupo **nulo** contém resultados para itens que não têm um valor para a propriedade especificada. Antes do Windows 7, o \[ outro \] rótulo é tratado como qualquer outro rótulo de grupo.

O código a seguir é um exemplo de como usar o \[ outro \] rótulo para grupos que seriam criados no Windows 7 ou posterior:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



A tabela a seguir mostra os grupos que seriam criados pelo código de Agrupamento anterior no Windows 7 ou posterior.



| Grupo     | System.Author | System. FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Dama         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| S         | Zara          | amet.docx       |
| \[OUTROS\] | Abner         | nonummy.docx    |
|           | Roberto           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Grupos de pedidos

Há três maneiras de ordenar itens em grupos:

-   Ordenação padrão: se você não especificar o contrário, os resultados serão ordenados pelos valores no grupo na coluna, em ordem crescente.
-   ORDENAr por: você pode especificar ordem decrescente em uma cláusula ORDER BY. Você deve ordenar os resultados pelo grupo na coluna.
-   ORDEM em Agrupar por: você pode especificar uma ordem diferente para cada grupo. Se você agrupar em [System. Kind](../properties/props-system-kind.md), poderá ordenar documentos por [System. Author](../properties/props-system-author.md) e música por [System. Music. artista](../properties/props-system-music-artist.md).

Para obter mais informações sobre como ordenar resultados, consulte as páginas de referência [ordem por cláusula](-search-sql-orderby.md) e [ordem nas cláusulas de grupo](-search-sql-orderingroup.md) .

## <a name="nesting-groups"></a>Aninhando grupos

Você pode aninhar grupos com várias cláusulas GROUP ON. A ordem especificada na consulta é refletida diretamente na hierarquia do grupo de saída, conforme mostrado no exemplo a seguir.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| Sistema. Kind    | System.Author | System. DateCreated |
|----------------|---------------|--------------------|
| documentos      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| comunicações | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Agrupamento em Propriedades de vetor

O agrupamento em Propriedades de vetor, propriedades que podem conter um ou mais valores simultaneamente, compara os valores de vetor individualmente por padrão. Por exemplo, se houver um documento, Lorem.docx, com a propriedade System. Author como "Theresa; Zara "e outro documento, Ipsum.docx, com a propriedade System. Author como" Zara ", a consulta retorna o conjunto de resultados em dois grupos, como mostrado aqui:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System. FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Como você pode ver, o agrupamento nas propriedades de vetor retorna linhas duplicadas. Lorem.docx aparece duas vezes porque tem dois autores.

 

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

 

 
