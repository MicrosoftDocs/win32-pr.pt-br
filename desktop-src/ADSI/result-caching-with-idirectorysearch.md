---
title: Caching de resultado com IDirectorySearch
description: A \_ preferência de resultados do cache SEARCHPREF do ADS armazena em \_ \_ cache o conjunto de resultados no cliente.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Caching de resultado com ADSI IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, Caching de resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838852"
---
# <a name="result-caching-with-idirectorysearch"></a>Caching de resultado com IDirectorySearch

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



 

 




