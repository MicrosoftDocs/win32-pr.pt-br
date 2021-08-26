---
description: O predicado NULL indica se o documento tem um valor para a coluna indicada.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicado nulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058116"
---
# <a name="null-predicate"></a>Predicado nulo

O predicado **NULL** indica se o documento tem um valor para a coluna indicada.

O predicado **NULL** tem a seguinte sintaxe:


```
...WHERE <column> IS [NOT] NULL
```



A palavra-chave NOT opcional nega o resultado. A coluna pode ser um [identificador](-search-sql-identifiers.md)regular ou delimitado.

> [!IMPORTANT]
> Para testar se uma coluna tem o valor **nulo** , você deve usar o predicado **NULL** . Não é válido usar o valor **nulo** em um predicado de comparação. "Onde a coluna é **nula**" está correta. "WHERE Column = **NULL**" não é válido.

 

## <a name="example"></a>Exemplo

O exemplo a seguir retorna documentos que não têm um valor de System. video. director.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Predicado LIKE](-search-sql-like.md)
</dt> <dt>

[Comparação de valor literal](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparações de vários valores (matriz)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados de texto não completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



