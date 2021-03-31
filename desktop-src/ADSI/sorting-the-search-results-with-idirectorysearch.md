---
title: Classificando os resultados da pesquisa com IDirectorySearch
description: Por padrão, os resultados de uma pesquisa são retornados em nenhuma ordem garantida. O ADS \_ SEARCHPREF \_ classificar \_ em preferência instrui o servidor a classificar o conjunto de resultados em um valor de atributo especificado antes que ele seja retornado ao cliente.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Classificando os resultados da pesquisa com IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, classificando resultados da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641834"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Classificando os resultados da pesquisa com IDirectorySearch

Por padrão, os resultados de uma pesquisa são retornados em nenhuma ordem garantida. O **ADS \_ SEARCHPREF \_ classificar \_ em** preferência instrui o servidor a classificar o conjunto de resultados em um valor de atributo especificado antes que ele seja retornado ao cliente.

É recomendável que os atributos indexados sejam usados para classificação. Caso contrário, o servidor deve recuperar o conjunto de resultados completo e classificá-lo antes de enviar qualquer resultado para o cliente. Isso também se aplica a pesquisas paginadas. Lembre-se de que o desempenho de uma pesquisa classificada será aumentado se o filtro incluir um atributo indexado e esse atributo for especificado como a chave de classificação; Nesse caso, Active Directory pode atender à classificação durante o processamento do filtro. Por exemplo, uma consulta de classificação eficiente para um conjunto de usuários poderia ter um filtro que incluía (SN>Smith) e uma chave de classificação de sn.

A classificação do lado do servidor com a opção **\_ SEARCHPREF \_ classificar \_ na** pesquisa do ADS reduzirá o desempenho do servidor. Se você estiver executando muitas pesquisas, considere classificar os resultados manualmente no lado do cliente para reduzir a carga de trabalho no servidor.

Por padrão, a classificação de resultados está desabilitada. Para habilitar a classificação de resultado, defina um **\_ SEARCHPREF \_ de anúncios classificar \_ na** opção de pesquisa com um **ADSTYPE \_ Prov \_ específico** que aponte para uma estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . A estrutura de **\_ SORTKEY do ADS** é usada para especificar o atributo a ser classificado e a ordem da classificação.

O exemplo de código a seguir mostra como habilitar a classificação de resultado.


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



Active Directory não dá suporte à classificação em atributos construídos, portanto não é possível especificar um atributo construído para classificação. O atributo [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) também não pode ser usado para classificação. Active Directory também não permite a classificação em mais de um atributo, portanto, a opção **ad \_ SEARCHPREF \_ Sort \_ on** Search pode conter apenas uma estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .

 

 