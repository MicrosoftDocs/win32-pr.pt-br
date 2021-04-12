---
title: Pesquisas síncronas e assíncronas com IDirectorySearch
description: Quando você executa uma pesquisa usando a interface IDirectorySearch, o método IDirectorySearch ExecuteSearch não envia a solicitação de pesquisa para o servidor.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Pesquisas síncronas e assíncronas com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, pesquisas síncronas e assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363645"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="13419-105">Pesquisas síncronas e assíncronas com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="13419-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="13419-106">Quando você executa uma pesquisa usando a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , o método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) não envia a solicitação de pesquisa para o servidor.</span><span class="sxs-lookup"><span data-stu-id="13419-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="13419-107">Esse método salva apenas os parâmetros de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="13419-107">This method only saves the search parameters.</span></span> <span data-ttu-id="13419-108">A solicitação de pesquisa é realmente enviada quando você chama [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span><span class="sxs-lookup"><span data-stu-id="13419-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="13419-109">Para pesquisas de Active Directory, a principal diferença entre síncrona e assíncrona é quando a primeira linha do resultado é retornada, ou seja, quando a primeira chamada [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retorna.</span><span class="sxs-lookup"><span data-stu-id="13419-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="13419-110">Em uma pesquisa síncrona, se a paginação não estiver habilitada, a primeira linha será retornada quando o servidor tiver construído e retornado o conjunto de resultados inteiro para o cliente.</span><span class="sxs-lookup"><span data-stu-id="13419-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="13419-111">Se a paginação estiver habilitada, a primeira linha será retornada quando a primeira página do conjunto de resultados for retornada.</span><span class="sxs-lookup"><span data-stu-id="13419-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="13419-112">Em uma pesquisa assíncrona, se a paginação não estiver habilitada, a primeira linha será retornada quando o servidor tiver construído a primeira linha do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="13419-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="13419-113">Se a paginação estiver habilitada, a primeira linha será retornada quando a primeira página do conjunto de resultados for retornada.</span><span class="sxs-lookup"><span data-stu-id="13419-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="13419-114">O tipo de pesquisa padrão é síncrono.</span><span class="sxs-lookup"><span data-stu-id="13419-114">The default search type is synchronous.</span></span> <span data-ttu-id="13419-115">Para especificar uma pesquisa assíncrona, defina uma opção de pesquisa **\_ \_ assíncrona do ADS SEARCHPREF** com um valor **\_ booliano de ADSTYPE** **true** na matriz de [**informações de \_ SEARCHPREF \_ do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="13419-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="13419-116">Essa operação é mostrada no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="13419-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




