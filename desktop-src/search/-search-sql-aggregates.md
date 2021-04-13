---
description: Uma função de agregação executa um cálculo em um conjunto de valores e retorna um valor. Isso torna possível gerar estatísticas de resumo para grupos de vários níveis com pouca sobrecarga.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funções de Agregação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555294"
---
# <a name="aggregate-functions"></a>Funções de Agregação

Uma função de agregação executa um cálculo em um conjunto de valores e retorna um valor. Isso torna possível gerar estatísticas de resumo para grupos de vários níveis com pouca sobrecarga.

## <a name="about-aggregate-functions"></a>Sobre funções de agregação

As funções de agregação no Windows Search linguagem SQL (SQL) têm a seguinte sintaxe:


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



A parte da função pode incluir qualquer uma das seguintes funções e sintaxe:



| Função                                                              | Descrição                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Méd ( <column> )                                                   | Retorna a média dos valores em um grupo. Aplica-se somente a números.                                                                                                                                      |
| BYFREQUENCY ( <column> , <N> )                                | Retorna os valores de N colunas mais frequentes dos resultados no grupo. Também inclui uma contagem de quantas vezes cada valor ocorreu e os identificadores de documento para resultados que contêm cada valor retornado. |
| CHILDCOUNT ()                                                          | Retorna o número de itens em um grupo (excluindo subgrupos). Se houver vários níveis de agrupamento, isso retornará o número de grupos filho imediatos.                                                  |
| CONTAGEM ()                                                               | Retorna o número de itens em um grupo e todos os subgrupos.                                                                                                                                                   |
| DATERANGE ( <column> )                                             | Retorna os limites inferior e superior dos valores de coluna encontrados no grupo de resultados de grupo. Válido somente para propriedades FILETIME.                                                                               |
| PRIMEIRO ( <column> , <N> )                                      | Retorna os primeiros N valores de coluna dos resultados folha encontrados em um grupo.                                                                                                                                       |
| MÁX. ( <column> )                                                   | Retorna o valor máximo na expressão. Aplica-se somente a números ou datas.                                                                                                                              |
| MIN ( <column> )                                                   | Retorna o valor mínimo na expressão. Aplica-se somente a números ou datas.                                                                                                                              |
| REPRESENTATIVEOF ( <column> , <idRepresentative> , <N> ) | Retorna N valores idRepresentative, cada um deles selecionado de um dos subconjuntos de resultados que tem um valor de coluna exclusivo. Cada valor também é retornado com um identificador de documento que tem o valor idRepresentative. |
| SUM ( <column> )                                                   | Retorna a soma dos valores em um grupo. Aplica-se somente a números.                                                                                                                                          |



 

 

> [!Note]  
> As agregações são retornadas como colunas individuais. Eles são, na maioria das vezes, tipos simples, exceto ByFrequency, First, DateRange e RepresentativeOf, que são retornados como tipos compostos.

 

Você pode usar qualquer coluna numérica ou de data para agregações, e não apenas aquelas que estão na cláusula SELECT. No entanto, você não pode agrupar em agregações. Um erro de sintaxe será retornado se o argumento de coluna passado não for um tipo numérico ou de data.

A parte do rótulo é opcional e fornece um alias mais legível para o rótulo. Se você não incluir um rótulo de alias, o Windows Search transformará a função e o nome da coluna em um rótulo. Por exemplo, MAX (System.Document. WordCount) torna-se MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Grupos e contagens de vários níveis

As agregações são definidas em folhas e duplicadas. Uma agregação usa como entrada as folhas do grupo que as define (documentos), em vez dos subgrupos de seus filhos. Essa funcionalidade é conhecida como agrupamento de vários níveis.

Além de agregações sendo definidas em todas as folhas e duplicadas, elas são contadas apenas uma vez. Embora o mesmo documento possa ser representado várias vezes em um grupo, as agregações só o consideram uma vez. O gráfico a seguir ilustra esse conceito.

![diagrama mostrando que as agregações são definidas em folhas e duplicadas, e são contadas apenas uma vez](images/aggregates.png)

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

O valor de retorno é uma variante encontrada no conjunto de linhas como uma propriedade personalizada, seja como os aliases especificados ou como "agregações" se nenhum rótulo de alias for especificado.

 

 



