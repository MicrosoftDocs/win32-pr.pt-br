---
description: A Microsoft fornece vários filtros padrão com o Windows Search. Os clientes chamam esses manipuladores de filtro (que são implementações da interface IFilter) para extrair texto e propriedades de um documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Manipuladores de filtro que acompanham o Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090080"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="7cba7-104">Manipuladores de filtro que acompanham o Windows</span><span class="sxs-lookup"><span data-stu-id="7cba7-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="7cba7-105">A Microsoft fornece vários filtros padrão com o Windows Search.</span><span class="sxs-lookup"><span data-stu-id="7cba7-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="7cba7-106">Os clientes chamam esses manipuladores de filtro (que são implementações da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para extrair texto e propriedades de um documento.</span><span class="sxs-lookup"><span data-stu-id="7cba7-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="7cba7-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7cba7-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="7cba7-108">Notas de implementação da pesquisa do Windows</span><span class="sxs-lookup"><span data-stu-id="7cba7-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="7cba7-109">Implementação do Windows 7 e 10</span><span class="sxs-lookup"><span data-stu-id="7cba7-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="7cba7-110">Implementação do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cba7-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="7cba7-111">Implementação herdada</span><span class="sxs-lookup"><span data-stu-id="7cba7-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="7cba7-112">Filtros de pesquisa do Windows</span><span class="sxs-lookup"><span data-stu-id="7cba7-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="7cba7-113">Manipulador de filtro MIME</span><span class="sxs-lookup"><span data-stu-id="7cba7-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="7cba7-114">Manipulador de filtro HTML</span><span class="sxs-lookup"><span data-stu-id="7cba7-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="7cba7-115">Manipulador de filtro de documento</span><span class="sxs-lookup"><span data-stu-id="7cba7-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="7cba7-116">Manipulador de filtro de texto sem formatação</span><span class="sxs-lookup"><span data-stu-id="7cba7-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="7cba7-117">Manipulador de filtro binário ou nulo</span><span class="sxs-lookup"><span data-stu-id="7cba7-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="7cba7-118">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7cba7-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="7cba7-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cba7-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="7cba7-120">Notas de implementação da pesquisa do Windows</span><span class="sxs-lookup"><span data-stu-id="7cba7-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="7cba7-121">No Windows 7 e posterior, os filtros gravados em código gerenciado são explicitamente bloqueados.</span><span class="sxs-lookup"><span data-stu-id="7cba7-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="7cba7-122">Os filtros devem ser escritos em código nativo devido a possíveis problemas de controle de versão do CLR com o processo em que vários suplementos são executados.</span><span class="sxs-lookup"><span data-stu-id="7cba7-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="7cba7-123">Implementação do Windows 7 e 10</span><span class="sxs-lookup"><span data-stu-id="7cba7-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="7cba7-124">No Windows 7 e posterior, há um novo comportamento que ocorre ao registrar um manipulador de filtro, um manipulador de propriedades ou uma nova extensão.</span><span class="sxs-lookup"><span data-stu-id="7cba7-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="7cba7-125">Quando um manipulador de propriedades novo e/ou manipulador de filtro é instalado, os arquivos com as extensões correspondentes são reindexados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7cba7-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="7cba7-126">No Windows 7 e posterior, recomendamos que você instale um manipulador de filtro em conjunto com seus manipuladores de propriedade correspondentes e que registre o manipulador de filtro antes do manipulador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7cba7-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="7cba7-127">O registro do manipulador de propriedades inicia a reindexação imediata de arquivos indexados anteriormente sem precisar primeiro de uma reinicialização e aproveita os manipuladores de filtro registrados anteriormente para fins de indexação de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="7cba7-128">Se apenas um manipulador de filtro for instalado sem um manipulador de propriedades correspondente, a reindexação automática ocorrerá após uma reinicialização do serviço de indexação ou uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="7cba7-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="7cba7-129">Para sinalizadores de descrição de propriedade específicos para o Windows 7, consulte os seguintes tópicos de referência: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) e [PROPDESC \_ SEARCHINFO \_ flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span><span class="sxs-lookup"><span data-stu-id="7cba7-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="7cba7-130">Implementação do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cba7-130">Windows Vista Implementation</span></span>

<span data-ttu-id="7cba7-131">No Windows Vista e versões anteriores, a instalação de um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou manipulador de propriedades não inicia uma reindexação de itens existentes, a menos que um ISV (fornecedor independente de software) chame explicitamente uma recompilação ou reindexação de URLs correspondentes.</span><span class="sxs-lookup"><span data-stu-id="7cba7-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="7cba7-132">Há duas diferenças principais entre aplicativos herdados, como serviço de indexação e aplicativos mais recentes, como o Windows Search, que você deve saber ao implementar filtros:</span><span class="sxs-lookup"><span data-stu-id="7cba7-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="7cba7-133">Uso da interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .</span><span class="sxs-lookup"><span data-stu-id="7cba7-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="7cba7-134">Uso de manipuladores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7cba7-134">Use of property handlers.</span></span>

<span data-ttu-id="7cba7-135">Primeiro, o Windows Vista e o Windows Search 3,0 e posterior exigem que você use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="7cba7-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="7cba7-136">Para garantir o desempenho e a compatibilidade futura.</span><span class="sxs-lookup"><span data-stu-id="7cba7-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="7cba7-137">Para ajudar a aumentar a segurança.</span><span class="sxs-lookup"><span data-stu-id="7cba7-137">To help increase security.</span></span> <span data-ttu-id="7cba7-138">Os filtros implementados com [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) são mais seguros porque o contexto no qual o filtro é executado não precisa dos direitos para abrir arquivos no disco ou pela rede.</span><span class="sxs-lookup"><span data-stu-id="7cba7-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="7cba7-139">Embora o Windows Search Use apenas [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), você também pode incluir a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/ou implementações de [interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) em seus filtros para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7cba7-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="7cba7-140">A segunda grande diferença é que o Windows Vista e o Windows Search 3,0 e posterior têm um novo [sistema de propriedades](../properties/building-property-handlers.md) que usa manipuladores de propriedade para enumerar Propriedades de itens.</span><span class="sxs-lookup"><span data-stu-id="7cba7-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="7cba7-141">No entanto, há ocasiões em que você precisa implementar um filtro que lide com o conteúdo e as propriedades para:</span><span class="sxs-lookup"><span data-stu-id="7cba7-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="7cba7-142">Suporte a implementações de MSSearch herdado.</span><span class="sxs-lookup"><span data-stu-id="7cba7-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="7cba7-143">Atravessar links.</span><span class="sxs-lookup"><span data-stu-id="7cba7-143">Traverse links.</span></span>
- <span data-ttu-id="7cba7-144">Preservar informações de idioma.</span><span class="sxs-lookup"><span data-stu-id="7cba7-144">Preserve language information.</span></span>
- <span data-ttu-id="7cba7-145">Filtrar itens inseridos recursivamente.</span><span class="sxs-lookup"><span data-stu-id="7cba7-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="7cba7-146">Nessas situações, você precisa de uma implementação completa de filtro, incluindo o método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) para acessar os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7cba7-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="7cba7-147">Implementação herdada</span><span class="sxs-lookup"><span data-stu-id="7cba7-147">Legacy Implementation</span></span>

<span data-ttu-id="7cba7-148">Como observado anteriormente, o Windows Vista e o Windows Search incluem um novo sistema de propriedades que encapsula as propriedades de um item que é separado do conteúdo de um item.</span><span class="sxs-lookup"><span data-stu-id="7cba7-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="7cba7-149">Este sistema de propriedades não existe em versões anteriores do Microsoft Windows Desktop Search (WDS) 2. x.</span><span class="sxs-lookup"><span data-stu-id="7cba7-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="7cba7-150">Se o filtro precisar dar suporte a outros aplicativos, conforme descrito acima, talvez seja necessário lidar com o conteúdo e as propriedades.</span><span class="sxs-lookup"><span data-stu-id="7cba7-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="7cba7-151">Para obter mais informações sobre como desenvolver um filtro compatível, consulte os tópicos a seguir, [IFilter (para aplicativos herdados)](/windows/win32/api/filter/nn-filter-ifilter)e [desenvolvendo suplementos de filtro (para aplicativos herdados)](../lwef/-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="7cba7-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="7cba7-152">Filtros de pesquisa do Windows</span><span class="sxs-lookup"><span data-stu-id="7cba7-152">Windows Search Filters</span></span>

<span data-ttu-id="7cba7-153">A Microsoft fornece vários filtros padrão com o Windows Search.</span><span class="sxs-lookup"><span data-stu-id="7cba7-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="7cba7-154">O conteúdo da dll do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  é resumido na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cba7-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="7cba7-155">Clicar no nome de um manipulador de filtro leva você para a descrição dessa implementação do **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="7cba7-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="7cba7-156">Manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="7cba7-156">Filter handler</span></span>                                                  | <span data-ttu-id="7cba7-157">Arquivos filtrados</span><span class="sxs-lookup"><span data-stu-id="7cba7-157">Files filtered</span></span>                              | <span data-ttu-id="7cba7-158">DLL do IFilter</span><span class="sxs-lookup"><span data-stu-id="7cba7-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="7cba7-159">Manipulador de filtro MIME</span><span class="sxs-lookup"><span data-stu-id="7cba7-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="7cba7-160">MIME (Multipurpose Internet Mail Extension)</span><span class="sxs-lookup"><span data-stu-id="7cba7-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="7cba7-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="7cba7-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="7cba7-162">Manipulador de filtro HTML</span><span class="sxs-lookup"><span data-stu-id="7cba7-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="7cba7-163">HTML 3,0 ou anterior</span><span class="sxs-lookup"><span data-stu-id="7cba7-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="7cba7-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="7cba7-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="7cba7-165">Manipulador de filtro de documento</span><span class="sxs-lookup"><span data-stu-id="7cba7-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="7cba7-166">Microsoft Word, Excel, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="7cba7-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="7cba7-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="7cba7-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="7cba7-168">Manipulador de filtro de texto sem formatação</span><span class="sxs-lookup"><span data-stu-id="7cba7-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="7cba7-169">Arquivos de texto sem formatação – IFilter padrão</span><span class="sxs-lookup"><span data-stu-id="7cba7-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="7cba7-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="7cba7-170">query.dll</span></span>    |
| [<span data-ttu-id="7cba7-171">Manipulador de filtro binário ou nulo</span><span class="sxs-lookup"><span data-stu-id="7cba7-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="7cba7-172">Arquivos binários-IFilter nulo</span><span class="sxs-lookup"><span data-stu-id="7cba7-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="7cba7-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="7cba7-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="7cba7-174">Manipulador de filtro MIME</span><span class="sxs-lookup"><span data-stu-id="7cba7-174">MIME Filter Handler</span></span>

<span data-ttu-id="7cba7-175">O manipulador de filtro MIME (em mimefilt.dll) extrai informações de texto e propriedade de arquivos com as extensões. eml,. mht e. mhtml.</span><span class="sxs-lookup"><span data-stu-id="7cba7-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="7cba7-176">Manipulador de filtro HTML</span><span class="sxs-lookup"><span data-stu-id="7cba7-176">HTML Filter Handler</span></span>

<span data-ttu-id="7cba7-177">O manipulador de filtro HTML (em nlhtml.dll) extrai informações de texto e propriedade da classe "htmlfiles" para que ela possa ser indexada pelo Windows Search.</span><span class="sxs-lookup"><span data-stu-id="7cba7-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="7cba7-178">Para obter uma descrição da associação entre o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e o tipo de arquivo, consulte "localizando a DLL do IFilter para um arquivo" em [Registrando manipuladores de filtro](-search-ifilter-registering-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7cba7-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="7cba7-179">Você pode usar o `META` recurso de marca de documentos HTML para transmitir solicitações de tratamento especial para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML.</span><span class="sxs-lookup"><span data-stu-id="7cba7-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="7cba7-180">`META` as marcas ocorrem próximo ao início de um arquivo HTML dentro das `HEAD ... /HEAD` marcas, conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cba7-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="7cba7-181">Algumas `META` marcas HTML são mapeadas automaticamente para valores bem conhecidos de conjunto de propriedades e ID de propriedade (PID)) para que as consultas nessas propriedades pesquisem o conteúdo mapeado.</span><span class="sxs-lookup"><span data-stu-id="7cba7-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="7cba7-182">Alguns exemplos são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cba7-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="7cba7-183">Para obter uma lista das propriedades do sistema que você pode usar para os formatos de arquivo, consulte [Propriedades definidas pelo sistema para formatos de arquivo personalizados](-shell-systemdefinedpropertiesforfileformats.md).</span><span class="sxs-lookup"><span data-stu-id="7cba7-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="7cba7-184">Exemplo da propriedade</span><span class="sxs-lookup"><span data-stu-id="7cba7-184">Property example</span></span>                              | <span data-ttu-id="7cba7-185">Mapeado para</span><span class="sxs-lookup"><span data-stu-id="7cba7-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7cba7-186">meta name = "Author" content = "Ruth"</span><span class="sxs-lookup"><span data-stu-id="7cba7-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="7cba7-187">A propriedade autor no conjunto de propriedades de informações resumidas.</span><span class="sxs-lookup"><span data-stu-id="7cba7-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="7cba7-188">meta name = "Subject" content = "processamento de texto"</span><span class="sxs-lookup"><span data-stu-id="7cba7-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="7cba7-189">A propriedade Subject no conjunto de propriedades de informações resumidas.</span><span class="sxs-lookup"><span data-stu-id="7cba7-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="7cba7-190">meta name = "palavras-chave" content = "fonts, serif"</span><span class="sxs-lookup"><span data-stu-id="7cba7-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="7cba7-191">A Propriedade Keyword no conjunto de propriedades de informações resumidas.</span><span class="sxs-lookup"><span data-stu-id="7cba7-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="7cba7-192">meta name = "MS. Category" content = "ficção"</span><span class="sxs-lookup"><span data-stu-id="7cba7-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="7cba7-193">A propriedade Category no conjunto de propriedades informações de resumo do documento.</span><span class="sxs-lookup"><span data-stu-id="7cba7-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="7cba7-194">Alguns recursos do [**IFILTER**](/windows/win32/api/filter/nn-filter-ifilter) HTML são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cba7-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (Esta tabela precisa ser HTML para que os exemplos sejam formatados corretamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cba7-196">Tarefa</span><span class="sxs-lookup"><span data-stu-id="7cba7-196">Task</span></span></th>
<th><span data-ttu-id="7cba7-197">Ação</span><span class="sxs-lookup"><span data-stu-id="7cba7-197">Action</span></span></th>
<th><span data-ttu-id="7cba7-198">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7cba7-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cba7-199">Criando resumos especiais de arquivos</span><span class="sxs-lookup"><span data-stu-id="7cba7-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="7cba7-200">Use a <code>META NAME=&quot;DESCRIPTION&quot;...</code> marca para instruir o <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> a usar a cadeia de caracteres após a <code>CONTENT</code> palavra-chave como o resumo do documento.</span><span class="sxs-lookup"><span data-stu-id="7cba7-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7cba7-201">O processo de filtragem pode gerar resumos para cada arquivo filtrado, cujo padrão é um conjunto de caracteres no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cba7-202">Impedindo que arquivos individuais sejam filtrados</span><span class="sxs-lookup"><span data-stu-id="7cba7-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="7cba7-203">Adicione uma <code>meta name</code> marca ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cba7-204">Configurando o código de idioma para um arquivo (para garantir que o sistema escolha os arquivos de palavras de som e de ruído do idioma correto)</span><span class="sxs-lookup"><span data-stu-id="7cba7-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="7cba7-205">Adicione a seguinte <code>meta name</code> marcação ao arquivo, em que o campo de conteúdo especifica o código de idioma apropriado (em caracteres ou usando o valor de localidade).</span><span class="sxs-lookup"><span data-stu-id="7cba7-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="7cba7-206">Manipulador de filtro de documento</span><span class="sxs-lookup"><span data-stu-id="7cba7-206">Document Filter Handler</span></span>

<span data-ttu-id="7cba7-207">O manipulador de filtro de documento (no offilt.dll) filtra arquivos para algumas extensões de documentos no Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="7cba7-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="7cba7-208">Isso inclui arquivos com extensões. doc,. mdb,. ppt e. xlt, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="7cba7-209">Manipulador de filtro de texto sem formatação</span><span class="sxs-lookup"><span data-stu-id="7cba7-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="7cba7-210">Para arquivos de texto sem formatação, o Windows Search usa o manipulador de filtro de texto, que filtra as propriedades do sistema (como nomes de arquivo) e o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="7cba7-211">Quando um tipo de arquivo não tem uma associação de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no registro, o Windows Search indexa apenas as propriedades do Shell para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="7cba7-212">No entanto, o usuário pode usar as **Opções avançadas** no painel de controle de **Opções de indexação** para **indexar Propriedades** ou **indexar Propriedades e conteúdo do arquivo**.</span><span class="sxs-lookup"><span data-stu-id="7cba7-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![captura de tela mostrando a caixa de diálogo Opções avançadas](images/ifilteradvancedoptions.png)

<span data-ttu-id="7cba7-214">Se o usuário escolher essa opção para um tipo de arquivo sem um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associado, o manipulador de filtro de texto será usado para extrair o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="7cba7-215">O manipulador de filtro de texto não "entende" nenhum formato de documento; ao filtrar o conteúdo de um arquivo, ele trata o arquivo como uma sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7cba7-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="7cba7-216">Ele verifica a marca de ordem de byte Unicode no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7cba7-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="7cba7-217">Manipulador de filtro binário ou nulo</span><span class="sxs-lookup"><span data-stu-id="7cba7-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="7cba7-218">Quando um arquivo binário registrado é encontrado, o manipulador de filtro nulo é usado.</span><span class="sxs-lookup"><span data-stu-id="7cba7-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="7cba7-219">O manipulador de filtro nulo recupera apenas as propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="7cba7-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="7cba7-220">O conteúdo de um arquivo binário não é filtrado.</span><span class="sxs-lookup"><span data-stu-id="7cba7-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="7cba7-221">Exemplos de propriedades do sistema são **filename**, **LastWriteTime**, **filesize** e **Attributes**.</span><span class="sxs-lookup"><span data-stu-id="7cba7-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cba7-222">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7cba7-222">Additional Resources</span></span>

- <span data-ttu-id="7cba7-223">O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="7cba7-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="7cba7-224">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7cba7-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="7cba7-225">Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="7cba7-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="7cba7-226">Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7cba7-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cba7-227">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cba7-227">Related topics</span></span>

[<span data-ttu-id="7cba7-228">Desenvolvendo manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="7cba7-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="7cba7-229">Sobre manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="7cba7-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="7cba7-230">Práticas recomendadas para a criação de manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="7cba7-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="7cba7-231">Retornando Propriedades de um manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="7cba7-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="7cba7-232">Implementando manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="7cba7-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="7cba7-233">Registrando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="7cba7-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="7cba7-234">Testando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="7cba7-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
