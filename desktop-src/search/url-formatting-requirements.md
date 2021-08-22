---
description: A partir Windows 7, as inconsistências permanecem no tratamento e na análise de URLs. Este tópico fornece um guia limitado para navegar por inconsistências em formatos de URL de arquivo.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Requisitos de formatação de URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1bb413501548922eaf1b60801b6d35495d7f8a37dc743675052d4e0e5bae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462228"
---
# <a name="url-formatting-requirements"></a>Requisitos de formatação de URL

A partir Windows 7, as inconsistências permanecem no tratamento e na análise de URLs. Este tópico fornece um guia limitado para navegar por inconsistências em formatos de URL de arquivo.

Este tópico é organizado da seguinte forma:

-   [Formatos de URL em uso](#url-formats-in-use)
-   [Direção da barra, estrela à trailing e sensibilidade de barra à trailing](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formatos de URL por API e Consulta](#url-formats-by-api-and-query)
-   [Tópicos relacionados](#related-topics)

## <a name="url-formats-in-use"></a>Formatos de URL em uso

Os protocolos de terceiros são responsáveis por definir seu formato de URL e definir consultas de maneira que esteja em conformidade com seu padrão. Por exemplo, o Microsoft Outlook dá suporte a nomes de pasta com caracteres arbitrários, incluindo aqueles que são ilícitos em URLs, como o `"?"` caractere . O manipulador de protocolo MAPI faz sua própria codificação de URL de suas URLs. Portanto, o índice armazena em vez de e Outlook deve levar isso `"%3F"` em conta ao criar `"?"` consultas.

Os diferentes formatos são listados na tabela a seguir e cada um recebe um identificador de letra para se referir a eles posteriormente neste tópico.



| ID  | URL do arquivo local ou remoto | Exemplo                     |
|-----|--------------------------|-----------------------------|
| Um   | Local                    | file:///c: exemplo \\ de \\ teste\\ |
| B   | Local                    | file:c:/test/example/       |
| C   | Local                    | c: \\ exemplo de \\ teste\\         |
| D   | Remoto                   | file:/// \\ \\ compartilhamento de \\ servidor\\ |
| E   | Remoto                   | file://server/share/        |
| F   | Remoto                   | \\\\compartilhamento \\ de servidor\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Direção da barra, estrela à trailing e sensibilidade de barra à trailing

No Windows Search não há, em grande parte, nenhuma sensibilidade à direção da barra. Se o `c:\test\example` formato for aceito, c:/test/example também será aceito. No entanto, embora [SCOPE](-search-sql-folderdepth.md) geralmente não seja sensível à direção da barra, ele é sensível à direção da barra no caso do formato de URL remoto F. Portanto, `Scope = '//server/share'` não funciona.

A única API que é sensível às estrelas à distância e distingue entre e `c:\test\ ` `c:\test\*` é [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Se houver uma regra de exclusão para , o diretório `c:\test\*` de URL em si ainda será `c:\test` indexado. Mas se a URL de `c:\test\` exclusão for , o diretório de URL `c:\test` em si não será indexado.

Há dois locais em que Windows Search é sensível a barras à frente: consultas ItemUrl e Path. Se houver um diretório , Windows Search tratará de forma `c:\test` `c:\test\` diferente de `c:\test` predicados como `path = 'c:\test'` e `System.ItemUrl = 'c:\test'` . Por exemplo, o `path='file:c:/test'` predicado corresponderia ao diretório , mas `c:\test` não `path='file:c:/test/'` corresponderia, devido à barra à sua parte.

## <a name="url-formats-by-api-and-query"></a>Formatos de URL por API e Consulta

Os formatos de URL de arquivo local aceitos por APIs e consultas selecionadas são listados na tabela a seguir. Os formatos são associados a uma letra (A a F), o significado do qual foi indicado na seção "[Formatos](#url-formats-in-use)de URL em Uso " anteriormente neste tópico.



| API ou consulta                                                                                                    | Formato A | Formato B | Formato C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | Y        | N        | Y        |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | Y        | Y        | Y        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | Y        | N        | N        |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | Y        | Y        | Y        |
| Scope=                                                                                                          | N        | Y        | Y        |
| Directory=                                                                                                      | N        | Y        | Y        |
| ItemUrl=                                                                                                        | N        | Y        | Y        |
| Path=                                                                                                           | N        | Y        | Y        |



 

Os formatos de URL de arquivo remoto aceitos pelas consultas selecionadas são listados na tabela a seguir.



| Consulta                                                                                                           | Formato D | Formato E | Formato F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/D      | N/D      | N/D      |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/D      | N/D      | N/D      |
| Escopo =                                                                                                          | Y        | Y        | Y        |
| Diretório =                                                                                                      | Y        | Y        | Y        |
| ItemUrl =                                                                                                        | Y        | Y        | Y        |
| Caminho =                                                                                                           | Y        | Y        | Y        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que está incluído no índice](-search-indexing-process-overview.md)
</dt> <dt>

[processo de indexação na pesquisa Windows](-search-indexing-process-overview.md)
</dt> <dt>

[processo de consulta na pesquisa Windows](querying-process--windows-search-.md)
</dt> <dt>

[processo de notificações na pesquisa Windows](-search-3x-wds-support.md)
</dt> </dl>

 

 
