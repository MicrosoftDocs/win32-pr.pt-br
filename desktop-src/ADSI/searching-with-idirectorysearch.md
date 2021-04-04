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
# <a name="searching-with-the-idirectorysearch-interface"></a>Pesquisando com a interface IDirectorySearch

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece uma interface de alto nível e baixa sobrecarga para consultar dados de um diretório ou de um catálogo global. A interface com **IDirectorySearch** pode ser usada somente com uma vtable e, portanto, não está disponível para ambientes de desenvolvimento baseados em automação.

**Para executar uma pesquisa**

1.  Associar a um objeto no diretório.
2.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter o ponteiro [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .
3.  Execute a pesquisa usando o ponteiro [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Chame o método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) e passe um filtro de pesquisa, os nomes de atributo solicitados e outros parâmetros.

Para obter mais informações sobre a sintaxe do filtro de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).

A execução da consulta é específica do provedor. Com alguns provedores, a execução da consulta real não ocorre até que [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) seja chamado. A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funciona diretamente com filtros de pesquisa. Nem o dialeto SQL nem o dialeto LDAP são necessários.

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece métodos para enumerar o conjunto de resultados, linha por linha. O método [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera a primeira linha e [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) move você para a próxima linha da linha atual. Quando você tiver atingido a última linha, chamar esses métodos retornará o \_ código de erro S anúncios de \_ mais \_ linhas. Por outro lado, [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) o move de volta uma linha por vez. Um valor de retorno de anúncios de S \_ \_ mais \_ linhas indica que você atingiu a primeira linha do conjunto de resultados. Esses métodos operam no conjunto de resultados, residente na memória, no cliente. Assim, quando pesquisas paginadas e assíncronas são executadas e a \_ opção de resultados de cache \_ é desativada, a rolagem regressiva pode ter consequências inesperadas.

Quando você localizar a linha apropriada, chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para obter itens de dados, coluna por coluna. Para cada chamada, você passa o nome da coluna de interesse. O item de dados retornado é um ponteiro para uma estrutura de [**\_ \_ coluna de pesquisa do ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) . **GetColumn** aloca essa estrutura para você, mas você deve liberá-la usando [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Chame [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) para concluir a operação de pesquisa.

**Para executar uma pesquisa de diretório**

1.  Associar a um provedor LDAP. Pode ser um controlador de domínio ou um provedor de catálogo global.
2.  Recupere a interface com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) com uma chamada para [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Essa operação pode ter sido feita na etapa 1 durante a associação inicial.

    Opcionalmente, chame [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) para selecionar opções para manipular os resultados de sua pesquisa.

3.  Chame [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch). Dependendo das opções definidas em [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , isso pode ou não iniciar a execução da consulta.
4.  Chame [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para mover o índice de linha (interno para [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) para a primeira linha.
5.  Leia os dados da linha usando [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)e, em seguida, chame [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) para liberar a memória alocada por **GetColumn**.
6.  Repita a etapa 5 até que todos os dados sejam recuperados do resultado da pesquisa, ou até que [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retorne S \_ anúncios, \_ mais \_ linhas.
7.  Chame [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) e [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) ao concluir.

O exemplo de código a seguir mostra esse cenário. Para iniciar a associação ao ADSI, chame a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


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



Isso fornece um ponteiro para a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

Agora que há uma interface COM para uma instância de IDirectoryInterface, chame [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Crie uma matriz de nomes de atributo para se preparar para chamar a função [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . Os nomes de atributo são definidos dentro do esquema de Active Directory. Para obter mais informações sobre a definição de esquema, consulte [modelo de esquema ADSI](adsi-schema-model.md). Os nomes de atributo listados são retornados, se houver suporte do objeto, como o conjunto de resultados da pesquisa.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Agora, chame a função [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . A pesquisa não é executada até que você chame o método [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Chame [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para iterar linhas no resultado. Em seguida, cada linha é consultada para o atributo "Description". Se o atributo for encontrado, ele será exibido.


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



Para finalizar a pesquisa, chame o método [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .

Lembre-se de que, se um tamanho de página não for definido, o [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) será bloqueado até que todo o conjunto de resultados seja retornado ao cliente. Se o tamanho da página for definido, os blocos **GetNextRow** até a primeira página (tamanho da página = número de linhas em uma página) serão retornados. Se o tamanho da página for definido e a consulta for classificada e você não estiver pesquisando pelo menos um atributo indexado, o valor de tamanho da página será ignorado e o servidor calculará todo o conjunto de resultados antes de retornar os dados. Isso tem o efeito de bloqueio de **GetNextRow** até que a consulta seja concluída.

> [!Note]  
> Para alterar essa consulta de uma pesquisa de diretório para uma pesquisa de catálogo global, a chamada [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) é alterada.

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 