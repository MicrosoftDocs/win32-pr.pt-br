---
description: Uma função de agregação executa um cálculo em um conjunto de valores e retorna um valor . Isso possibilita gerar estatísticas resumidas para grupos de vários níveis com pouca sobrecarga.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funções de Agregação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d504a9343116bc23e847728716eeaa79fc2d26d993e962dd81ccd43669e22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094947"
---
# <a name="aggregate-functions"></a>Funções de Agregação

Uma função de agregação executa um cálculo em um conjunto de valores e retorna um valor . Isso possibilita gerar estatísticas resumidas para grupos de vários níveis com pouca sobrecarga.

## <a name="about-aggregate-functions"></a>Sobre funções de agregação

As funções de agregação Windows Search linguagem SQL (SQL) têm a seguinte sintaxe:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



A parte da função pode incluir qualquer uma das seguintes funções e sintaxe:



| Função                                                              | Descrição                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVG( <column> )                                                   | Retorna a média dos valores em um grupo. Aplica-se somente a números.                                                                                                                                      |
| BYFREQUENCY( <column> , <N> )                                | Retorna os valores de coluna N mais frequentes dos resultados no grupo. Também inclui uma contagem de quantas vezes cada valor ocorreu e identificadores de documento para resultados que contêm cada valor retornado. |
| CHILDCOUNT()                                                          | Retorna o número de itens em um grupo (excluindo subgrupos). Se houver vários níveis de agrupamento, isso retornará o número de grupos filho imediatos.                                                  |
| COUNT()                                                               | Retorna o número de itens em um grupo e todos os subgrupos.                                                                                                                                                   |
| DATERANGE( <column> )                                             | Retorna os limites inferior e superior dos valores de coluna encontrados no grupo de resultados do grupo. Válido somente para propriedades de tempo de arquivo.                                                                               |
| FIRST( <column> , <N> )                                      | Retorna os primeiros valores de coluna N dos resultados folha encontrados em um grupo.                                                                                                                                       |
| MAX( <column> )                                                   | Retorna o valor máximo na expressão. Aplica-se somente a números ou datas.                                                                                                                              |
| MIN( <column> )                                                   | Retorna o valor mínimo na expressão. Aplica-se somente a números ou datas.                                                                                                                              |
| REPRESENTATIVEOF( <column> , <idRepresentative> , <N> ) | Retorna valores N idRepresentative, cada um selecionado de um dos subconjunto de resultados que tem um valor de coluna exclusivo. Cada valor também é retornado com um identificador de documento que tem o valor idRepresentative. |
| SUM( <column> )                                                   | Retorna a soma dos valores em um grupo. Aplica-se somente a números.                                                                                                                                          |



 

 

> [!Note]  
> As agregações são retornadas como colunas individuais. Eles são principalmente tipos simples, exceto ByFrequency, First, DateRange e RepresentativeOf, que são retornados como tipos compostos.

 

Você pode usar qualquer coluna numérica ou de data para as agregação e não apenas aquelas que estão na cláusula SELECT. No entanto, você não pode agrupar agregações. Um erro de sintaxe será retornado se o argumento de coluna passado não for um tipo numérico ou de data.

A parte do rótulo é opcional e fornece um alias mais acessível para o rótulo. Se você não incluir um rótulo de alias, Windows Search transformará a função e o nome da coluna em um rótulo. Por exemplo, MAX(System.Document. WordCount) torna-se MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Grupos e contagem de vários níveis

As agregações são definidas em folhas e duplicadas. Uma agregação assume como entrada as folhas do grupo que a define (documentos), em vez dos subgrupos de seus filhos. Essa funcionalidade é conhecida como agrupamento de vários níveis.

Além das agregações que estão sendo definidas em folhas e duplicadas, elas são contadas apenas uma vez. Embora o mesmo documento possa ser representado várias vezes em um grupo, as agregações só o considerariam uma vez. O gráfico a seguir ilustra esse conceito.

![diagrama mostrando que as agregações são definidas sobre folhas e duplicadas e são contadas apenas uma vez](images/aggregates.png)

## <a name="aggregate-examples"></a>Exemplos de agregação

Veja a seguir exemplos de funções de agregação dentro da cláusula GROUP ON:


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a>Valor Retornado

O valor de retorno é uma variante encontrada no conjunto de linhas como uma propriedade personalizada, como os aliases especificados ou como "Agregações" se nenhum rótulo de alias for especificado.

 

 



