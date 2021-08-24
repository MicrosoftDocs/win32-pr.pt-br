---
title: Classificação dos resultados da pesquisa com IDirectorySearch
description: Por padrão, os resultados de uma pesquisa são retornados em nenhuma ordem garantida. A preferência ADS SEARCHPREF SORT ON instrui o servidor a classificar o conjunto de resultados em um valor de atributo especificado antes que ele seja \_ \_ retornado ao \_ cliente.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Classificação dos resultados da pesquisa com IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, classificação de resultados da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7864a3878d2cdc44d58c6f6090f6b791b9fe29b3d2613e6e3d4aaf0b6289e100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443866"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Classificação dos resultados da pesquisa com IDirectorySearch

Por padrão, os resultados de uma pesquisa são retornados em nenhuma ordem garantida. A **preferência ADS \_ SEARCHPREF \_ SORT \_ ON** instrui o servidor a classificar o conjunto de resultados em um valor de atributo especificado antes que ele seja retornado ao cliente.

É recomendável que os atributos indexados sejam usados para classificação. Caso contrário, o servidor deverá recuperar o conjunto de resultados completo e classificar antes de enviar os resultados ao cliente. Isso também se aplica a pesquisas pagedas. Esteja ciente de que o desempenho de uma pesquisa classificação será aumentado se o filtro incluir um atributo indexado e esse atributo for especificado como a chave de classificação; nesse caso, o Active Directory pode satisfazer a classificação durante o processamento do filtro. Por exemplo, uma consulta de classificação eficiente para um conjunto de usuários pode ter um filtro que inclui (sn>smith) e uma chave de classificação de sn.

A classificação do lado do servidor com a **opção de pesquisa ADS \_ SEARCHPREF \_ SORT \_ ON** reduzirá o desempenho do servidor. Se você estiver executando muitas pesquisas, considere classificar os resultados manualmente no lado do cliente para reduzir a carga de trabalho no servidor.

Por padrão, a classificação de resultados está desabilitada. Para habilitar a classificação de resultados, de definir uma opção de pesquisa **ADS \_ SEARCHPREF \_ SORT \_ ON** com um **ADSTYPE \_ PROV \_ SPECIFIC** que aponta para uma estrutura [**\_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) ads na matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) A **estrutura \_ SORTKEY do ADS** é usada para especificar o atributo a ser classificados e a ordem da classificação.

O exemplo de código a seguir mostra como habilitar a classificação de resultados.


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



O Active Directory não dá suporte à classificação em atributos construídos, portanto, não é possível especificar um atributo construído para classificação. O [**atributo distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) também não pode ser usado para classificação. O Active Directory também não permite a classificação em mais de um atributo, portanto, a opção de pesquisa **ADS \_ SEARCHPREF \_ SORT \_ ON** só pode conter uma estrutura [**\_ SORTKEY ads.**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)

 

 