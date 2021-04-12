---
title: Cache de resultados com IDirectorySearch
description: A \_ preferência de resultados do cache SEARCHPREF do ADS armazena em \_ \_ cache o conjunto de resultados no cliente.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Cache de resultados com ADSI IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, cache de resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291782"
---
# <a name="result-caching-with-idirectorysearch"></a>Cache de resultados com IDirectorySearch

A preferência de **\_ \_ \_ resultados do cache SEARCHPREF do ADS** armazena em cache o conjunto de resultados no cliente. O cache de resultados permite que um aplicativo retenha um conjunto de resultados recuperado e percorra as linhas recuperadas novamente. Ele também habilita o suporte a cursor em que os métodos [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) e [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) podem ser usados para mover para cima e para baixo o conjunto de resultados.

Por padrão, o cache de resultados está desabilitado. O cache de resultados deve ser habilitado se qualquer uma das seguintes opções for verdadeira:

-   Se o mesmo conjunto de resultados deve ser enumerado várias vezes sem executar a pesquisa novamente no servidor.
-   Se a execução da pesquisa estiver com uso intensivo de recursos no servidor (conexão lenta, grande conjunto de resultados ou consulta complexa).
-   Se o suporte ao cursor for necessário.

Desative o cache se seu aplicativo precisar reduzir os requisitos de memória para armazenar em cache um grande conjunto de resultados no cliente.

O cache de resultados aumenta os requisitos de memória no cliente, portanto, o cache de resultados deve ser desabilitado se isso for uma preocupação.

Para habilitar o cache de resultados, defina uma opção de pesquisa de **\_ \_ \_ resultados do cache SEARCHPREF do ADS** com um valor **\_ booliano de ADSTYPE** **true** na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

O exemplo de código a seguir mostra como habilitar o cache de resultados.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




