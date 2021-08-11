---
title: Especificando outras opções de pesquisa com IDirectorySearch
description: A interface IDirectorySearch fornece controle adicional sobre como a pesquisa é executada por meio do uso de opções de pesquisa.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Especificando outras opções de pesquisa com IDirectorySearch ADSI
- ADSI, Pesquisando, IDirectorySearch, outras opções de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67105d9716934c8c7d1d56193ca0cdfde5f6a4bc4c32605420513dc62700d8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178761"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Especificando outras opções de pesquisa com IDirectorySearch

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece controle adicional sobre como a pesquisa é executada por meio do uso de opções de pesquisa. Essas opções de pesquisa são definidas preenchendo uma matriz de estruturas [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e chamando o [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Para obter mais informações, consulte estes tópicos:

-   [Usando o método SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Pesquisas síncronas e assíncronas com IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paging com IDirectorySearch](paging-with-idirectorysearch.md)
-   [Resultado Caching com IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Executando uma consulta de escopo de atributo](performing-an-attribute-scoped-query.md)
-   [Classificação dos resultados da pesquisa com IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Indicação de busca com IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Limite de tamanho com IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Limite de tempo do servidor com IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Limite de tempo do cliente com IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Retornando apenas nomes de atributo com IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




