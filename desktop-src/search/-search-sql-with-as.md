---
description: Os aliases de grupo de colunas fornecem uma maneira de usar nomes mais curtos no lugar do nome de uma coluna ou de um grupo de colunas. O predicado de alias de grupo opcional faz parte da cláusula WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: Como predicado de alias de grupo--AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646866"
---
# <a name="with----as-group-alias-predicate"></a>Como predicado de alias de grupo--AS

Os aliases de grupo de colunas fornecem uma maneira de usar nomes mais curtos no lugar do nome de uma coluna ou de um grupo de colunas. O predicado de alias de grupo opcional faz parte da cláusula WHERE. A sintaxe a seguir:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Você pode especificar mais de um alias de grupo, separando o com... COMO predicados por vírgulas.

Quando um alias de grupo é referenciado em um predicado de cláusula WHERE, a condição é aplicada a cada coluna no grupo. Os valores lógicos resultantes da correspondência de cada coluna são combinados usando o operador **or** lógico.

Um alias deve ser definido antes que possa ser usado e pode ser usado somente dentro da cláusula WHERE. O nome do alias deve ser um identificador regular precedido por um sinal de sustenido necessário ( \# ).

O especificador de coluna pode conter um ou mais especificadores de coluna, separados por vírgulas. A lista de colunas deve ser colocada entre parênteses e o peso pode ser atribuído a cada uma delas. Cada coluna tem a seguinte sintaxe:


```
<column_identifier> [<weight_assignment>]
```



Para obter informações sobre como especificar pesos de coluna, consulte [predicado FREETEXT](-search-sql-freetext.md) e [contém predicado](-search-sql-contains.md).

O identificador de coluna pode ser regular ou delimitado.

## <a name="examples"></a>Exemplos

Os exemplos de cláusula WHERE a seguir demonstram quando e como você pode usar o predicado de alias de grupo. O primeiro exemplo mostra uma cláusula WHERE mais repetitiva que não usa a alias de grupo.


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



Veja a seguir um exemplo de peso positivo em que a propriedade **title** recebe mais peso na determinação da classificação relativa.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Veja a seguir um exemplo de peso negativo em que a propriedade **title** com peso de 0 não é considerada.


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

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



