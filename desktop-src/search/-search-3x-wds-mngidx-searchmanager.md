---
description: A interface ISearchManager fornece métodos que fazem alterações em catálogos.
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: Usando o Gerenciador de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920770"
---
# <a name="using-the-search-manager"></a>Usando o Gerenciador de pesquisa

A interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) fornece métodos que fazem alterações em catálogos. As alterações feitas no nível de **ISearchManager** se aplicam globalmente a todos os catálogos usados pelo indexador, enquanto as alterações feitas no nível de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) se aplicam a catálogos específicos. No entanto, no momento, o Windows Search usa apenas um catálogo, SystemIndex. Você pode usar o Gerenciador de pesquisa para fazer o seguinte:

- Obtenha uma instância do Gerenciador de catálogo para o catálogo de pesquisa.
- Obtenha informações de versão sobre o mecanismo de pesquisa do Windows.

Os métodos a seguir da interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) podem ajudá-lo a gerenciar seu catálogo (s) de pesquisa:

| Método                                                                      | Descrição                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | Obtém um catálogo por nome e retorna uma instância de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) para esse catálogo. Isso permite que você gerencie um catálogo de pesquisa individual.                                          |
| [**GetIndexerVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | Retorna a versão do indexador em dois inteiros: a versão principal e a versão secundária. Por exemplo, o número de versão principal para a pesquisa do Windows 10 é "10" e o número de versão secundária é "0". Para o Windows Vista Search e o Windows Search 3,0 no Windows XP, o número de versão principal é "3" e o número de versão secundária é "0". |
| [**GetIndexerVersionStr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | Retorna o número de versão completo do indexador como uma cadeia de caracteres: por exemplo, "10.0.18309.1000". Para o Windows 10, isso normalmente corresponderá ao número de versão do sistema operacional. Para o Windows XP, vista e 7, ele será diferente.                                                                                                                                        |


Para obter mais informações sobre esses métodos, consulte a documentação do [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .

Os métodos [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) a seguir são reservados para uso futuro. No entanto, eles são implementados e não afetam o indexador ou catálogo, pois há apenas um catálogo para o Windows Search no momento.

- **obter \_ BypassList**
- **obter \_ LocalBypass**
- **obter \_ PortNumber**
- **obter \_ ProxyName**
- **obter \_ UseProxy**
- **obter \_ UserAgent**
- **colocar \_ UserAgent**
- **SetProxy**

**GetParameter** e **SetParameter** também são reservados para uso futuro, mas não são implementados.

## <a name="related-topics"></a>Tópicos relacionados

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para gerenciar o índice](interfaces-for-managing-the-index.md)

[Usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md)

[Usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md)
