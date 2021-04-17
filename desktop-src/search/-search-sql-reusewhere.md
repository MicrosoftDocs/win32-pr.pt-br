---
description: A cláusula WHERE em uma consulta especifica um conjunto de itens aos quais os resultados são correspondidos.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Função ReuseWhere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784596"
---
# <a name="reusewhere-function"></a>Função ReuseWhere

A cláusula [Where](-search-sql-where.md) em uma consulta especifica um conjunto de itens aos quais os resultados são correspondidos. As consultas subsequentes podem compartilhar o trabalho executado para uma consulta anterior usando a função ReuseWhere em uma nova cláusula WHERE de consulta. As consultas que tiram proveito dessa função são executadas mais rapidamente.

## <a name="examples"></a>Exemplos

O cenário a seguir mostra como usar a função ReuseWhere:

1.  Você emite a seguinte consulta:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  No conjunto de linhas retornado, você obtém uma [id where](-search-sql-rowset-properties.md), *Query1WhereID*.

    A ID WHERE é uma propriedade Rowset com PROPset {aa6ee6b0-e828-11D0-B2-3E-00-AA-00-47-FC-01}, PROPID 8 e Type UI4.

3.  Você emite uma segunda consulta com a função ReuseWhere, passando o *Query1WhereID* da etapa 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

A segunda consulta é equivalente à seguinte:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



A função ReuseWhere pode ser usada como na cláusula [Where](-search-sql-where.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Propriedades do conjunto de linhas](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



