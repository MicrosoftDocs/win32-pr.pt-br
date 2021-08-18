---
title: Pesquisando com a interface IDirectorySearch
description: A interface IDirectorySearch fornece uma interface de alto nível e baixa sobrecarga para consultar dados de um diretório ou um catálogo global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Pesquisando com a INTERFACE IDirectorySearch ADSI
- Consultas ADSI, interfaces de consulta, IDirectorySearch
- ADSI ADSI , código de exemplo C/C++, pesquisando um diretório com IDirectorySearch
- IDirectorySearch ADSI , usando para pesquisar um diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46700c48f82955bd01967808cd30f2fa078e3b6c998fb3beaac4bf7c7fe8707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023214"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Pesquisando com a interface IDirectorySearch

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece uma interface de alto nível e baixa sobrecarga para consultar dados de um diretório ou um catálogo global. A interface **COM IDirectorySearch** só pode ser usada com uma vtable e, portanto, não está disponível para ambientes de desenvolvimento baseados em Automação.

**Para executar uma pesquisa**

1.  A bind a um objeto no diretório .
2.  Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter o ponteiro [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
3.  Execute a pesquisa usando o [**ponteiro IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Chame o [**método IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) e passe um filtro de pesquisa, os nomes de atributo solicitados e outros parâmetros.

Para obter mais informações sobre a sintaxe de filtro de pesquisa, consulte [Sintaxe de filtro de pesquisa](search-filter-syntax.md).

A execução da consulta é específica do provedor. Com alguns provedores, a execução real da consulta não ocorre até [**que IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) [**ou IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) seja chamado. A [**interface IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) funciona diretamente com filtros de pesquisa. Nem o dialeto SQL nem o dialeto LDAP são necessários.

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece métodos para enumerar o conjunto de resultados, linha por linha. O [**método IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) recupera a primeira linha e [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) move você para a próxima linha da linha atual. Quando você tiver atingido a última linha, chamar esses métodos retornará o código de erro S \_ ADS \_ NOMORE \_ ROWS. Por outro lado, [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) move você de volta uma linha por vez. Um valor de retorno S \_ ADS \_ NOMORE ROWS indica que você atingiu a primeira linha do conjunto \_ de resultados. Esses métodos operam no conjunto de resultados, residentes na memória, no cliente. Portanto, quando pesquisas pagedas e assíncronas são executadas e a opção CACHE RESULTS é desligada, a rolagem regressiva pode ter \_ \_ consequências inesperadas.

Quando você localizar a linha apropriada, chame [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para obter itens de dados, coluna por coluna. Para cada chamada, você passa o nome da coluna de interesse. O item de dados retornado é um ponteiro para uma [**estrutura ADS \_ SEARCH \_ COLUMN.**](/windows/desktop/api/Iads/ns-iads-ads_search_column) **GetColumn** aloca essa estrutura para você, mas você deve liberar usando [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Chame [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) para concluir a operação de pesquisa.

**Para executar uma pesquisa de diretório**

1.  A vincular a um provedor LDAP. Pode ser um controlador de domínio ou um provedor de catálogo global.
2.  Recupere a [**interface COM IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) com uma chamada [**para QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); essa operação pode ter sido feita na Etapa 1 durante a associação inicial.

    Opcionalmente, chame [**SetSearchPreference para**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) selecionar opções para lidar com os resultados da pesquisa.

3.  Chame [**ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) Dependendo das opções definidas em [**SetSearchPreference,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) isso pode ou não iniciar a execução da consulta.
4.  Chame [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para mover o índice de linha (interno [**para IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) para a primeira linha.
5.  Leia os dados da linha usando [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)e, em seguida, chame [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) para liberar a memória alocada por **GetColumn.**
6.  Repita a Etapa 5 até que todos os dados são recuperados do resultado da pesquisa ou até [**que GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retorne S \_ ADS \_ NOMORE \_ ROWS.
7.  Chame [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) e [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) quando concluir.

O exemplo de código a seguir mostra esse cenário. Para iniciar a associação ao ADSI, chame [**a função ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)


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



Isso fornece um ponteiro para a interface [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Agora que há uma interface COM para uma instância IDirectoryInterface, chame [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Crie uma matriz de nomes de atributo para se preparar para chamar a [**função IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) Os nomes de atributo são definidos dentro do esquema do Active Directory. Para obter mais informações sobre a definição de esquema, consulte [Modelo de esquema ADSI](adsi-schema-model.md). Os nomes de atributo listados são retornados, se suportados pelo objeto , como o conjunto de resultados da pesquisa.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



Agora, chame a [**função ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) A pesquisa não é executado até que você chame o [**método GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Chame [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) para iterar linhas no resultado. Em seguida, cada linha é consultada para o atributo "description". Se o atributo for encontrado, ele será exibido.


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



Para encerrar a pesquisa, chame o [**método AbandonSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch)

Esteja ciente de que, se um tamanho de página não for definido, [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) bloqueará até que todo o conjunto de resultados seja retornado ao cliente. Se o tamanho da página for definido, **GetNextRow** bloqueará até que a primeira página (tamanho da página = número de linhas em uma página) seja retornada. Se o tamanho da página for definido e a consulta for classificar e você não estiver pesquisando pelo menos um atributo indexado, o valor do tamanho da página será ignorado e o servidor calculará todo o conjunto de resultados antes de retornar os dados. Isso tem o efeito do **bloqueio GetNextRow** até que a consulta seja concluída.

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



 

 