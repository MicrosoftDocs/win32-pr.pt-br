---
description: 'Você pode usar a interface ISearchQueryHelper para consultar o índice. Essa interface é implementada como uma classe auxiliar para ISearchCatalogManager (e ISearchCatalogManager2) e é obtida chamando ISearchCatalogManager:: GetQueryHelper.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Consultando o índice com ISearchQueryHelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164340"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>Consultando o índice com ISearchQueryHelper

Você pode usar a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para consultar o índice. Essa interface é implementada como uma classe auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) e é obtida chamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Essa interface permite que você:

-   Obtenha uma cadeia de conexão OLE DB para se conectar ao banco de dados de pesquisa do Windows.
-   Converta as consultas de usuário AQS (sintaxe de consulta avançada) para o Windows Search linguagem SQL (SQL).
-   Especifique as restrições de consulta que podem ser expressas em SQL, mas não em AQS.

Este tópico é organizado da seguinte maneira:

-   [Introdução com ISearchQueryHelper](#getting-started-with-isearchqueryhelper)
-   [Usando o método GenerateSqlFromUserQuery](#using-the-generatesqlfromuserquery-method)
-   [Trabalhando com identificadores de localidade](#working-with-locale-identifiers)
-   [Trabalhando com propriedades e colunas](#working-with-properties-and-columns)
-   [Trabalhando com expansão de termo de consulta](#working-with-query-term-expansion)
-   [Trabalhando com outros métodos ISearchQueryHelper](#working-with-other-isearchqueryhelper-methods)
-   [Tópicos relacionados](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>Introdução com ISearchQueryHelper

Há algumas interfaces e métodos principais que você deve estar atento antes de poder iniciar a consulta por meio de programação do Windows Search usando a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Em um alto nível, você precisa seguir estas etapas:

1.  Instanciar uma instância de [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Obtenha uma instância de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) usando [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog). O nome do catálogo do sistema para a pesquisa do Windows é `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Obtenha uma instância de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) usando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  Depois de ter uma instância de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), você pode obter a cadeia de conexão usada para se conectar ao conector de OLE DB do índice do Windows Search.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Usando o método GenerateSqlFromUserQuery

O método [**ISearchQueryHelper:: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforma a entrada do usuário em uma cadeia de caracteres de consulta SQL, que pode ser enviada para o provedor de OLE DB para Windows Search. Esse método traduz a consulta de [sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md) (AQS) ou nQS (sintaxe de consulta natural) inserida pelo usuário no SQL e permite que você adicione outros fragmentos do SQL, conforme necessário.

A cadeia de caracteres de consulta SQL é retornada no seguinte formato:


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



Veja a seguir um exemplo da cadeia de caracteres SQL retornada da chamada `GenerateSQLFromUserQuery("comput")` :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> O método gera os predicados FREETEXT e CONTAINS porque CONTAINS sozinho não gera uma classificação significativa.

 

## <a name="working-with-locale-identifiers"></a>Trabalhando com identificadores de localidade



| Método                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: obter \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**ISearchQueryHelper::p UT \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Obtém/coloca o LCID (identificador de código de idioma) da consulta. Isso ajuda a obter o separador de separador e o lematizador corretos para comparar os termos de consulta com o índice/catálogo invertido. O padrão é a localidade de entrada atual. |
| [**ISearchQueryHelper:: obter \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**ISearchQueryHelper::p UT \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Obtém/coloca o LCID para o idioma a ser usado ao analisar palavras-chave de sintaxe de consulta avançada (AQS). O padrão é a localidade do usuário padrão.                                                                              |



 

A localidade do **conteúdo** e a **localidade da palavra-chave** são identificadores de localidade (LCID) que ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma dos termos da consulta e o idioma das palavras-chave AQS. Esses nem sempre são os mesmos LCIDs porque o Windows Search é oferecido em várias versões internacionais e também inclui pacotes MUI (Multilingual User interface) para mais idiomas. A localidade do conteúdo identifica o LCID para a linguagem na qual os usuários inserim sua consulta de pesquisa, enquanto a localidade da palavra-chave identifica o LCID que o mecanismo de pesquisa usa ao analisar as palavras-chave da sintaxe de consulta avançada (AQS).

Por exemplo, se você tiver a versão em inglês-EUA sem MUI Packs, tanto a localidade de conteúdo quanto a localidade de palavra-chave serão 1033. Se você tiver a versão em alemão sem MUI Packs, tanto a localidade do conteúdo quanto a localidade da palavra-chave serão 1031 (GR-GR). No entanto, se você tiver a versão em inglês com o pacote MUI do romeno, a localidade do conteúdo será 2072 (RO) e a localidade da palavra-chave será 1033 (en-US).

## <a name="working-with-properties-and-columns"></a>Trabalhando com propriedades e colunas



| Métodos                                                                                                                                                                                                                                                  | Descrição                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: obter \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**ISearchQueryHelper::p UT \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Obtém/define as propriedades de conteúdo da pesquisa (coluna de propriedade listada nas cláusulas CONTAINS ou FREETEXT).                                   |
| [**ISearchQueryHelper:: obter \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**ISearchQueryHelper::p UT \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Obtém/define as colunas (ou Propriedades) solicitadas na instrução SELECT. O padrão é System. ItemUrl e as propriedades usadas na cláusula WHERE. |



 

Os itens são representados no repositório de propriedades como uma linha. Cada linha contém um número de colunas que representam propriedades para esse item. Nem todos os itens terão um valor para uma determinada propriedade. Por exemplo, um arquivo de áudio normalmente não conteria um valor para a propriedade System. Property. FromName, mas pode conter informações sobre o System. Music. artista.

Com esses métodos, você acessa ou modifica a propriedade com uma cadeia de caracteres Unicode delimitada por vírgula, terminada em nulo que especifica um ou mais nomes de coluna do repositório de propriedades: "System.Document. Autor, System.Document. Título ".

## <a name="working-with-query-term-expansion"></a>Trabalhando com expansão de termo de consulta



| Métodos                                                                                                                                                                                                                                 | Descrição                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**ISearchQueryHelper:: obter \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**ISearchQueryHelper::p UT \_ QueryTermExpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Obtém/define o sinalizador de expansão do termo de pesquisa. |



 

Esse método permite a expansão de alguns termos de consulta com caracteres curinga, semelhante à expansão de expressão regular. A expansão de prefixo procura palavras com o mesmo prefixo (diversão/funil). Se não estiver definido, o valor padrão é o termo de pesquisa \_ \_ prefixo \_ todos. Os valores com suporte da enumeração de [**\_ \_ expansão do termo de pesquisa**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) são os seguintes:

-   \_Prefixo do termo \_ de pesquisa \_ todos-todos os termos de pesquisa são expandidos
-   Termo de pesquisa \_ \_ sem \_ expansão-nenhum termo de pesquisa é expandido

## <a name="working-with-other-isearchqueryhelper-methods"></a>Trabalhando com outros métodos ISearchQueryHelper

Muitos dos métodos na interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) são usados para definir argumentos de consulta ou definir as propriedades retornadas.



| Métodos                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchQueryHelper:: obter \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Retorna a cadeia de conexão OLE DB. Esse é o método preferencial para obter uma cadeia de conexão corretamente formatada e correta.                                  |
| [**ISearchQueryHelper:: obter \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**ISearchQueryHelper::p UT \_ QueryMaxResults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Obtém/define o número máximo de resultados a serem retornados por uma consulta (ou seja, selecione TOP n). O padrão é-1, o que significa que nenhuma cláusula de resultados máximo é gerada. |
| [**ISearchQueryHelper:: obter \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**ISearchQueryHelper::p UT \_ QuerySorting**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Obtém/define a ordem de classificação para o conjunto de resultados da consulta (ORDER BY). Se nenhuma cláusula ORDER BY existir, os resultados serão retornados em uma ordem não determinística.                   |
| [**ISearchQueryHelper:: obter \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**ISearchQueryHelper::p UT \_ QuerySyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Obtém/define a sintaxe da consulta: sintaxe de consulta avançada ou sintaxe de consulta natural.                                                                                  |
| [**ISearchQueryHelper:: obter \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**ISearchQueryHelper::p UT \_ QueryWhereRestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Obtém/define as restrições anexadas por meio de cláusulas WHERE.                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Usando abordagens SQL e AQS para consultar o índice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




