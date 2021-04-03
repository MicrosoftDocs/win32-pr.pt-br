---
title: Especificando outras opções de pesquisa com IDirectorySearch
description: A interface IDirectorySearch fornece controle adicional sobre como a pesquisa é executada por meio do uso de opções de pesquisa.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Especificando outras opções de pesquisa com a ADSI IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915882"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="f2378-105">Especificando outras opções de pesquisa com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="f2378-106">A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornece controle adicional sobre como a pesquisa é executada por meio do uso de opções de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f2378-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="f2378-107">Essas opções de pesquisa são definidas preenchendo uma matriz de estruturas de [**\_ \_ informações do SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e chamando o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="f2378-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="f2378-108">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f2378-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f2378-109">Usando o método SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="f2378-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="f2378-110">Pesquisas síncronas e assíncronas com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-111">Paginação com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-112">Cache de resultados com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-113">Executando uma consulta de escopo de atributo</span><span class="sxs-lookup"><span data-stu-id="f2378-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="f2378-114">Classificando os resultados da pesquisa com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-115">Caça de referência com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-116">Limite de tamanho com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-117">Limite de tempo do servidor com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-118">Limite de tempo do cliente com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="f2378-119">Retornando somente nomes de atributo com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="f2378-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




