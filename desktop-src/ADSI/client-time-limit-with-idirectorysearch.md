---
title: Limite de tempo do cliente com IDirectorySearch
description: Um cliente pode impor um limite de tempo para um servidor retornar o conjunto de resultados. Quando o servidor não responde a uma consulta dentro do período de tempo especificado, o cliente pode abandonar a pesquisa e tentar novamente mais tarde.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite de tempo do cliente com IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, limite de tempo do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755869"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Limite de tempo do cliente com IDirectorySearch

Um cliente pode impor um limite de tempo para um servidor retornar o conjunto de resultados. Quando o servidor não responde a uma consulta dentro do período de tempo especificado, o cliente pode abandonar a pesquisa e tentar novamente mais tarde.

A preferência de limite de tempo do cliente é útil quando um cliente solicita uma pesquisa assíncrona. Em uma pesquisa assíncrona, o cliente faz uma solicitação e prossegue com outras tarefas enquanto aguarda o servidor retornar os resultados. É possível que o servidor possa ficar offline sem notificar o cliente. Nesse caso, o cliente não terá nenhuma notificação se o servidor ainda estiver processando a consulta ou se ele não estiver mais ativo. A preferência de limite de tempo do cliente fornece ao cliente algum controle de situações como essa.

O padrão para o limite de tempo do cliente é sem limite. Para definir um limite de tempo do cliente, defina uma opção de pesquisa de **\_ \_ tempo limite do ADS SEARCHPREF** com um valor **\_ inteiro ADSTYPE** que contenha o limite de tempo do cliente, em segundos, na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Um limite de tempo de cliente igual A zero indica que não há limite de tempo.

O exemplo de código a seguir mostra como definir o limite de tempo do cliente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




