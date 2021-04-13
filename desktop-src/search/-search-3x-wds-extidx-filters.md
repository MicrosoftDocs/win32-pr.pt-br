---
description: O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Práticas recomendadas para manipuladores de filtro no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501484"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="193eb-103">Práticas recomendadas para a criação de manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="193eb-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="193eb-104">O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="193eb-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="193eb-105">Você pode estender o Windows Search para indexar tipos de arquivo novos ou proprietários, escrevendo manipuladores de filtro para extrair o conteúdo e manipuladores de propriedade para extrair as propriedades dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="193eb-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="193eb-106">Os filtros são associados a tipos de arquivo, como indicado pelas extensões de nome de arquivo, tipos MIME ou identificadores de classe (CLSIDs).</span><span class="sxs-lookup"><span data-stu-id="193eb-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="193eb-107">Embora um filtro possa lidar com vários tipos de arquivo, cada tipo funciona com apenas um filtro.</span><span class="sxs-lookup"><span data-stu-id="193eb-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="193eb-108">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="193eb-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="193eb-109">Código nativo</span><span class="sxs-lookup"><span data-stu-id="193eb-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="193eb-110">Práticas de código seguro para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="193eb-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="193eb-111">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="193eb-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="193eb-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="193eb-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="193eb-113">Código nativo</span><span class="sxs-lookup"><span data-stu-id="193eb-113">Native Code</span></span>

<span data-ttu-id="193eb-114">No Windows 7 e posterior, os filtros gravados em código gerenciado são explicitamente bloqueados.</span><span class="sxs-lookup"><span data-stu-id="193eb-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="193eb-115">Os filtros devem ser escritos em código nativo devido a possíveis problemas de controle de versão do CLR com o processo em que vários suplementos são executados.</span><span class="sxs-lookup"><span data-stu-id="193eb-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="193eb-116">Práticas de código seguro para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="193eb-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="193eb-117">Veja a seguir as práticas para escrever aplicativos seguros para uso com o Windows Search.</span><span class="sxs-lookup"><span data-stu-id="193eb-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="193eb-118">**Para aplicativos de consulta:**</span><span class="sxs-lookup"><span data-stu-id="193eb-118">**For query applications:**</span></span>

-   <span data-ttu-id="193eb-119">Ao gravar clientes de pesquisa, você deve escolher a API que é executada em um contexto de segurança que permite ao usuário o privilégio mínimo.</span><span class="sxs-lookup"><span data-stu-id="193eb-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="193eb-120">Por exemplo, as páginas ASP podem usar o objeto de consulta IXSSO, que é executado como um processo de usuário.</span><span class="sxs-lookup"><span data-stu-id="193eb-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="193eb-121">**Para IFilters e recursos de idioma:**</span><span class="sxs-lookup"><span data-stu-id="193eb-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="193eb-122">Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtro for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="193eb-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="193eb-123">Não há nenhum mecanismo para encadear filtros.</span><span class="sxs-lookup"><span data-stu-id="193eb-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="193eb-124">Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.</span><span class="sxs-lookup"><span data-stu-id="193eb-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="193eb-125">IFilters, separadores de palavras e lematizadores para o Windows Search são executados no contexto de segurança local.</span><span class="sxs-lookup"><span data-stu-id="193eb-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="193eb-126">Eles devem ser gravados para gerenciar buffers e para empilhar corretamente.</span><span class="sxs-lookup"><span data-stu-id="193eb-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="193eb-127">Todas as cópias de cadeia de caracteres devem ter verificações explícitas para proteção contra estouros de buffer.</span><span class="sxs-lookup"><span data-stu-id="193eb-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="193eb-128">Você sempre deve verificar o tamanho alocado do buffer e testar o tamanho dos dados em relação ao tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="193eb-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="193eb-129">Saturações de buffer são uma técnica comum para explorar o código que não impõe restrições de tamanho de buffer.</span><span class="sxs-lookup"><span data-stu-id="193eb-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="193eb-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), separador de palavras e componentes de lematizador devem nunca chamar a função de [função ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ou API semelhante que encerra um processo e todos os seus threads.</span><span class="sxs-lookup"><span data-stu-id="193eb-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="193eb-131">Não aloque ou libere recursos no ponto de entrada DllMain.</span><span class="sxs-lookup"><span data-stu-id="193eb-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="193eb-132">Isso pode levar a falhas durante testes de estresse de recursos baixos.</span><span class="sxs-lookup"><span data-stu-id="193eb-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="193eb-133">Codifique todos os objetos a serem thread-safe.</span><span class="sxs-lookup"><span data-stu-id="193eb-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="193eb-134">O Windows Search chama qualquer instância de um separador de palavras ou lematizador em um thread por vez, mas ele pode chamar várias instâncias ao mesmo tempo em vários threads.</span><span class="sxs-lookup"><span data-stu-id="193eb-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="193eb-135">Evite criar arquivos temporários ou gravar no registro.</span><span class="sxs-lookup"><span data-stu-id="193eb-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="193eb-136">Se você usar o compilador Microsoft Visual C++, certifique-se de compilar seu aplicativo usando a opção **/GS** .</span><span class="sxs-lookup"><span data-stu-id="193eb-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="193eb-137">A opção **/GS** é usada para detectar saturações de buffer.</span><span class="sxs-lookup"><span data-stu-id="193eb-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="193eb-138">A opção/GS coloca as verificações de segurança no código compilado.</span><span class="sxs-lookup"><span data-stu-id="193eb-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="193eb-139">Para obter mais informações, consulte a [função DllGetClassObject](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (verificação de segurança do buffer) na seção Opções do compilador Visual C++ do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="193eb-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="193eb-140">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="193eb-140">Additional Resources</span></span>

-   <span data-ttu-id="193eb-141">O exemplo [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) demonstra como criar uma classe base de IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="193eb-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="193eb-142">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="193eb-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="193eb-143">Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="193eb-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="193eb-144">Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="193eb-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="193eb-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="193eb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="193eb-146">Desenvolvendo manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="193eb-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="193eb-147">Sobre manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="193eb-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="193eb-148">Retornando Propriedades de um manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="193eb-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="193eb-149">Manipuladores de filtro que acompanham o Windows</span><span class="sxs-lookup"><span data-stu-id="193eb-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="193eb-150">Implementando manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="193eb-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="193eb-151">Registrando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="193eb-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="193eb-152">Testando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="193eb-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
