---
title: Cache de resultados com IDirectorySearch
description: A \_ preferência de resultados do cache SEARCHPREF do ADS armazena em \_ \_ cache o conjunto de resultados no cliente.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Cache de resultados com ADSI IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, cache de resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291782"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="9ea45-105">Cache de resultados com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="9ea45-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="9ea45-106">A preferência de **\_ \_ \_ resultados do cache SEARCHPREF do ADS** armazena em cache o conjunto de resultados no cliente.</span><span class="sxs-lookup"><span data-stu-id="9ea45-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="9ea45-107">O cache de resultados permite que um aplicativo retenha um conjunto de resultados recuperado e percorra as linhas recuperadas novamente.</span><span class="sxs-lookup"><span data-stu-id="9ea45-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="9ea45-108">Ele também habilita o suporte a cursor em que os métodos [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) e [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) podem ser usados para mover para cima e para baixo o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="9ea45-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="9ea45-109">Por padrão, o cache de resultados está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9ea45-109">By default, result caching is disabled.</span></span> <span data-ttu-id="9ea45-110">O cache de resultados deve ser habilitado se qualquer uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="9ea45-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="9ea45-111">Se o mesmo conjunto de resultados deve ser enumerado várias vezes sem executar a pesquisa novamente no servidor.</span><span class="sxs-lookup"><span data-stu-id="9ea45-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="9ea45-112">Se a execução da pesquisa estiver com uso intensivo de recursos no servidor (conexão lenta, grande conjunto de resultados ou consulta complexa).</span><span class="sxs-lookup"><span data-stu-id="9ea45-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="9ea45-113">Se o suporte ao cursor for necessário.</span><span class="sxs-lookup"><span data-stu-id="9ea45-113">If cursor support is required.</span></span>

<span data-ttu-id="9ea45-114">Desative o cache se seu aplicativo precisar reduzir os requisitos de memória para armazenar em cache um grande conjunto de resultados no cliente.</span><span class="sxs-lookup"><span data-stu-id="9ea45-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="9ea45-115">O cache de resultados aumenta os requisitos de memória no cliente, portanto, o cache de resultados deve ser desabilitado se isso for uma preocupação.</span><span class="sxs-lookup"><span data-stu-id="9ea45-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="9ea45-116">Para habilitar o cache de resultados, defina uma opção de pesquisa de **\_ \_ \_ resultados do cache SEARCHPREF do ADS** com um valor **\_ booliano de ADSTYPE** **true** na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="9ea45-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="9ea45-117">O exemplo de código a seguir mostra como habilitar o cache de resultados.</span><span class="sxs-lookup"><span data-stu-id="9ea45-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




