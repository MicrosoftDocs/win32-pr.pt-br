---
title: Exemplo de código para pesquisar atributos
description: O exemplo de código a seguir mostra como usar a \_ única preferência de pesquisa do ADS SEARCHPREF \_ ATTRIBTYPES \_ somente para recuperar os nomes dos atributos aos quais os valores foram atribuídos.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, código de exemplo C/C++, pesquisando atributos
- Exemplo de código para pesquisar atributos
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, retornando apenas nomes de atributo, código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207fcfd2bd688f5bb6ddcd19dcb9b1a87a2e40ddb0a7db1e63e9457e671f9947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428459"
---
# <a name="example-code-for-searching-for-attributes"></a>Exemplo de código para pesquisar atributos

O exemplo de código a seguir mostra como usar a única preferência de pesquisa do **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ somente** para recuperar os nomes dos atributos aos quais os valores foram atribuídos. O exemplo Inicializa uma estrutura de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e define a preferência de pesquisa chamando o método [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) da interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Em seguida, o exemplo chama o método [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) para executar a pesquisa.


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




