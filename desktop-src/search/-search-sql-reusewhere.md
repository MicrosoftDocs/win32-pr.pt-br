---
description: A cláusula WHERE em uma consulta especifica um conjunto de itens para corresponder aos resultados.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Função ReuseWhere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f073a7ac0d5faf5973d08ff53ccebdacf8bead080a53e2d9a4a6ae9ed5724db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944655"
---
# <a name="reusewhere-function"></a>Função ReuseWhere

A [cláusula WHERE](-search-sql-where.md) em uma consulta especifica um conjunto de itens para corresponder aos resultados. As consultas subsequentes podem compartilhar o trabalho executado para uma consulta anterior usando a função ReuseWhere em uma nova cláusula WHERE de consulta. As consultas que aproveitam essa função são executadas mais rapidamente.

## <a name="examples"></a>Exemplos

O cenário a seguir mostra como usar a função ReuseWhere:

1.  Em seguida, você emitirá a seguinte consulta:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  No conjuntos de linhas retornado, você obterá [um Where ID](-search-sql-rowset-properties.md), *Query1WhereID.*

    A ID em que é uma propriedade de conjuntos de linhas com PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8 e tipo UI4.

3.  Emito uma segunda consulta com a função ReuseWhere, passando *a Query1WhereID* da etapa 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

A segunda consulta é equivalente à seguinte:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



A função ReuseWhere pode ser usada em algum lugar na [cláusula WHERE.](-search-sql-where.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Propriedades do conjunto de linhas](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



