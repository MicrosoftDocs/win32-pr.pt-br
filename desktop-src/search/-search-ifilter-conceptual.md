---
description: O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desenvolvendo manipuladores de filtro para o Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010391"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="ae7e2-103">Desenvolvendo manipuladores de filtro para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="ae7e2-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="ae7e2-104">O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="ae7e2-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="ae7e2-105">Você pode estender o Windows Search para indexar tipos de arquivo novos ou proprietários escrevendo filtros para extrair o conteúdo e os manipuladores de propriedade para extrair as propriedades dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="ae7e2-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="ae7e2-106">Esta seção fornece a estrutura conceitual necessária para implementar um manipulador de filtro (uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).</span><span class="sxs-lookup"><span data-stu-id="ae7e2-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="ae7e2-107">Noções básicas sobre manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="ae7e2-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="ae7e2-108">Práticas recomendadas para a criação de manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="ae7e2-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="ae7e2-109">Retornando Propriedades de um manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="ae7e2-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="ae7e2-110">Manipuladores de filtro que acompanham o Windows</span><span class="sxs-lookup"><span data-stu-id="ae7e2-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="ae7e2-111">Implementando manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="ae7e2-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="ae7e2-112">Registrando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="ae7e2-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="ae7e2-113">Testando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="ae7e2-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="ae7e2-114">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="ae7e2-114">Additional Resources</span></span>

- <span data-ttu-id="ae7e2-115">O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="ae7e2-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="ae7e2-116">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae7e2-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="ae7e2-117">Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ae7e2-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="ae7e2-118">Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae7e2-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
