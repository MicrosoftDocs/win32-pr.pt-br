---
description: Os resultados de uma consulta incluem as linhas retornadas pela consulta e um valor de classificação para cada linha se a coluna de classificação for incluída na cláusula SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: CLASSIFICAR por cláusula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164334"
---
# <a name="rank-by-clause"></a>CLASSIFICAR por cláusula

Os resultados de uma consulta incluem as linhas retornadas pela consulta e um valor de classificação para cada linha se a coluna de classificação for incluída na cláusula SELECT. Os valores de classificação são calculados pelo mecanismo de pesquisa e retornados como inteiros no intervalo de zero a 1000. Para tornar os resultados da classificação mais significativos, a consulta pode controlar como os valores de classificação brutos são calculados na cláusula RANK BY.

Este tópico é organizado da seguinte maneira:

-   [CLASSIFICAR por cláusula](#rank-by-clause)
-   [Função WEIGHT](#weight-function)
-   [Função de COERÇÃO](#coercion-function)

## <a name="rank-by-clause"></a>CLASSIFICAR por cláusula

A sintaxe para a cláusula RANK BY é a seguinte:


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



A cláusula de classificação por é aplicada ao critério de pesquisa \_ imediatamente antes, especificando efetivamente uma classificação inferior ou superior para linhas retornadas por esse critério de pesquisa do que as linhas retornadas por outra condição de pesquisa. Os parênteses em torno da \_ condição de pesquisa são obrigatórios. Os parênteses em torno da especificação de classificação são opcionais.

Mais de uma cláusula de classificação por pode ser aplicada a uma única condição. Você pode incluir mais CLASSIFICAções por cláusulas uma após a outra usando parênteses.

> [!Note]  
> Predicados de texto completo retornam valores de classificação no intervalo de 0 a 1000. Os valores de classificação para todos os documentos correspondidos por um predicado de texto não completo são 1000. As modificações nos valores de classificação devem levar essas informações em conta.

 

A \_ parte de especificação de classificação da cláusula RANKBY identifica uma ou mais funções a serem aplicadas aos valores de classificação. A função WEIGHT aplica um multiplicador ao valor de classificação bruta para uma linha retornada. Quanto menor o multiplicador, menor o valor de classificação resultante. A função de COERÇÃO pode ser usada para multiplicar, adicionar ou definir um valor de classificação específico para uma linha retornada. Cada especificação de classificação pode incluir zero ou uma função de peso e zero ou mais funções de COERÇÃO. Se as funções de peso e COERÇÃO forem incluídas em uma cláusula de classificação por, a função de peso deverá ser a primeira.

## <a name="weight-function"></a>Função WEIGHT

A sintaxe da função WEIGHT é:


```
WEIGHT ( <weight_multipler> ) 
```



O multiplicador deve ser um decimal de 0, 1 a 1, 0. O valor de classificação bruta retornado pelo predicado de critério de pesquisa é multiplicado pelo multiplicador de peso para definir um novo valor de classificação.

No exemplo a seguir, a função WEIGHT fornece documentos com a palavra "Theresa" no System.Document. Campo LastAuthor metade do valor de classificação de documentos com "Theresa" no campo System. Author:


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Os recursos de ponderação de coluna de predicado CONTAINS e FREETEXT dão suporte a um formato abreviado usando dois pontos entre o termo de pesquisa e o multiplicador ("software": 0,25). A cláusula de classificação por não oferece suporte à forma abreviada.

 

Há uma limitação ao usar RANK por peso: ela não funciona com cláusulas CONTAINS que usam condições booleanas; por exemplo, o exemplo a seguir não é permitido:


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Função de COERÇÃO

A função de coerção de classificação pode ser usada para alterar o valor de classificação retornado por adição ou multiplicação ou atribuindo a ele um valor específico.

A sintaxe da função de COERÇÃO é:


```
COERCION ( <coercion_operation> , <coercion_value> )
```



O valor de coerção é um valor inteiro.

A tabela a seguir descreve as configurações de operação de coerção disponíveis.



| Operação de coerção | Descrição                                                                                    | Intervalo de valor  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | O valor de classificação retornado é o valor especificado no valor de coerção.                          | 0 a 1000    |
| ADD                | O valor de classificação retornado é a soma do valor de classificação bruta e o valor de coerção especificado.     | 0, 1 a 1,0 |
| MULTIPLY           | O valor de classificação retornado é o produto do valor de classificação bruta e o valor de coerção especificado. | 0, 1 a 1,0 |



 

 

> [!IMPORTANT]
> A pesquisa pode retornar valores de classificação somente no intervalo de 0 a 1000.

 

 

O exemplo a seguir usa a função de COERÇÃO para definir todos os documentos com "computador" no título para ter uma classificação de 1000, enquanto reduz por um trimestre a classificação de documentos que contém "computador" e "software" no título.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



