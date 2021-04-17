---
title: Limite de tamanho com IDirectorySearch
description: O cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite de tamanho com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, limite de tamanho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748293"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="9a767-105">Limite de tamanho com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="9a767-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="9a767-106">Para reduzir o requisito de memória ou para outras finalidades, o cliente pode se concentrar em um pequeno número de objetos retornados do servidor e ignorar o restante do conjunto de resultados que não são de interesse.</span><span class="sxs-lookup"><span data-stu-id="9a767-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="9a767-107">Para fazer isso, o cliente especifica o limite de tamanho de pesquisa e outros critérios de pesquisa apropriados.</span><span class="sxs-lookup"><span data-stu-id="9a767-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="9a767-108">Por exemplo, se o diretório armazena as pontuações de teste de um distrito escolar, você pode consultar os dez principais alunos com as pontuações de teste mais altas especificando um limite de tamanho de dez (10) e uma ordem de classificação decrescente.</span><span class="sxs-lookup"><span data-stu-id="9a767-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="9a767-109">O limite de tamanho padrão é sem limite.</span><span class="sxs-lookup"><span data-stu-id="9a767-109">The default for size limit is no limit.</span></span> <span data-ttu-id="9a767-110">Para definir um limite de tamanho, defina uma opção de pesquisa de **\_ limite de \_ tamanho \_ do ADS SEARCHPREF** com um valor **\_ inteiro de ADSTYPE** que contenha o tamanho máximo na matriz de [**informações de \_ SEARCHPREF \_ de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="9a767-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="9a767-111">O exemplo de código a seguir mostra como definir o limite de tamanho.</span><span class="sxs-lookup"><span data-stu-id="9a767-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="9a767-112">Um valor de limite de tamanho igual A zero indica que não há limite de tamanho.</span><span class="sxs-lookup"><span data-stu-id="9a767-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="9a767-113">Por Active Directory, o limite de tamanho especifica o número máximo de objetos a serem retornados pela pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a767-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="9a767-114">Além disso, para Active Directory, o número máximo de objetos retornados por uma pesquisa é de 1000 objetos.</span><span class="sxs-lookup"><span data-stu-id="9a767-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




