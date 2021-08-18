---
title: Limite de tempo do cliente com IDirectorySearch
description: Um cliente pode impor um limite de tempo para um servidor retornar o conjunto de resultados. Quando o servidor não responder a uma consulta dentro do período de tempo especificado, o cliente poderá abandonar a pesquisa e tentar novamente mais tarde.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite de tempo do cliente com IDirectorySearch
- ADSI, Search, IDirectorySearch, outras opções de pesquisa, limite de tempo do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1798094a980c41de2e1902533415839020cfd690384f0e56a37bff918d4ecc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692505"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Limite de tempo do cliente com IDirectorySearch

Um cliente pode impor um limite de tempo para um servidor retornar o conjunto de resultados. Quando o servidor não responder a uma consulta dentro do período de tempo especificado, o cliente poderá abandonar a pesquisa e tentar novamente mais tarde.

A preferência de limite de tempo do cliente é útil quando um cliente solicita uma pesquisa assíncrona. Em uma pesquisa assíncrona, o cliente faz uma solicitação e, em seguida, continua com outras tarefas enquanto aguarda o servidor retornar os resultados. É possível que o servidor possa ficar offline sem notificar o cliente. Nesse caso, o cliente não terá nenhuma notificação de se o servidor ainda está processando a consulta ou se ele não está mais em tempo de vida. A preferência de limite de tempo do cliente fornece ao cliente algum controle de situações como esta.

O padrão para o limite de tempo do cliente não é nenhum limite. Para definir um limite de tempo do cliente, de definir uma opção de pesquisa **ADS \_ SEARCHPREF \_ TIMEOUT** com um valor **INTEIRO ADSTYPE \_** que contém o limite de tempo do cliente, em segundos, na matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Um limite de tempo do cliente de zero não indica nenhum limite de tempo.

O exemplo de código a seguir mostra como definir o limite de tempo do cliente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




