---
title: Montando cadeias de consulta
description: No Active Directory, o uso de critérios de filtragem específicos pode aumentar o desempenho da pesquisa. Isso ocorre porque Active Directory avalia todos os predicados, identifica os índices e, em seguida, seleciona um índice que provavelmente produzirá o menor conjunto de valores retornados.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Montando cadeias de caracteres de consulta ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56dec34f63a4a3e12385a36ad5fe5339a0f3d9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755739"
---
# <a name="assembling-query-strings"></a><span data-ttu-id="5abee-105">Montando cadeias de consulta</span><span class="sxs-lookup"><span data-stu-id="5abee-105">Assembling Query Strings</span></span>

<span data-ttu-id="5abee-106">No Active Directory, o uso de critérios de filtragem específicos pode aumentar o desempenho da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5abee-106">In Active Directory, using specific filtering criteria can boost search performance.</span></span> <span data-ttu-id="5abee-107">Isso ocorre porque Active Directory avalia todos os predicados, identifica os índices e, em seguida, seleciona um índice que provavelmente produzirá o menor conjunto de valores retornados.</span><span class="sxs-lookup"><span data-stu-id="5abee-107">This is because Active Directory evaluates all predicates, identifies the indices, and then selects one index likely to yield the smallest set of returned values.</span></span>

<span data-ttu-id="5abee-108">Evite Pesquisar texto no meio ou no final de uma cadeia de caracteres, por exemplo, "CN = \* Hill \* " ou "CN = \* Larouse".</span><span class="sxs-lookup"><span data-stu-id="5abee-108">Avoid searching for text in the middle or the end of a string, for example, "cn=\*hille\*" or "cn=\*larouse".</span></span>

<span data-ttu-id="5abee-109">Quando possível, procure atributos indexados.</span><span class="sxs-lookup"><span data-stu-id="5abee-109">When possible, search for indexed attributes.</span></span> <span data-ttu-id="5abee-110">Os atributos indexados são armazenados em todos os controladores de domínio, de modo que a consulta provavelmente será mais rápida do que pesquisar um atributo não indexado.</span><span class="sxs-lookup"><span data-stu-id="5abee-110">Indexed attributes are stored on all domain controllers, so the query will most likely be faster than searching for a non-indexed attribute.</span></span>

 

 




