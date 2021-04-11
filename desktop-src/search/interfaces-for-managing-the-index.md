---
description: 'O Windows Search permite que você gerencie o índice do Windows Search com três componentes principais: Gerenciador de pesquisa, Gerenciador de catálogo e Gerenciador de escopo de rastreamento.'
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para gerenciar o índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164328"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="d2320-103">Interfaces para gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="d2320-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="d2320-104">O Windows Search permite que você gerencie o índice do Windows Search com três componentes principais: Gerenciador de pesquisa, Gerenciador de catálogo e Gerenciador de escopo de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="d2320-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="d2320-105">Algumas dessas interfaces de gerenciamento podem ser usadas com privilégios de usuário padrão, mas as que alteram o estado do índice exigem privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="d2320-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="d2320-106">Sobre as interfaces para gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="d2320-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2320-107">Componente</span><span class="sxs-lookup"><span data-stu-id="d2320-107">Component</span></span></th>
<th><span data-ttu-id="d2320-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d2320-108">Interfaces</span></span></th>
<th><span data-ttu-id="d2320-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2320-110">Gerenciador de pesquisa</span><span class="sxs-lookup"><span data-stu-id="d2320-110">Search Manager</span></span></td>
<td><span data-ttu-id="d2320-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="d2320-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="d2320-112">Fornece métodos para recuperar e definir informações sobre o Windows Search:</span><span class="sxs-lookup"><span data-stu-id="d2320-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="d2320-113">Obter uma instância do Gerenciador de catálogo para um catálogo específico.</span><span class="sxs-lookup"><span data-stu-id="d2320-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="d2320-114">Obter ou definir informações de proxy.</span><span class="sxs-lookup"><span data-stu-id="d2320-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="d2320-115">Obtendo informações de versão sobre o mecanismo de pesquisa do Windows.</span><span class="sxs-lookup"><span data-stu-id="d2320-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="d2320-116">Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-searchmanager.md">usando o Gerenciador de pesquisa</a>.</span><span class="sxs-lookup"><span data-stu-id="d2320-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2320-117">Gerenciador de catálogos</span><span class="sxs-lookup"><span data-stu-id="d2320-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="d2320-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="d2320-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="d2320-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="d2320-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="d2320-120">Fornece métodos para gerenciar um catálogo de pesquisa individual, como causar uma nova indexação ou definir tempos limite.</span><span class="sxs-lookup"><span data-stu-id="d2320-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="d2320-121">Essa interface gerencia o catálogo em quatro áreas:</span><span class="sxs-lookup"><span data-stu-id="d2320-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="d2320-122">Conteúdo do catálogo – garantindo que novos dados sejam indexados e que outros aplicativos e componentes funcionem corretamente, forçando uma reindexação de todo ou parte do catálogo ou redefinindo o catálogo inteiro.</span><span class="sxs-lookup"><span data-stu-id="d2320-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="d2320-123">Propriedades do catálogo – definir propriedades que determinam como o catálogo gerencia os tempos limite ao se conectar a manipuladores de protocolo e como as marcas de diacríticos são tratadas em pesquisas.</span><span class="sxs-lookup"><span data-stu-id="d2320-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="d2320-124">Status do catálogo-obtendo informações sobre o catálogo, incluindo status, tamanho e estado da atividade atual.</span><span class="sxs-lookup"><span data-stu-id="d2320-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="d2320-125">Acesso a outras interfaces – recuperando outras interfaces relacionadas à pesquisa exigidas pelo Gerenciador de escopo de rastreamento, notificações de alteração de dados e a interface <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2320-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="d2320-126">Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-catalog-manager.md">usando o Gerenciador de catálogo</a>.</span><span class="sxs-lookup"><span data-stu-id="d2320-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2320-127">Gerenciador de escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="d2320-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="d2320-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2320-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="d2320-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="d2320-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="d2320-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2320-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="d2320-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="d2320-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="d2320-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2320-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="d2320-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2320-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="d2320-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="d2320-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="d2320-135">Fornece métodos para informar o mecanismo de pesquisa sobre contêineres para rastreamento ou inspeção e itens sob esses contêineres para incluir ou excluir no índice.</span><span class="sxs-lookup"><span data-stu-id="d2320-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="d2320-136">Você também pode consultar o Gerenciador de escopo de rastreamento para ver se uma URL específica está no escopo do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="d2320-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="d2320-137">Para obter mais informações, consulte <a href="-search-3x-wds-extidx-csm.md">usando o Gerenciador de escopo de rastreamento</a>.</span><span class="sxs-lookup"><span data-stu-id="d2320-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="d2320-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2320-138">Related topics</span></span>

[<span data-ttu-id="d2320-139">Gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="d2320-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="d2320-140">Usando o Gerenciador de pesquisa</span><span class="sxs-lookup"><span data-stu-id="d2320-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="d2320-141">Usando o Gerenciador de catálogo</span><span class="sxs-lookup"><span data-stu-id="d2320-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="d2320-142">Usando o Gerenciador de escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="d2320-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
