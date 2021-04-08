---
title: Usando o método SetSearchPreference
description: Chamar o método IDirectorySearch SetSearchPreference altera a maneira como os resultados da pesquisa são obtidos e apresentados por meio da interface IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI, usando o método SetSearchPreference
- ADSI ADSI, código de exemplo C/C++, usando o método SetSearchPreference
- consulta ADSI, usando SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004848"
---
# <a name="using-the-setsearchpreference-method"></a><span data-ttu-id="bf605-106">Usando o método SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="bf605-106">Using the SetSearchPreference Method</span></span>

<span data-ttu-id="bf605-107">Chamar o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) altera a maneira como os resultados da pesquisa são obtidos e apresentados por meio da interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="bf605-107">Calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method changes the way in which the search results are obtained and presented through the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="bf605-108">A documentação do SDK define [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bf605-108">The SDK documentation defines [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) as follows:</span></span>


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



<span data-ttu-id="bf605-109">Várias preferências podem ser definidas passando uma matriz como o primeiro parâmetro e o tamanho da matriz como o segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bf605-109">Multiple preferences may be set by passing an array as the first parameter and the array size as the second parameter.</span></span>


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



<span data-ttu-id="bf605-110">Este exemplo define o tamanho da página como 100 linhas e o escopo para o \_ tipo de subárvore de escopo ADS \_ .</span><span class="sxs-lookup"><span data-stu-id="bf605-110">This example sets the page size to 100 rows and the scope to the ADS\_SCOPE\_SUBTREE type.</span></span> <span data-ttu-id="bf605-111">A configuração tamanho da página faz com que o servidor retorne imediatamente os dados para o cliente, depois de 100 linhas terem sido calculadas.</span><span class="sxs-lookup"><span data-stu-id="bf605-111">The page size setting causes the server to immediately return data to the client, after 100 rows have been calculated.</span></span> <span data-ttu-id="bf605-112">A \_ \_ configuração subárvore do escopo ADS faz com que a pesquisa abranja todas as ramificações na árvore abaixo do ponto em que a pesquisa está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="bf605-112">The ADS\_SCOPE\_SUBTREE setting causes the search to encompass all branches in the tree below the point from which the search is being executed.</span></span>

 

 




