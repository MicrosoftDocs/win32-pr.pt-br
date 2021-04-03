---
title: Especificando outras opções de pesquisa com IDirectorySearch
description: A interface IDirectorySearch fornece controle adicional sobre como a pesquisa é executada por meio do uso de opções de pesquisa.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Especificando outras opções de pesquisa com a ADSI IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915882"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Especificando outras opções de pesquisa com IDirectorySearch

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece controle adicional sobre como a pesquisa é executada por meio do uso de opções de pesquisa. Essas opções de pesquisa são definidas preenchendo uma matriz de estruturas de [**\_ \_ informações do SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e chamando o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Para mais informações, consulte os seguintes tópicos:

-   [Usando o método SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Pesquisas síncronas e assíncronas com IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paginação com IDirectorySearch](paging-with-idirectorysearch.md)
-   [Cache de resultados com IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Executando uma consulta de escopo de atributo](performing-an-attribute-scoped-query.md)
-   [Classificando os resultados da pesquisa com IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Caça de referência com IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Limite de tamanho com IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Limite de tempo do servidor com IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Limite de tempo do cliente com IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Retornando somente nomes de atributo com IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




