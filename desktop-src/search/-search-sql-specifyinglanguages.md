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
# <a name="specifying-languages"></a><span data-ttu-id="ada66-103">Especificando idiomas</span><span class="sxs-lookup"><span data-stu-id="ada66-103">Specifying Languages</span></span>

<span data-ttu-id="ada66-104">Você pode especificar o idioma usado em consultas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ada66-104">You can specify the language used in search queries.</span></span> <span data-ttu-id="ada66-105">Os predicados FREETEXT e CONTAINS na cláusula WHERE dão suporte à especificação de um idioma.</span><span class="sxs-lookup"><span data-stu-id="ada66-105">Both the FREETEXT and CONTAINS predicates in the WHERE clause support specifying a language.</span></span> <span data-ttu-id="ada66-106">Você pode indicar a linguagem de consulta fornecendo um LCID (identificador de código de idioma numérico) no predicado CONTAINS ou FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="ada66-106">You can indicate the query language by providing a numeric language code identifier (LCID) in the CONTAINS or FREETEXT predicate.</span></span> <span data-ttu-id="ada66-107">Esse LCID especifica qual separador de palavras usar para analisar a cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="ada66-107">This LCID specifies which word breaker to use to parse the query string.</span></span> <span data-ttu-id="ada66-108">Ela usa a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="ada66-108">It uses the following syntax:</span></span>


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



<span data-ttu-id="ada66-109">Para obter mais informações, consulte a sintaxe dos predicados [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ada66-109">For more information, see the syntax for the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates.</span></span>

 

 



