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
# <a name="querying-the-index-with-isearchqueryhelper"></a><span data-ttu-id="0d03c-104">Consultando o índice com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="0d03c-104">Querying the Index with ISearchQueryHelper</span></span>

<span data-ttu-id="0d03c-105">Você pode usar a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para consultar o índice.</span><span class="sxs-lookup"><span data-stu-id="0d03c-105">You can use the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface to query the index.</span></span> <span data-ttu-id="0d03c-106">Essa interface é implementada como uma classe auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) e é obtida chamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="0d03c-106">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (and [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)), and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span> <span data-ttu-id="0d03c-107">Essa interface permite que você:</span><span class="sxs-lookup"><span data-stu-id="0d03c-107">This interface permits you to:</span></span>

-   <span data-ttu-id="0d03c-108">Obtenha uma cadeia de conexão OLE DB para se conectar ao banco de dados de pesquisa do Windows.</span><span class="sxs-lookup"><span data-stu-id="0d03c-108">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
-   <span data-ttu-id="0d03c-109">Converta as consultas de usuário AQS (sintaxe de consulta avançada) para o Windows Search linguagem SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="0d03c-109">Convert Advanced Query Syntax (AQS) user queries to Windows Search Structured Query Language (SQL).</span></span>
-   <span data-ttu-id="0d03c-110">Especifique as restrições de consulta que podem ser expressas em SQL, mas não em AQS.</span><span class="sxs-lookup"><span data-stu-id="0d03c-110">Specify query restrictions that can be expressed in SQL, but not in AQS.</span></span>

<span data-ttu-id="0d03c-111">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0d03c-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0d03c-112">Introdução com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="0d03c-112">Getting Started with ISearchQueryHelper</span></span>](#getting-started-with-isearchqueryhelper)
-   [<span data-ttu-id="0d03c-113">Usando o método GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="0d03c-113">Using the GenerateSqlFromUserQuery Method</span></span>](#using-the-generatesqlfromuserquery-method)
-   [<span data-ttu-id="0d03c-114">Trabalhando com identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="0d03c-114">Working with Locale Identifiers</span></span>](#working-with-locale-identifiers)
-   [<span data-ttu-id="0d03c-115">Trabalhando com propriedades e colunas</span><span class="sxs-lookup"><span data-stu-id="0d03c-115">Working with Properties and Columns</span></span>](#working-with-properties-and-columns)
-   [<span data-ttu-id="0d03c-116">Trabalhando com expansão de termo de consulta</span><span class="sxs-lookup"><span data-stu-id="0d03c-116">Working with Query Term Expansion</span></span>](#working-with-query-term-expansion)
-   [<span data-ttu-id="0d03c-117">Trabalhando com outros métodos ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="0d03c-117">Working with Other ISearchQueryHelper Methods</span></span>](#working-with-other-isearchqueryhelper-methods)
-   [<span data-ttu-id="0d03c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d03c-118">Related topics</span></span>](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a><span data-ttu-id="0d03c-119">Introdução com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="0d03c-119">Getting Started with ISearchQueryHelper</span></span>

<span data-ttu-id="0d03c-120">Há algumas interfaces e métodos principais que você deve estar atento antes de poder iniciar a consulta por meio de programação do Windows Search usando a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="0d03c-120">There are a few key interfaces and methods you should be aware of before you can start programmatically querying Windows Search using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface.</span></span> <span data-ttu-id="0d03c-121">Em um alto nível, você precisa seguir estas etapas:</span><span class="sxs-lookup"><span data-stu-id="0d03c-121">At a high level, you need to follow these steps:</span></span>

1.  <span data-ttu-id="0d03c-122">Instanciar uma instância de [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="0d03c-122">Instantiate an [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) instance.</span></span>
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  <span data-ttu-id="0d03c-123">Obtenha uma instância de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) usando [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span><span class="sxs-lookup"><span data-stu-id="0d03c-123">Obtain an instance of [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) using [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog).</span></span> <span data-ttu-id="0d03c-124">O nome do catálogo do sistema para a pesquisa do Windows é `SYSTEMINDEX` .</span><span class="sxs-lookup"><span data-stu-id="0d03c-124">The name of the system catalog for Windows Search is `SYSTEMINDEX`.</span></span>
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  <span data-ttu-id="0d03c-125">Obtenha uma instância de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) usando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="0d03c-125">Obtain an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) using [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).</span></span>
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  <span data-ttu-id="0d03c-126">Depois de ter uma instância de [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), você pode obter a cadeia de conexão usada para se conectar ao conector de OLE DB do índice do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="0d03c-126">After you have an instance of [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), you can then get the connection string used to connect to the Windows Search index OLE DB connector.</span></span>
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a><span data-ttu-id="0d03c-127">Usando o método GenerateSqlFromUserQuery</span><span class="sxs-lookup"><span data-stu-id="0d03c-127">Using the GenerateSqlFromUserQuery Method</span></span>

<span data-ttu-id="0d03c-128">O método [**ISearchQueryHelper:: GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) transforma a entrada do usuário em uma cadeia de caracteres de consulta SQL, que pode ser enviada para o provedor de OLE DB para Windows Search.</span><span class="sxs-lookup"><span data-stu-id="0d03c-128">The [**ISearchQueryHelper::GenerateSQLFromUserQuery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) method transforms user input into a SQL query string, which can then be submitted to the OLE DB provider for Windows Search.</span></span> <span data-ttu-id="0d03c-129">Esse método traduz a consulta de [sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md) (AQS) ou nQS (sintaxe de consulta natural) inserida pelo usuário no SQL e permite que você adicione outros fragmentos do SQL, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="0d03c-129">This method translates the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md) (AQS) or Natural Query Syntax (NQS) query entered by the user into SQL, and lets you add other SQL fragments as needed.</span></span>

<span data-ttu-id="0d03c-130">A cadeia de caracteres de consulta SQL é retornada no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="0d03c-130">The SQL query string is returned in the following form:</span></span>


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



<span data-ttu-id="0d03c-131">Veja a seguir um exemplo da cadeia de caracteres SQL retornada da chamada `GenerateSQLFromUserQuery("comput")` :</span><span class="sxs-lookup"><span data-stu-id="0d03c-131">The following is an example of the SQL string returned from the call `GenerateSQLFromUserQuery("comput")`:</span></span>


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> <span data-ttu-id="0d03c-132">O método gera os predicados FREETEXT e CONTAINS porque CONTAINS sozinho não gera uma classificação significativa.</span><span class="sxs-lookup"><span data-stu-id="0d03c-132">The method generates both the FREETEXT and the CONTAINS predicates because CONTAINS alone does not generate meaningful ranking.</span></span>

 

## <a name="working-with-locale-identifiers"></a><span data-ttu-id="0d03c-133">Trabalhando com identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="0d03c-133">Working with Locale Identifiers</span></span>



| <span data-ttu-id="0d03c-134">Método</span><span class="sxs-lookup"><span data-stu-id="0d03c-134">Method</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="0d03c-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d03c-135">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d03c-136">[**ISearchQueryHelper:: obter \_ QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span><span class="sxs-lookup"><span data-stu-id="0d03c-136">[**ISearchQueryHelper::get\_QueryContentLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/</span></span><br/> [<span data-ttu-id="0d03c-137">**ISearchQueryHelper::p UT \_ QueryContentLocale**</span><span class="sxs-lookup"><span data-stu-id="0d03c-137">**ISearchQueryHelper::put\_QueryContentLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | <span data-ttu-id="0d03c-138">Obtém/coloca o LCID (identificador de código de idioma) da consulta.</span><span class="sxs-lookup"><span data-stu-id="0d03c-138">Gets/Puts the language code identifier (LCID) of the query.</span></span> <span data-ttu-id="0d03c-139">Isso ajuda a obter o separador de separador e o lematizador corretos para comparar os termos de consulta com o índice/catálogo invertido.</span><span class="sxs-lookup"><span data-stu-id="0d03c-139">This helps get the correct wordbreaker and stemmer to compare query terms against the catalog/inverted index.</span></span> <span data-ttu-id="0d03c-140">O padrão é a localidade de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="0d03c-140">The default is the current input locale.</span></span> |
| <span data-ttu-id="0d03c-141">[**ISearchQueryHelper:: obter \_ QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span><span class="sxs-lookup"><span data-stu-id="0d03c-141">[**ISearchQueryHelper::get\_QueryKeywordLocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/</span></span><br/> [<span data-ttu-id="0d03c-142">**ISearchQueryHelper::p UT \_ QueryKeywordLocale**</span><span class="sxs-lookup"><span data-stu-id="0d03c-142">**ISearchQueryHelper::put\_QueryKeywordLocale**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | <span data-ttu-id="0d03c-143">Obtém/coloca o LCID para o idioma a ser usado ao analisar palavras-chave de sintaxe de consulta avançada (AQS).</span><span class="sxs-lookup"><span data-stu-id="0d03c-143">Gets/Puts the LCID for the language to use when parsing Advanced Query Syntax (AQS) keywords.</span></span> <span data-ttu-id="0d03c-144">O padrão é a localidade do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="0d03c-144">The default is the default user locale.</span></span>                                                                              |



 

<span data-ttu-id="0d03c-145">A localidade do **conteúdo** e a **localidade da palavra-chave** são identificadores de localidade (LCID) que ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma dos termos da consulta e o idioma das palavras-chave AQS.</span><span class="sxs-lookup"><span data-stu-id="0d03c-145">The **content locale** and **keyword locale** are locale identifiers (LCID) that help the search engine use the correct word breakers by identifying the language of the query terms and the language the AQS keywords.</span></span> <span data-ttu-id="0d03c-146">Esses nem sempre são os mesmos LCIDs porque o Windows Search é oferecido em várias versões internacionais e também inclui pacotes MUI (Multilingual User interface) para mais idiomas.</span><span class="sxs-lookup"><span data-stu-id="0d03c-146">These are not always the same LCIDs because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="0d03c-147">A localidade do conteúdo identifica o LCID para a linguagem na qual os usuários inserim sua consulta de pesquisa, enquanto a localidade da palavra-chave identifica o LCID que o mecanismo de pesquisa usa ao analisar as palavras-chave da sintaxe de consulta avançada (AQS).</span><span class="sxs-lookup"><span data-stu-id="0d03c-147">The content locale identifies the LCID for the language users input their search query in, while the keyword locale identifies the LCID the search engine uses when parsing Advanced Query Syntax (AQS) keywords.</span></span>

<span data-ttu-id="0d03c-148">Por exemplo, se você tiver a versão em inglês-EUA sem MUI Packs, tanto a localidade de conteúdo quanto a localidade de palavra-chave serão 1033.</span><span class="sxs-lookup"><span data-stu-id="0d03c-148">For example, if you have the English-US version with no MUI packs, both the content locale and keyword locale are 1033.</span></span> <span data-ttu-id="0d03c-149">Se você tiver a versão em alemão sem MUI Packs, tanto a localidade do conteúdo quanto a localidade da palavra-chave serão 1031 (GR-GR).</span><span class="sxs-lookup"><span data-stu-id="0d03c-149">If you have the German version with no MUI packs, then both the content locale and keyword locale are 1031 (gr-gr).</span></span> <span data-ttu-id="0d03c-150">No entanto, se você tiver a versão em inglês com o pacote MUI do romeno, a localidade do conteúdo será 2072 (RO) e a localidade da palavra-chave será 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="0d03c-150">However, if you have the English version with the Romanian MUI pack, the content locale is 2072 (ro) and the keyword locale is 1033 (en-us).</span></span>

## <a name="working-with-properties-and-columns"></a><span data-ttu-id="0d03c-151">Trabalhando com propriedades e colunas</span><span class="sxs-lookup"><span data-stu-id="0d03c-151">Working with Properties and Columns</span></span>



| <span data-ttu-id="0d03c-152">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d03c-152">Methods</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="0d03c-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d03c-153">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d03c-154">[**ISearchQueryHelper:: obter \_ QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span><span class="sxs-lookup"><span data-stu-id="0d03c-154">[**ISearchQueryHelper::get\_QueryContentProperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/</span></span><br/> [<span data-ttu-id="0d03c-155">**ISearchQueryHelper::p UT \_ QueryContentProperties**</span><span class="sxs-lookup"><span data-stu-id="0d03c-155">**ISearchQueryHelper::put\_QueryContentProperties**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | <span data-ttu-id="0d03c-156">Obtém/define as propriedades de conteúdo da pesquisa (coluna de propriedade listada nas cláusulas CONTAINS ou FREETEXT).</span><span class="sxs-lookup"><span data-stu-id="0d03c-156">Gets/Sets the content properties for the search (property column listed in the CONTAINS or FREETEXT clauses).</span></span>                                   |
| <span data-ttu-id="0d03c-157">[**ISearchQueryHelper:: obter \_ QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span><span class="sxs-lookup"><span data-stu-id="0d03c-157">[**ISearchQueryHelper::get\_QuerySelectColumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/</span></span><br/> [<span data-ttu-id="0d03c-158">**ISearchQueryHelper::p UT \_ QuerySelectColumns**</span><span class="sxs-lookup"><span data-stu-id="0d03c-158">**ISearchQueryHelper::put\_QuerySelectColumns**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | <span data-ttu-id="0d03c-159">Obtém/define as colunas (ou Propriedades) solicitadas na instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="0d03c-159">Gets/Sets the columns (or properties) requested in the SELECT statement.</span></span> <span data-ttu-id="0d03c-160">O padrão é System. ItemUrl e as propriedades usadas na cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="0d03c-160">The default is System.ItemUrl and properties used in the WHERE clause.</span></span> |



 

<span data-ttu-id="0d03c-161">Os itens são representados no repositório de propriedades como uma linha.</span><span class="sxs-lookup"><span data-stu-id="0d03c-161">Items are represented in the property store as a row.</span></span> <span data-ttu-id="0d03c-162">Cada linha contém um número de colunas que representam propriedades para esse item.</span><span class="sxs-lookup"><span data-stu-id="0d03c-162">Each row contains a number of columns that represent properties for that item.</span></span> <span data-ttu-id="0d03c-163">Nem todos os itens terão um valor para uma determinada propriedade.</span><span class="sxs-lookup"><span data-stu-id="0d03c-163">Not all items will have a value for a given property.</span></span> <span data-ttu-id="0d03c-164">Por exemplo, um arquivo de áudio normalmente não conteria um valor para a propriedade System. Property. FromName, mas pode conter informações sobre o System. Music. artista.</span><span class="sxs-lookup"><span data-stu-id="0d03c-164">For example, an audio file would typically not contain a value for the System.Property.FromName property but may contain information regarding the System.Music.Artist.</span></span>

<span data-ttu-id="0d03c-165">Com esses métodos, você acessa ou modifica a propriedade com uma cadeia de caracteres Unicode delimitada por vírgula, terminada em nulo que especifica um ou mais nomes de coluna do repositório de propriedades: "System.Document. Autor, System.Document. Título ".</span><span class="sxs-lookup"><span data-stu-id="0d03c-165">With these methods, you access or modify the property with a comma delimited, null-terminated, Unicode string that specifies one or more column names of the property store: "System.Document.Author, System.Document.Title".</span></span>

## <a name="working-with-query-term-expansion"></a><span data-ttu-id="0d03c-166">Trabalhando com expansão de termo de consulta</span><span class="sxs-lookup"><span data-stu-id="0d03c-166">Working with Query Term Expansion</span></span>



| <span data-ttu-id="0d03c-167">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d03c-167">Methods</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="0d03c-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d03c-168">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="0d03c-169">**ISearchQueryHelper:: obter \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="0d03c-169">**ISearchQueryHelper::get\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [<span data-ttu-id="0d03c-170">**ISearchQueryHelper::p UT \_ QueryTermExpansion**</span><span class="sxs-lookup"><span data-stu-id="0d03c-170">**ISearchQueryHelper::put\_QueryTermExpansion**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | <span data-ttu-id="0d03c-171">Obtém/define o sinalizador de expansão do termo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0d03c-171">Gets/Sets the search term expansion flag.</span></span> |



 

<span data-ttu-id="0d03c-172">Esse método permite a expansão de alguns termos de consulta com caracteres curinga, semelhante à expansão de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="0d03c-172">This method enables the expansion of some query terms with wild card characters, similar to regular expression expansion.</span></span> <span data-ttu-id="0d03c-173">A expansão de prefixo procura palavras com o mesmo prefixo (diversão/funil).</span><span class="sxs-lookup"><span data-stu-id="0d03c-173">Prefix expansion searches for words with the same prefix (fun/funnel).</span></span> <span data-ttu-id="0d03c-174">Se não estiver definido, o valor padrão é o termo de pesquisa \_ \_ prefixo \_ todos.</span><span class="sxs-lookup"><span data-stu-id="0d03c-174">If not set, the default value is SEARCH\_TERM\_PREFIX\_ALL.</span></span> <span data-ttu-id="0d03c-175">Os valores com suporte da enumeração de [**\_ \_ expansão do termo de pesquisa**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0d03c-175">The supported values of the [**SEARCH\_TERM\_EXPANSION**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) enumeration are as follows:</span></span>

-   <span data-ttu-id="0d03c-176">\_Prefixo do termo \_ de pesquisa \_ todos-todos os termos de pesquisa são expandidos</span><span class="sxs-lookup"><span data-stu-id="0d03c-176">SEARCH\_TERM\_PREFIX\_ALL - All search terms are expanded</span></span>
-   <span data-ttu-id="0d03c-177">Termo de pesquisa \_ \_ sem \_ expansão-nenhum termo de pesquisa é expandido</span><span class="sxs-lookup"><span data-stu-id="0d03c-177">SEARCH\_TERM\_NO\_EXPANSION - No search terms are expanded</span></span>

## <a name="working-with-other-isearchqueryhelper-methods"></a><span data-ttu-id="0d03c-178">Trabalhando com outros métodos ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="0d03c-178">Working with Other ISearchQueryHelper Methods</span></span>

<span data-ttu-id="0d03c-179">Muitos dos métodos na interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) são usados para definir argumentos de consulta ou definir as propriedades retornadas.</span><span class="sxs-lookup"><span data-stu-id="0d03c-179">Many of the methods in the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface are used to set query arguments or define the properties returned.</span></span>



| <span data-ttu-id="0d03c-180">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d03c-180">Methods</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="0d03c-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d03c-181">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d03c-182">**ISearchQueryHelper:: obter \_ ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="0d03c-182">**ISearchQueryHelper::get\_ConnectionString**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | <span data-ttu-id="0d03c-183">Retorna a cadeia de conexão OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0d03c-183">Returns the OLE DB connection string.</span></span> <span data-ttu-id="0d03c-184">Esse é o método preferencial para obter uma cadeia de conexão corretamente formatada e correta.</span><span class="sxs-lookup"><span data-stu-id="0d03c-184">This is the preferred method of getting a properly formatted and correct connection string.</span></span>                                  |
| [<span data-ttu-id="0d03c-185">**ISearchQueryHelper:: obter \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="0d03c-185">**ISearchQueryHelper::get\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [<span data-ttu-id="0d03c-186">**ISearchQueryHelper::p UT \_ QueryMaxResults**</span><span class="sxs-lookup"><span data-stu-id="0d03c-186">**ISearchQueryHelper::put\_QueryMaxResults**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | <span data-ttu-id="0d03c-187">Obtém/define o número máximo de resultados a serem retornados por uma consulta (ou seja, selecione TOP n).</span><span class="sxs-lookup"><span data-stu-id="0d03c-187">Gets/Sets the maximum number of results to be returned by a query (that is, SELECT TOP n).</span></span> <span data-ttu-id="0d03c-188">O padrão é-1, o que significa que nenhuma cláusula de resultados máximo é gerada.</span><span class="sxs-lookup"><span data-stu-id="0d03c-188">The default is -1, meaning that no maximum results clause is generated.</span></span> |
| [<span data-ttu-id="0d03c-189">**ISearchQueryHelper:: obter \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="0d03c-189">**ISearchQueryHelper::get\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [<span data-ttu-id="0d03c-190">**ISearchQueryHelper::p UT \_ QuerySorting**</span><span class="sxs-lookup"><span data-stu-id="0d03c-190">**ISearchQueryHelper::put\_QuerySorting**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | <span data-ttu-id="0d03c-191">Obtém/define a ordem de classificação para o conjunto de resultados da consulta (ORDER BY).</span><span class="sxs-lookup"><span data-stu-id="0d03c-191">Gets/Sets the sort order for the query result set (ORDER BY).</span></span> <span data-ttu-id="0d03c-192">Se nenhuma cláusula ORDER BY existir, os resultados serão retornados em uma ordem não determinística.</span><span class="sxs-lookup"><span data-stu-id="0d03c-192">If no ORDER BY clause exists, the results are returned in non-deterministic order.</span></span>                   |
| [<span data-ttu-id="0d03c-193">**ISearchQueryHelper:: obter \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="0d03c-193">**ISearchQueryHelper::get\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [<span data-ttu-id="0d03c-194">**ISearchQueryHelper::p UT \_ QuerySyntax**</span><span class="sxs-lookup"><span data-stu-id="0d03c-194">**ISearchQueryHelper::put\_QuerySyntax**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | <span data-ttu-id="0d03c-195">Obtém/define a sintaxe da consulta: sintaxe de consulta avançada ou sintaxe de consulta natural.</span><span class="sxs-lookup"><span data-stu-id="0d03c-195">Gets/Sets the syntax of the query: Advanced Query Syntax or Natural Query Syntax.</span></span>                                                                                  |
| [<span data-ttu-id="0d03c-196">**ISearchQueryHelper:: obter \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="0d03c-196">**ISearchQueryHelper::get\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [<span data-ttu-id="0d03c-197">**ISearchQueryHelper::p UT \_ QueryWhereRestrictions**</span><span class="sxs-lookup"><span data-stu-id="0d03c-197">**ISearchQueryHelper::put\_QueryWhereRestrictions**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | <span data-ttu-id="0d03c-198">Obtém/define as restrições anexadas por meio de cláusulas WHERE.</span><span class="sxs-lookup"><span data-stu-id="0d03c-198">Gets/Sets the restrictions appended via WHERE clauses.</span></span>                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="0d03c-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d03c-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d03c-200">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="0d03c-200">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="0d03c-201">Usando abordagens SQL e AQS para consultar o índice</span><span class="sxs-lookup"><span data-stu-id="0d03c-201">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="0d03c-202">Consultando o índice com o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="0d03c-202">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="0d03c-203">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="0d03c-203">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="0d03c-204">Usando a sintaxe de consulta avançada programaticamente</span><span class="sxs-lookup"><span data-stu-id="0d03c-204">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




