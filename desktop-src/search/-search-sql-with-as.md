---
description: Aliases de grupo de colunas fornecem uma maneira de usar nomes mais curtos no lugar do nome de uma coluna ou de um grupo de colunas. O predicado de alias de grupo opcional faz parte da cláusula WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: WITH – Predicado de alias de grupo AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed77072c83d1c28dcc3ec63396b46a21a57c4a97d9c6dcd70259bd861d19762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226729"
---
# <a name="with----as-group-alias-predicate"></a>WITH – Predicado de alias de grupo AS

Aliases de grupo de colunas fornecem uma maneira de usar nomes mais curtos no lugar do nome de uma coluna ou de um grupo de colunas. O predicado de alias de grupo opcional faz parte da cláusula WHERE. A sintaxe é a seguinte:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Você pode especificar mais de um alias de grupo, separando WITH... Predicados AS por vírgulas.

Quando um alias de grupo é referenciado em um predicado de cláusula WHERE, a condição é aplicada a cada coluna no grupo. Os valores lógicos resultantes da correspondência de cada coluna são combinados usando o operador **OR** lógico.

Um alias deve ser definido antes de poder ser usado e só pode ser usado dentro da cláusula WHERE. O nome do alias deve ser um identificador regular precedido por um sinal de quilo de peso necessário ( \# ).

O especificador de coluna pode conter um ou mais especificadores de coluna, separados por vírgulas. A lista de colunas deve ser entre parênteses e a ponderação pode ser atribuída a cada uma delas. Cada coluna tem a seguinte sintaxe:


```
<column_identifier> [<weight_assignment>]
```



Para obter informações sobre como especificar pesos de coluna, consulte [Predicado FREETEXT](-search-sql-freetext.md) e [Predicado CONTAINS](-search-sql-contains.md).

O identificador de coluna pode ser regular ou delimitado.

## <a name="examples"></a>Exemplos

Os exemplos de cláusula WHERE a seguir demonstram quando e como você pode usar o predicado de alias de grupo. O primeiro exemplo mostra uma cláusula WHERE mais repetitiva que não usa alias de grupo.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



O exemplo anterior pode ser simplificado usando um alias de grupo, conforme mostrado no exemplo a seguir.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



A seguir está um exemplo de ponderação positiva em que a **propriedade Title** recebe mais peso na determinação da classificação relativa.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



A seguir está um exemplo de ponderação negativa em que a **propriedade Title** com peso de 0 não é considerada.


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado FREETEXT](-search-sql-freetext.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que não são de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



