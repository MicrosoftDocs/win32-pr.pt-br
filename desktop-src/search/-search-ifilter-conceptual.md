---
description: Saiba como desenvolver manipuladores de filtro em Windows Search. A pesquisa usa filtros para extrair itens para inclusão em um índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desenvolvendo manipuladores de filtro para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988855"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="85e19-104">Desenvolvendo manipuladores de filtro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="85e19-104">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="85e19-105">O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="85e19-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="85e19-106">Você pode estender Windows Search para indexar tipos de arquivo novos ou proprietários escrevendo filtros para extrair o conteúdo e manipuladores de propriedades para extrair as propriedades dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="85e19-106">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="85e19-107">Esta seção fornece a estrutura conceitual necessária para implementar um manipulador de filtro (uma implementação da interface [**IFilter).**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="85e19-107">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="85e19-108">Noções básicas sobre manipuladores de filtro Windows Search</span><span class="sxs-lookup"><span data-stu-id="85e19-108">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="85e19-109">Práticas recomendadas para criar manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="85e19-109">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="85e19-110">Retornando propriedades de um manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="85e19-110">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="85e19-111">Manipuladores de filtros que são enviar com o Windows</span><span class="sxs-lookup"><span data-stu-id="85e19-111">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="85e19-112">Implementando manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="85e19-112">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="85e19-113">Registrando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="85e19-113">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="85e19-114">Testando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="85e19-114">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="85e19-115">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="85e19-115">Additional Resources</span></span>

- <span data-ttu-id="85e19-116">O exemplo de código [IFilterSample,](-search-sample-ifiltersample.md) disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="85e19-116">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="85e19-117">Para uma visão geral do processo de indexação, consulte [O processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="85e19-117">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="85e19-118">Para uma visão geral dos tipos de arquivo, consulte [Tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="85e19-118">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="85e19-119">Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e Registro de Aplicativo.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85e19-119">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
