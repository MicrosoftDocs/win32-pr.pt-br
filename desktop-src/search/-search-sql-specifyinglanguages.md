---
description: Você pode especificar o idioma usado em consultas de pesquisa.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Especificando idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501464"
---
# <a name="specifying-languages"></a>Especificando idiomas

Você pode especificar o idioma usado em consultas de pesquisa. Os predicados FREETEXT e CONTAINS na cláusula WHERE dão suporte à especificação de um idioma. Você pode indicar a linguagem de consulta fornecendo um LCID (identificador de código de idioma numérico) no predicado CONTAINS ou FREETEXT. Esse LCID especifica qual separador de palavras usar para analisar a cadeia de caracteres de consulta. Ela usa a seguinte sintaxe:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Para obter mais informações, consulte a sintaxe dos predicados [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) .

 

 



