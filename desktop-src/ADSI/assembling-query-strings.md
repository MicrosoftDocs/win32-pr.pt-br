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
# <a name="assembling-query-strings"></a>Montando cadeias de consulta

No Active Directory, o uso de critérios de filtragem específicos pode aumentar o desempenho da pesquisa. Isso ocorre porque Active Directory avalia todos os predicados, identifica os índices e, em seguida, seleciona um índice que provavelmente produzirá o menor conjunto de valores retornados.

Evite Pesquisar texto no meio ou no final de uma cadeia de caracteres, por exemplo, "CN = \* Hill \* " ou "CN = \* Larouse".

Quando possível, procure atributos indexados. Os atributos indexados são armazenados em todos os controladores de domínio, de modo que a consulta provavelmente será mais rápida do que pesquisar um atributo não indexado.

 

 




