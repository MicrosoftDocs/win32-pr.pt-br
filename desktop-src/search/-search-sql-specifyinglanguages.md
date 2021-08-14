---
description: Você pode especificar o idioma usado em consultas de pesquisa.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Especificando idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ab2b5b5c5da4e9f71e49330d966895415467a671289bd4f5607e1265d22a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226811"
---
# <a name="specifying-languages"></a>Especificando idiomas

Você pode especificar o idioma usado em consultas de pesquisa. Os predicados FREETEXT e CONTAINS na cláusula WHERE dão suporte à especificação de um idioma. Você pode indicar a linguagem de consulta fornecendo um LCID (identificador de código de idioma numérico) no predicado CONTAINS ou FREETEXT. Esse LCID especifica qual separador de palavras usar para analisar a cadeia de caracteres de consulta. Ela usa a seguinte sintaxe:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Para obter mais informações, consulte a sintaxe dos predicados [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) .

 

 



