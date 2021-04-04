---
title: Pesquisando com a interface IDirectorySearch
description: A interface IDirectorySearch fornece uma interface de alto nível e baixa sobrecarga para consultar dados de um diretório ou de um catálogo global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Pesquisando com a interface IDirectorySearch ADSI
- Consulta ADSI, interfaces de consulta, IDirectorySearch
- ADSI ADSI, código de exemplo C/C++, pesquisando um diretório com IDirectorySearch
- IDirectorySearch ADSI, usando para pesquisar um diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823992"
---
# <a name="searching-with-the-idirectorysearch-interface"></a><span data-ttu-id="b7a8f-107">Pesquisando com a interface IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b7a8f-107">Searching with the IDirectorySearch Interface</span></span>

<span data-ttu-id="b7a8f-108">A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece uma interface de alto nível e baixa sobrecarga para consultar dados de um diretório ou de um catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-108">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides a high-level and low-overhead interface for querying data of a directory or a global catalog.</span></span> <span data-ttu-id="b7a8f-109">A interface com **IDirectorySearch** pode ser usada somente com uma vtable e, portanto, não está disponível para ambientes de desenvolvimento baseados em automação.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-109">The **IDirectorySearch** COM interface can be used only with a vtable, and thus, is not available to Automation-based development environments.</span></span>

<span data-ttu-id="b7a8f-110">**Para executar uma pesquisa**</span><span class="sxs-lookup"><span data-stu-id="b7a8f-110">**To perform a search**</span></span>

1.  <span data-ttu-id="b7a8f-111">Associar a um objeto no diretório.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-111">Bind to an object in the directory.</span></span>
2.  <span data-ttu-id="b7a8f-112">Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter o ponteiro [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-112">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span>
3.  <span data-ttu-id="b7a8f-113">Execute a pesquisa usando o ponteiro [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-113">Run the search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pointer.</span></span> <span data-ttu-id="b7a8f-114">Chame o método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) e passe um filtro de pesquisa, os nomes de atributo solicitados e outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-114">Call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method, and pass a search filter, the requested attribute names, and other parameters.</span></span>

<span data-ttu-id="b7a8f-115">Para obter mais informações sobre a sintaxe do filtro de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="b7a8f-115">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="b7a8f-116">A execução da consulta é específica do provedor.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-116">Query execution is provider-specific.</span></span> <span data-ttu-id="b7a8f-117">Com alguns provedores, a execução da consulta real não ocorre até que [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-117">With some providers, the actual query execution does not occur until [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) is called.</span></span> <span data-ttu-id="b7a8f-118">A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funciona diretamente com filtros de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-118">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface works with search filters directly.</span></span> <span data-ttu-id="b7a8f-119">Nem o dialeto SQL nem o dialeto LDAP são necessários.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-119">Neither the SQL dialect nor the LDAP dialect are required.</span></span>

<span data-ttu-id="b7a8f-120">A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece métodos para enumerar o conjunto de resultados, linha por linha.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-120">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provides methods to enumerate the result set, row by row.</span></span> <span data-ttu-id="b7a8f-121">O método [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera a primeira linha e [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) move você para a próxima linha da linha atual.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-121">The [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) method retrieves the first row and [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) moves you to the next row from the current row.</span></span> <span data-ttu-id="b7a8f-122">Quando você tiver atingido a última linha, chamar esses métodos retornará o \_ código de erro S anúncios de \_ mais \_ linhas.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-122">When you have reached the last row, calling these methods returns the S\_ADS\_NOMORE\_ROWS error code.</span></span> <span data-ttu-id="b7a8f-123">Por outro lado, [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) o move de volta uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-123">Conversely, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) moves you back one row at a time.</span></span> <span data-ttu-id="b7a8f-124">Um valor de retorno de anúncios de S \_ \_ mais \_ linhas indica que você atingiu a primeira linha do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-124">An S\_ADS\_NOMORE\_ROWS return value indicates that you have reached the first row of the result set.</span></span> <span data-ttu-id="b7a8f-125">Esses métodos operam no conjunto de resultados, residente na memória, no cliente.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-125">These methods operate on the result set, resident in memory, on the client.</span></span> <span data-ttu-id="b7a8f-126">Assim, quando pesquisas paginadas e assíncronas são executadas e a \_ opção de resultados de cache \_ é desativada, a rolagem regressiva pode ter consequências inesperadas.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-126">Thus, when paged and asynchronous searches are performed and the \_CACHE\_RESULTS option is turned off, backward scrolling can have unexpected consequences.</span></span>

<span data-ttu-id="b7a8f-127">Quando você localizar a linha apropriada, chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para obter itens de dados, coluna por coluna.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-127">When you have located the appropriate row, call [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) to obtain data items, column by column.</span></span> <span data-ttu-id="b7a8f-128">Para cada chamada, você passa o nome da coluna de interesse.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-128">For each call, you pass the name of the column of interest.</span></span> <span data-ttu-id="b7a8f-129">O item de dados retornado é um ponteiro para uma estrutura de [**\_ \_ coluna de pesquisa do ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-129">The data item returned is a pointer to an [**ADS\_SEARCH\_COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) structure.</span></span> <span data-ttu-id="b7a8f-130">**GetColumn** aloca essa estrutura para você, mas você deve liberá-la usando [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span><span class="sxs-lookup"><span data-stu-id="b7a8f-130">**GetColumn** allocates this structure for you, but you must free it using [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn).</span></span> <span data-ttu-id="b7a8f-131">Chame [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) para concluir a operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-131">Call [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) to complete the search operation.</span></span>

<span data-ttu-id="b7a8f-132">**Para executar uma pesquisa de diretório**</span><span class="sxs-lookup"><span data-stu-id="b7a8f-132">**To perform a directory search**</span></span>

1.  <span data-ttu-id="b7a8f-133">Associar a um provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-133">Bind to an LDAP provider.</span></span> <span data-ttu-id="b7a8f-134">Pode ser um controlador de domínio ou um provedor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-134">It may be a domain controller or a global catalog provider.</span></span>
2.  <span data-ttu-id="b7a8f-135">Recupere a interface com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) com uma chamada para [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Essa operação pode ter sido feita na etapa 1 durante a associação inicial.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-135">Retrieve the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM Interface with a call to [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); this operation may have been done in Step 1 during the initial binding.</span></span>

    <span data-ttu-id="b7a8f-136">Opcionalmente, chame [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) para selecionar opções para manipular os resultados de sua pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-136">Optionally, call [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) to select options for handling the results of your search.</span></span>

3.  <span data-ttu-id="b7a8f-137">Chame [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span><span class="sxs-lookup"><span data-stu-id="b7a8f-137">Call [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).</span></span> <span data-ttu-id="b7a8f-138">Dependendo das opções definidas em [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , isso pode ou não iniciar a execução da consulta.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-138">Depending on the options set in [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) this may, or may not, begin query execution.</span></span>
4.  <span data-ttu-id="b7a8f-139">Chame [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para mover o índice de linha (interno para [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) para a primeira linha.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-139">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to move the row index (internal to [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) to the first row.</span></span>
5.  <span data-ttu-id="b7a8f-140">Leia os dados da linha usando [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)e, em seguida, chame [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) para liberar a memória alocada por **GetColumn**.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-140">Read the data from the row using [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), then call [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) to release the memory allocated by **GetColumn**.</span></span>
6.  <span data-ttu-id="b7a8f-141">Repita a etapa 5 até que todos os dados sejam recuperados do resultado da pesquisa, ou até que [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retorne S \_ anúncios, \_ mais \_ linhas.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-141">Repeat Step 5 until all data is retrieved from the search result, or until [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) returns S\_ADS\_NOMORE\_ROWS.</span></span>
7.  <span data-ttu-id="b7a8f-142">Chame [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) e [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) ao concluir.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-142">Call [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) and [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) when complete.</span></span>

<span data-ttu-id="b7a8f-143">O exemplo de código a seguir mostra esse cenário.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-143">The following code example shows this scenario.</span></span> <span data-ttu-id="b7a8f-144">Para iniciar a associação ao ADSI, chame a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-144">To start binding to ADSI, call the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



<span data-ttu-id="b7a8f-145">Isso fornece um ponteiro para a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-145">This provides a pointer to the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="b7a8f-146">Agora que há uma interface COM para uma instância de IDirectoryInterface, chame [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span><span class="sxs-lookup"><span data-stu-id="b7a8f-146">Now that there is a COM interface for an IDirectoryInterface instance, call [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).</span></span>

<span data-ttu-id="b7a8f-147">Crie uma matriz de nomes de atributo para se preparar para chamar a função [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-147">Build an array of attribute names to prepare to call the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="b7a8f-148">Os nomes de atributo são definidos dentro do esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-148">The attribute names are defined within the schema of Active Directory.</span></span> <span data-ttu-id="b7a8f-149">Para obter mais informações sobre a definição de esquema, consulte [modelo de esquema ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="b7a8f-149">For more information about the schema definition, see [ADSI Schema Model](adsi-schema-model.md).</span></span> <span data-ttu-id="b7a8f-150">Os nomes de atributo listados são retornados, se houver suporte do objeto, como o conjunto de resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-150">The attribute names listed are returned, if supported by the object, as the result set of the search.</span></span>


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



<span data-ttu-id="b7a8f-151">Agora, chame a função [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-151">Now, call the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) function.</span></span> <span data-ttu-id="b7a8f-152">A pesquisa não é executada até que você chame o método [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-152">The search does not run until you call the [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) method.</span></span>


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



<span data-ttu-id="b7a8f-153">Chame [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para iterar linhas no resultado.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-153">Call [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) to iterate rows in the result.</span></span> <span data-ttu-id="b7a8f-154">Em seguida, cada linha é consultada para o atributo "Description".</span><span class="sxs-lookup"><span data-stu-id="b7a8f-154">Each row is then queried for the "description" attribute.</span></span> <span data-ttu-id="b7a8f-155">Se o atributo for encontrado, ele será exibido.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-155">If the attribute is found, it is displayed.</span></span>


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



<span data-ttu-id="b7a8f-156">Para finalizar a pesquisa, chame o método [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .</span><span class="sxs-lookup"><span data-stu-id="b7a8f-156">To end the search, call the [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) method.</span></span>

<span data-ttu-id="b7a8f-157">Lembre-se de que, se um tamanho de página não for definido, o [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) será bloqueado até que todo o conjunto de resultados seja retornado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-157">Be aware that if a page size is not set, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) blocks until the entire result set is returned to the client.</span></span> <span data-ttu-id="b7a8f-158">Se o tamanho da página for definido, os blocos **GetNextRow** até a primeira página (tamanho da página = número de linhas em uma página) serão retornados.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-158">If page size is set, then **GetNextRow** blocks until the first page (page size = number of rows in a page) is returned.</span></span> <span data-ttu-id="b7a8f-159">Se o tamanho da página for definido e a consulta for classificada e você não estiver pesquisando pelo menos um atributo indexado, o valor de tamanho da página será ignorado e o servidor calculará todo o conjunto de resultados antes de retornar os dados.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-159">If page size is set and the query is to be sorted and you are not searching on at least one indexed attribute, then the page size value is ignored, and the server calculates the entire result set prior to returning the data.</span></span> <span data-ttu-id="b7a8f-160">Isso tem o efeito de bloqueio de **GetNextRow** até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-160">This has the effect of **GetNextRow** blocking until the query completes.</span></span>

> [!Note]  
> <span data-ttu-id="b7a8f-161">Para alterar essa consulta de uma pesquisa de diretório para uma pesquisa de catálogo global, a chamada [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) é alterada.</span><span class="sxs-lookup"><span data-stu-id="b7a8f-161">To change this query from a directory search to a global catalog search, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) call is changed.</span></span>

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 