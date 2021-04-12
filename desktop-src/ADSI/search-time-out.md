---
title: Tempo limite de pesquisa
description: Um cliente também pode impor um limite de tempo que aguardará que um servidor retorne o conjunto de resultados.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- ADSI de tempo limite de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291779"
---
# <a name="search-time-out"></a>Tempo limite de pesquisa

Um cliente também pode impor um limite de tempo que aguardará que um servidor retorne o conjunto de resultados. O valor da opção "tempo limite de pesquisa" especifica esse limite. Quando o servidor não responde a uma consulta dentro do período de tempo especificado, o cliente pode interromper a pesquisa e tentar novamente mais tarde.

A propriedade de tempo limite é útil quando um cliente solicita uma pesquisa assíncrona. Em uma pesquisa assíncrona, o cliente faz uma solicitação e prossegue com outras tarefas enquanto aguarda o servidor retornar os resultados. É possível que o servidor possa ficar offline sem notificar o cliente. Nesse caso, o cliente não tem como reconhecer que o servidor ainda está processando a consulta, ou se ele parou de ser dinâmico. A propriedade de tempo limite fornece ao cliente algum controle nessas instâncias.

Para obter mais informações sobre como usar a opção de tempo limite de pesquisa com uma interface de pesquisa específica, consulte:

-   [Limite de tempo do cliente com IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




