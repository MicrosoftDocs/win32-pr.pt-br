---
description: 'Saiba mais sobre: cláusula ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Cláusula ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090064"
---
# <a name="order-by-clause"></a>Cláusula ORDER BY

A cláusula ORDER BY classifica os resultados com base no valor de uma ou mais colunas que você especificar. A seguir, a sintaxe da cláusula ORDER BY:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



O especificador de coluna deve ser uma coluna válida. Você pode usar o especificador de coluna para fazer referência a colunas pela ordem em que elas aparecem na consulta. A primeira coluna na consulta é numerada 1. Você pode incluir mais de uma coluna na cláusula ORDER BY, separada por vírgulas.

O especificador de direção opcional pode ser "ASC" para crescente (baixo para alto) ou "DESC" para decrescente (alto para baixo). Se você não fornecer um especificador de direção, o padrão, Ascending, será usado. Se você especificar mais de uma coluna, mas não especificar todas as direções, a direção especificada por último será aplicada a cada coluna até que você altere explicitamente a direção.

Por exemplo, na cláusula ORDER BY a seguir, as colunas A, B, C e G são classificadas em ordem crescente, enquanto as colunas D, E e F são classificadas em ordem decrescente.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Cláusula FROM](-search-sql-from.md)
</dt> <dt>

[CLASSIFICAR por cláusula](-search-sql-rankby.md)
</dt> <dt>

[Instrução SELECT](-search-sql-select.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



