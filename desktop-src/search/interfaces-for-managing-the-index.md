---
description: Saiba como Windows Search permite gerenciar o índice Windows Search com o Gerenciador de Pesquisa, o Gerenciador de Catálogos e Gerenciador do Escopo de Rastreamento.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para gerenciar o índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120011"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="fad80-103">Interfaces para gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="fad80-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="fad80-104">Windows Search permite gerenciar o índice Windows Search com três componentes principais: Gerenciador de Pesquisa, Gerenciador de Catálogos e Gerenciador do Escopo de Rastreamento.</span><span class="sxs-lookup"><span data-stu-id="fad80-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="fad80-105">Algumas dessas interfaces de gerenciamento podem ser usadas com privilégios de usuário padrão, mas aquelas que alteram o estado do índice exigem privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="fad80-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="fad80-106">Sobre as interfaces para gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="fad80-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fad80-107">Componente</span><span class="sxs-lookup"><span data-stu-id="fad80-107">Component</span></span></th>
<th><span data-ttu-id="fad80-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="fad80-108">Interfaces</span></span></th>
<th><span data-ttu-id="fad80-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fad80-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fad80-110">Gerenciador de Pesquisa</span><span class="sxs-lookup"><span data-stu-id="fad80-110">Search Manager</span></span></td>
<td><span data-ttu-id="fad80-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="fad80-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="fad80-112">Fornece métodos para recuperar e definir informações sobre Windows Search:</span><span class="sxs-lookup"><span data-stu-id="fad80-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="fad80-113">Obter uma instância do Gerenciador de Catálogo para um catálogo específico.</span><span class="sxs-lookup"><span data-stu-id="fad80-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="fad80-114">Obter ou definir informações de proxy.</span><span class="sxs-lookup"><span data-stu-id="fad80-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="fad80-115">Obter informações de versão sobre o Windows Search de dados.</span><span class="sxs-lookup"><span data-stu-id="fad80-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="fad80-116">Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-searchmanager.md">Usando o Gerenciador de Pesquisa</a>.</span><span class="sxs-lookup"><span data-stu-id="fad80-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fad80-117">Gerenciador de Catálogo</span><span class="sxs-lookup"><span data-stu-id="fad80-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="fad80-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="fad80-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="fad80-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="fad80-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="fad80-120">Fornece métodos para gerenciar um catálogo de pesquisa individual, como causar uma nova indexação ou definir tempos-máximos.</span><span class="sxs-lookup"><span data-stu-id="fad80-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="fad80-121">Essa interface gerencia o catálogo em quatro áreas:</span><span class="sxs-lookup"><span data-stu-id="fad80-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="fad80-122">Conteúdo do catálogo – garantir que novos dados sejam indexados e que outros aplicativos e componentes funcionem corretamente forçando uma nova indexação de todo ou parte do catálogo ou redefinindo todo o catálogo.</span><span class="sxs-lookup"><span data-stu-id="fad80-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="fad80-123">Propriedades do catálogo – definindo propriedades que determinam como o catálogo gerencia tempos-tempos ao se conectar a manipuladores de protocolo e como as marcas diacríticas são tratadas em pesquisas.</span><span class="sxs-lookup"><span data-stu-id="fad80-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="fad80-124">Status do catálogo – obter informações sobre o catálogo, incluindo status, tamanho e estado da atividade atual.</span><span class="sxs-lookup"><span data-stu-id="fad80-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="fad80-125">Acesso a outras interfaces – recuperando outras interfaces relacionadas à pesquisa exigidas pelo Gerenciador do Escopo de Rastreamento, notificações de alteração de dados e a interface <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fad80-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="fad80-126">Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-catalog-manager.md">Usando o Gerenciador de Catálogo.</a></span><span class="sxs-lookup"><span data-stu-id="fad80-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fad80-127">Gerenciador do Escopo de Rastreamento</span><span class="sxs-lookup"><span data-stu-id="fad80-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="fad80-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="fad80-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="fad80-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="fad80-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="fad80-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="fad80-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="fad80-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="fad80-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="fad80-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="fad80-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="fad80-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="fad80-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="fad80-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="fad80-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="fad80-135">Fornece métodos para informar o mecanismo de pesquisa sobre contêineres a rastrear ou observar e itens nesses contêineres para incluir ou excluir no índice.</span><span class="sxs-lookup"><span data-stu-id="fad80-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="fad80-136">Você também pode consultar o Gerenciador do Escopo de Rastreamento para ver se uma URL específica está no escopo do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="fad80-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="fad80-137">Para obter mais informações, <a href="-search-3x-wds-extidx-csm.md">consulte Usando o Gerenciador do Escopo de Rastreamento</a>.</span><span class="sxs-lookup"><span data-stu-id="fad80-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="fad80-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fad80-138">Related topics</span></span>

[<span data-ttu-id="fad80-139">Gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="fad80-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="fad80-140">Usando o Gerenciador de Pesquisa</span><span class="sxs-lookup"><span data-stu-id="fad80-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="fad80-141">Usando o Gerenciador de Catálogo</span><span class="sxs-lookup"><span data-stu-id="fad80-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="fad80-142">Usando o Gerenciador do Escopo de Rastreamento</span><span class="sxs-lookup"><span data-stu-id="fad80-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
