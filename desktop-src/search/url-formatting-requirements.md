---
description: A partir do Windows 7, as inconsistências permanecem no tratamento e na análise de URLs. Este tópico fornece um guia limitado para navegar por inconsistências em formatos de URL de arquivo.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Requisitos de formatação de URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08d7945578118f4d3103f44e6da60b96022e472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501451"
---
# <a name="url-formatting-requirements"></a>Requisitos de formatação de URL

A partir do Windows 7, as inconsistências permanecem no tratamento e na análise de URLs. Este tópico fornece um guia limitado para navegar por inconsistências em formatos de URL de arquivo.

Este tópico é organizado da seguinte maneira:

-   [Formatos de URL em uso](#url-formats-in-use)
-   [Sentido de barra, estrela à direita e sensibilidade de barra à direita](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formatos de URL por API e consulta](#url-formats-by-api-and-query)
-   [Tópicos relacionados](#related-topics)

## <a name="url-formats-in-use"></a>Formatos de URL em uso

Protocolos de terceiros são responsáveis por definir seu formato de URL e definir consultas de uma maneira que esteja de acordo com seu padrão. Por exemplo, o Microsoft Outlook oferece suporte a nomes de pastas com caracteres arbitrários, incluindo aqueles que são ilegais em URLs como o `"?"` caractere. O manipulador de protocolo MAPI faz sua própria codificação de URL de suas URLs. Portanto, o índice armazena `"%3F"` em vez de `"?"` e o Outlook deve levar isso em conta ao criar consultas.

Os diferentes formatos são listados na tabela a seguir e cada um deles recebe um identificador de letra para se referir a eles posteriormente neste tópico.



| ID  | URL do arquivo local ou remoto | Exemplo                     |
|-----|--------------------------|-----------------------------|
| Um   | Local                    | file:///c: \\ exemplo de teste \\\\ |
| B   | Local                    | arquivo: c:/Test/example/       |
| C   | Local                    | c: \\ exemplo de teste \\\\         |
| D   | Remoto                   | \\ \\ compartilhamento do servidor file:/// \\\\ |
| E   | Remoto                   | file://server/share/        |
| F   | Remoto                   | \\\\compartilhamento de servidor \\\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Sentido de barra, estrela à direita e sensibilidade de barra à direita

Na pesquisa do Windows, há basicamente nenhuma sensibilidade à direção da barra. Se o formato `c:\test\example` for aceito, c:/Test/example também será aceito. No entanto, embora o [escopo](-search-sql-folderdepth.md) seja geralmente insensível à direção da barra, ele é sensível à direção da barra no caso do formato de URL remoto F. portanto, o não `Scope = '//server/share'` funciona.

A única API que é sensível às estrelas à direita e se distingue entre `c:\test\ ` e `c:\test\*` é [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager). Se houver uma regra de exclusão para `c:\test\*` o, o diretório de URL em `c:\test` si ainda será indexado. Mas se a URL de exclusão for `c:\test\` , o diretório de URL em `c:\test` si não será indexado.

Há dois locais em que o Windows Search é sensível a barras à direita: ItemUrl e consultas de caminho. Se houver um diretório `c:\test` , a pesquisa do Windows tratará `c:\test\` de forma diferente de `c:\test` predicados como `path = 'c:\test'` e `System.ItemUrl = 'c:\test'` . Por exemplo, o predicado `path='file:c:/test'` corresponderia ao diretório `c:\test` , mas `path='file:c:/test/'` não deveria, devido à barra à direita.

## <a name="url-formats-by-api-and-query"></a>Formatos de URL por API e consulta

Formatos de URL de arquivo local aceitos por APIs e consultas selecionadas são listados na tabela a seguir. Os formatos são associados a uma letra (A até F), o significado do que foi indicado na seção "[formatos de URL em uso](#url-formats-in-use)" anteriormente neste tópico.



| API ou consulta                                                                                                    | Formatar um | Formato B | Formatar C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | S        | N        | S        |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | S        | S        | S        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | S        | S        | S        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | S        | N        | N        |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | S        | S        | S        |
| Escopo =                                                                                                          | N        | S        | S        |
| Diretório =                                                                                                      | N        | S        | S        |
| ItemUrl =                                                                                                        | N        | S        | S        |
| Caminho =                                                                                                           | N        | S        | S        |



 

Formatos de URL de arquivo remoto aceitos por consultas selecionadas são listados na tabela a seguir.



| Consulta                                                                                                           | Formato D | Formatar E | Formato F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/D      | N/D      | N/D      |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/D      | N/D      | N/D      |
| Escopo =                                                                                                          | S        | S        | S        |
| Diretório =                                                                                                      | S        | S        | S        |
| ItemUrl =                                                                                                        | S        | S        | S        |
| Caminho =                                                                                                           | S        | S        | S        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que está incluído no índice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de indexação no Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de consulta no Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Processo de notificações no Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
