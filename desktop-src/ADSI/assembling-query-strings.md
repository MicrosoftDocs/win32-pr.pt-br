---
title: Assembling Query Strings
description: No Active Directory, o uso de critérios de filtragem específicos pode aumentar o desempenho da pesquisa. Isso porque o Active Directory avalia todos os predicados, identifica os índices e, em seguida, seleciona um índice que provavelmente produzirá o menor conjunto de valores retornados.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Assembling Query Strings ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610ba78d6536d9cfe12f296fcbfa46d04cd572ae05cdb7d3bb8b0e1e7b5d32a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962186"
---
# <a name="assembling-query-strings"></a>Assembling Query Strings

No Active Directory, o uso de critérios de filtragem específicos pode aumentar o desempenho da pesquisa. Isso porque o Active Directory avalia todos os predicados, identifica os índices e, em seguida, seleciona um índice que provavelmente produzirá o menor conjunto de valores retornados.

Evite pesquisar texto no meio ou no final de uma cadeia de caracteres, por exemplo, "cn= \* montanhe" \* ou "cn= \* lação".

Quando possível, pesquise atributos indexados. Os atributos indexados são armazenados em todos os controladores de domínio, portanto, a consulta provavelmente será mais rápida do que procurar um atributo não indexado.

 

 




