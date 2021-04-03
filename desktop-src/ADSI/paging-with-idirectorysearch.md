---
title: Paginação com IDirectorySearch
description: A paginação especifica quantas linhas o servidor retorna ao cliente.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paginação com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, paginação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915892"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="88e72-105">Paginação com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="88e72-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="88e72-106">A paginação especifica quantas linhas o servidor retorna ao cliente.</span><span class="sxs-lookup"><span data-stu-id="88e72-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="88e72-107">Uma página pode ser definida pelo número de linhas ou um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="88e72-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="88e72-108">O objeto COM ADSI recupera cada página de resultados com base nos valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="88e72-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="88e72-109">O chamador chama [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) quando atingiu o final da página e o objeto com ADSI recupera a próxima página.</span><span class="sxs-lookup"><span data-stu-id="88e72-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="88e72-110">Valor</span><span class="sxs-lookup"><span data-stu-id="88e72-110">Value</span></span>                                   | <span data-ttu-id="88e72-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="88e72-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e72-112">**PageSize do ADS \_ SEARCHPREF \_**</span><span class="sxs-lookup"><span data-stu-id="88e72-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="88e72-113">Especifica o número máximo de linhas a serem retornadas em uma página.</span><span class="sxs-lookup"><span data-stu-id="88e72-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="88e72-114">**\_limite de \_ tempo paginado do ADS SEARCHPREF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="88e72-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="88e72-115">Especifica o tempo máximo, em segundos, que o servidor deve gastar para coletar uma página de resultados antes de retornar a página para o cliente.</span><span class="sxs-lookup"><span data-stu-id="88e72-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="88e72-116">Se o limite for atingido, o servidor parará a pesquisa e retornará as linhas já recuperadas para a página.</span><span class="sxs-lookup"><span data-stu-id="88e72-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="88e72-117">Se nenhuma dessas preferências de pesquisa for definida, o padrão será nenhuma paginação.</span><span class="sxs-lookup"><span data-stu-id="88e72-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="88e72-118">As pesquisas do Active Directory executadas sem paginação são limitadas a retornar um máximo dos primeiros 1000 registros, portanto, você deve usar uma pesquisa paginada se houver a possibilidade de que o conjunto de resultados contenha mais de 1000 itens.</span><span class="sxs-lookup"><span data-stu-id="88e72-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="88e72-119">Uma operação de pesquisa pode resultar em um grande número de objetos retornados.</span><span class="sxs-lookup"><span data-stu-id="88e72-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="88e72-120">Se o servidor retornar o resultado em um conjunto, ele poderá diminuir o desempenho do cliente e do servidor, bem como afetar a carga de rede.</span><span class="sxs-lookup"><span data-stu-id="88e72-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="88e72-121">Pesquisas paginadas podem ser usadas para evitar isso.</span><span class="sxs-lookup"><span data-stu-id="88e72-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="88e72-122">Em uma pesquisa paginada, o cliente pode aceitar resultados em pacotes menores.</span><span class="sxs-lookup"><span data-stu-id="88e72-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="88e72-123">O tamanho de um pacote é conhecido como o tamanho da página de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="88e72-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="88e72-124">As pesquisas paginadas oferecem benefícios ao cliente e ao servidor.</span><span class="sxs-lookup"><span data-stu-id="88e72-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="88e72-125">O cliente pode ser mais responsivo na apresentação dos resultados para os usuários.</span><span class="sxs-lookup"><span data-stu-id="88e72-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="88e72-126">Isso é especialmente relevante para as ferramentas gráficas de interface do usuário que podem iniciar o processo de exibição da janela enquanto o outro thread recebe os dados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="88e72-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="88e72-127">No lado do servidor, as pesquisas paginadas tornam a operação escalonável.</span><span class="sxs-lookup"><span data-stu-id="88e72-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="88e72-128">Por exemplo, se 100 clientes emitirem solicitações de pesquisa simultaneamente e, na média, cada cliente receberá 200 objetos.</span><span class="sxs-lookup"><span data-stu-id="88e72-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="88e72-129">Se nenhum tamanho de página for especificado, no pior cenário, o servidor deverá ter memória suficiente para conter 20.000 objetos.</span><span class="sxs-lookup"><span data-stu-id="88e72-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="88e72-130">Por outro lado, se cada cliente especifica um tamanho de página, por exemplo, dez objetos, o requisito de memória no servidor é reduzido por um fator de 20.</span><span class="sxs-lookup"><span data-stu-id="88e72-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="88e72-131">Além disso, usando uma pesquisa paginada, um cliente pode abandonar a operação em andamento.</span><span class="sxs-lookup"><span data-stu-id="88e72-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="88e72-132">Por outro lado, em uma pesquisa não paginável, o cliente recebe um conjunto de resultados em um pacote.</span><span class="sxs-lookup"><span data-stu-id="88e72-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="88e72-133">Isso pode diminuir o desempenho da rede.</span><span class="sxs-lookup"><span data-stu-id="88e72-133">This can decrease network performance.</span></span>

<span data-ttu-id="88e72-134">A ADSI manipula o tamanho da página para o cliente.</span><span class="sxs-lookup"><span data-stu-id="88e72-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="88e72-135">O cliente não precisa contar o número de objetos em andamento.</span><span class="sxs-lookup"><span data-stu-id="88e72-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="88e72-136">A ADSI encapsula a interação do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="88e72-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="88e72-137">Da perspectiva do cliente, a pesquisa retorna um conjunto de resultados completo.</span><span class="sxs-lookup"><span data-stu-id="88e72-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="88e72-138">É recomendável que a paginação seja usada.</span><span class="sxs-lookup"><span data-stu-id="88e72-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="88e72-139">Para especificar um tamanho máximo de página, defina uma opção de pesquisa do **ADS \_ SEARCHPREF \_ PageSize** com um valor **\_ inteiro ADSTYPE** definido como o número máximo de linhas por página na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="88e72-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="88e72-140">O exemplo de código a seguir mostra como definir o tamanho máximo da página.</span><span class="sxs-lookup"><span data-stu-id="88e72-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="88e72-141">Para especificar um tempo de página, defina uma opção de pesquisa de **\_ \_ \_ \_ limite de tempo paginado do ADS SEARCHPREF** com um valor **\_ inteiro de ADSTYPE** definido como o número máximo de segundos que o servidor deve gastar para recuperar uma página na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="88e72-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="88e72-142">O exemplo de código a seguir mostra como especificar o tempo de página.</span><span class="sxs-lookup"><span data-stu-id="88e72-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




