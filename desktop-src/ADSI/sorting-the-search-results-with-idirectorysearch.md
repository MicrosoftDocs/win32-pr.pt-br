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
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="f49ae-106">Classificando os resultados da pesquisa com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f49ae-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="f49ae-107">Por padrão, os resultados de uma pesquisa são retornados em nenhuma ordem garantida.</span><span class="sxs-lookup"><span data-stu-id="f49ae-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="f49ae-108">O **ADS \_ SEARCHPREF \_ classificar \_ em** preferência instrui o servidor a classificar o conjunto de resultados em um valor de atributo especificado antes que ele seja retornado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="f49ae-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="f49ae-109">É recomendável que os atributos indexados sejam usados para classificação.</span><span class="sxs-lookup"><span data-stu-id="f49ae-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="f49ae-110">Caso contrário, o servidor deve recuperar o conjunto de resultados completo e classificá-lo antes de enviar qualquer resultado para o cliente.</span><span class="sxs-lookup"><span data-stu-id="f49ae-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="f49ae-111">Isso também se aplica a pesquisas paginadas.</span><span class="sxs-lookup"><span data-stu-id="f49ae-111">This also applies to paged searches.</span></span> <span data-ttu-id="f49ae-112">Lembre-se de que o desempenho de uma pesquisa classificada será aumentado se o filtro incluir um atributo indexado e esse atributo for especificado como a chave de classificação; Nesse caso, Active Directory pode atender à classificação durante o processamento do filtro.</span><span class="sxs-lookup"><span data-stu-id="f49ae-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="f49ae-113">Por exemplo, uma consulta de classificação eficiente para um conjunto de usuários poderia ter um filtro que incluía (SN>Smith) e uma chave de classificação de sn.</span><span class="sxs-lookup"><span data-stu-id="f49ae-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="f49ae-114">A classificação do lado do servidor com a opção **\_ SEARCHPREF \_ classificar \_ na** pesquisa do ADS reduzirá o desempenho do servidor.</span><span class="sxs-lookup"><span data-stu-id="f49ae-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="f49ae-115">Se você estiver executando muitas pesquisas, considere classificar os resultados manualmente no lado do cliente para reduzir a carga de trabalho no servidor.</span><span class="sxs-lookup"><span data-stu-id="f49ae-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="f49ae-116">Por padrão, a classificação de resultados está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f49ae-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="f49ae-117">Para habilitar a classificação de resultado, defina um **\_ SEARCHPREF \_ de anúncios classificar \_ na** opção de pesquisa com um **ADSTYPE \_ Prov \_ específico** que aponte para uma estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="f49ae-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="f49ae-118">A estrutura de **\_ SORTKEY do ADS** é usada para especificar o atributo a ser classificado e a ordem da classificação.</span><span class="sxs-lookup"><span data-stu-id="f49ae-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="f49ae-119">O exemplo de código a seguir mostra como habilitar a classificação de resultado.</span><span class="sxs-lookup"><span data-stu-id="f49ae-119">The following code example shows how to enable result sorting.</span></span>


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



<span data-ttu-id="f49ae-120">Active Directory não dá suporte à classificação em atributos construídos, portanto não é possível especificar um atributo construído para classificação.</span><span class="sxs-lookup"><span data-stu-id="f49ae-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="f49ae-121">O atributo [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) também não pode ser usado para classificação.</span><span class="sxs-lookup"><span data-stu-id="f49ae-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="f49ae-122">Active Directory também não permite a classificação em mais de um atributo, portanto, a opção **ad \_ SEARCHPREF \_ Sort \_ on** Search pode conter apenas uma estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .</span><span class="sxs-lookup"><span data-stu-id="f49ae-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 