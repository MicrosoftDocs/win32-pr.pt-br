---
title: Tempo de tempo de pesquisa
description: Um cliente também pode impor um limite de tempo que aguardará um servidor retornar o conjunto de resultados.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- ADSI de tempo de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99b287c1bc0ba0da5e39b579c4a454eae821cf2c443930a5ae0376412e2c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082300"
---
# <a name="search-time-out"></a>Tempo de tempo de pesquisa

Um cliente também pode impor um limite de tempo que aguardará um servidor retornar o conjunto de resultados. O valor da opção "tempo limite da pesquisa" especifica esse limite. Quando o servidor não responder a uma consulta dentro do período de tempo especificado, o cliente poderá interromper a pesquisa e tentar novamente mais tarde.

A propriedade de tempo-out é útil quando um cliente solicita uma pesquisa assíncrona. Em uma pesquisa assíncrona, o cliente faz uma solicitação e, em seguida, continua com outras tarefas enquanto aguarda o servidor retornar os resultados. É possível que o servidor possa ficar offline sem notificar o cliente. Nesse caso, o cliente não tem como reconhecer que o servidor ainda está processando a consulta ou se ele não tem como estar em tempo de vida. A propriedade time-out fornece ao cliente algum controle em tais instâncias.

Para obter mais informações sobre como usar a opção de tempo-out de pesquisa com uma interface de pesquisa específica, consulte:

-   [Limite de tempo do cliente com IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Pesquisando com objetos ActiveX dados](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




