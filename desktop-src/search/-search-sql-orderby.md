---
description: 'Saiba mais sobre: Cláusula ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Cláusula ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3815ddecc659a47d7cf2c8547b49e878c54ba6bf8537e2589eea4441d9d3f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227180"
---
# <a name="order-by-clause"></a>Cláusula ORDER BY

A cláusula ORDER BY classifica os resultados com base no valor de uma ou mais colunas que você especificar. A seguir está a sintaxe da cláusula ORDER BY:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



O especificador de coluna deve ser uma coluna válida. Você pode usar o especificador de coluna para se referir às colunas pela ordem em que elas aparecem na consulta. A primeira coluna na consulta é numerada como 1. Você pode incluir mais de uma coluna na cláusula ORDER BY, separada por vírgulas.

O especificador de direção opcional pode ser "ASC" para crescente (baixo a alto) ou "DESC" para decrescente (de alto para baixo). Se você não fornecer um especificador de direção, o padrão, crescente, será usado. Se você especificar mais de uma coluna, mas não especificar todas as direções, a direção especificada por último será aplicada a cada coluna até que você altere explicitamente a direção.

Por exemplo, na cláusula ORDER BY a seguir, as colunas A, B, C e G são classificação em ordem crescente, enquanto as colunas D, E e F são classificação em ordem decrescente.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Cláusula FROM](-search-sql-from.md)
</dt> <dt>

[Cláusula RANK BY](-search-sql-rankby.md)
</dt> <dt>

[Instrução SELECT](-search-sql-select.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que não são de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



