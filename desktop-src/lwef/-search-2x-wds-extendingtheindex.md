---
title: Estendendo o índice (recursos herdados do ambiente Windows)
description: O uso do e do desenvolvimento para as versões 2. x do Microsoft Windows Desktop Search (WDS) é fortemente desencorajado em favor do Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085107"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="c98e2-103">Estendendo o índice (recursos herdados do ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="c98e2-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="c98e2-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c98e2-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c98e2-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c98e2-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c98e2-106">O uso do e do desenvolvimento para as versões 2. x do Microsoft Windows Desktop Search (WDS) é fortemente desencorajado em favor do [Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c98e2-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="c98e2-107">O WDS pode ser estendido para indexar o conteúdo de novos tipos de arquivo e armazenamentos de dados.</span><span class="sxs-lookup"><span data-stu-id="c98e2-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="c98e2-108">Atualmente, o WDS 2. x contém filtros para mais de 200 tipos de itens (incluindo itens de texto sem formatação, como HTML, XML e arquivos de código-fonte) e usa o mesmo [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e a mesma tecnologia de manipulador de protocolo que os serviços do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c98e2-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="c98e2-109">Se você já tiver implementações de filtro instaladas para os novos tipos de arquivo, o WDS poderá usar as interfaces de filtro existentes para indexar esses dados.</span><span class="sxs-lookup"><span data-stu-id="c98e2-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="c98e2-110">Os suplementos do WDS 2. x permitem que o índice Percorra e analise novos dados e estruturas de dados para obter informações a serem adicionadas ao catálogo pesquisável.</span><span class="sxs-lookup"><span data-stu-id="c98e2-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="c98e2-111">Esses suplementos também podem estender o Shell do Windows para associar ícones e manipuladores de menu de contexto aos novos tipos de arquivo e armazenamentos de dados.</span><span class="sxs-lookup"><span data-stu-id="c98e2-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="c98e2-112">Para incluir novos tipos de arquivo no catálogo do WDS, um suplemento deve implementar a interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).</span><span class="sxs-lookup"><span data-stu-id="c98e2-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="c98e2-113">Para incluir novos armazenamentos de dados, um suplemento deve ser um manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c98e2-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="c98e2-114">Se o novo armazenamento de dados incluir arquivos incorporados ou novos tipos de arquivo, também será necessário escrever um filtro apropriado.</span><span class="sxs-lookup"><span data-stu-id="c98e2-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="c98e2-115">Filtros e manipuladores de protocolo devem ser escritos em código nativo devido a possíveis problemas de controle de versão do CLR com o processo em que todos os suplementos são executados.</span><span class="sxs-lookup"><span data-stu-id="c98e2-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="c98e2-116">Adicionando tipos de arquivo ao índice</span><span class="sxs-lookup"><span data-stu-id="c98e2-116">Adding File Types to the Index</span></span>

<span data-ttu-id="c98e2-117">Os suplementos podem estender o WDS para indexar tipos de arquivo novos ou proprietários e associar cada novo tipo de arquivo a um menu de contexto ou ícone específico de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c98e2-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="c98e2-118">Para fazer isso, você pode criar e registrar um suplemento que:</span><span class="sxs-lookup"><span data-stu-id="c98e2-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="c98e2-119">Implementa uma interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para cada tipo de arquivo, de modo que o WDS possa acessar e indexar o texto e os metadados do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c98e2-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="c98e2-120">Implementa as interfaces **IExtractIcon** e **IContextMenu** para adicionar ícones e menus de contexto para maior integração e usabilidade.</span><span class="sxs-lookup"><span data-stu-id="c98e2-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="c98e2-121">Para obter uma discussão sobre a implementação de filtros, consulte [desenvolvendo suplementos do IFilter](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="c98e2-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="c98e2-122">Adicionando armazenamentos de dados ao índice</span><span class="sxs-lookup"><span data-stu-id="c98e2-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="c98e2-123">Os suplementos podem estender o WDS para indexar novos armazenamentos de dados e associar arquivos a um menu de contexto ou ícone específico de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c98e2-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="c98e2-124">Para fazer isso, você pode criar e registrar um manipulador de protocolo que:</span><span class="sxs-lookup"><span data-stu-id="c98e2-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="c98e2-125">Implementa as interfaces **ISearchProtocol** e **IUrlAccessor** para processar e associar itens individuais na fonte de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c98e2-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="c98e2-126">O WDS usa URLs para identificar itens de forma exclusiva, independentemente de esses itens estarem no sistema de arquivos, dentro de uma loja do tipo banco de dados ou na Web.</span><span class="sxs-lookup"><span data-stu-id="c98e2-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="c98e2-127">Implementa a interface **IPersistFolder** e partes da interface **IShellFolder** para adicionar ícones e menus de contexto para maior integração e usabilidade.</span><span class="sxs-lookup"><span data-stu-id="c98e2-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="c98e2-128">Para obter uma discussão sobre a implementação de manipuladores de protocolo, consulte [desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="c98e2-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="c98e2-129">Diretrizes do instalador do suplemento</span><span class="sxs-lookup"><span data-stu-id="c98e2-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="c98e2-130">A instalação de um suplemento deve seguir as seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="c98e2-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="c98e2-131">O instalador deve usar o EXE ou o instalador MSI.</span><span class="sxs-lookup"><span data-stu-id="c98e2-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="c98e2-132">As notas de versão devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="c98e2-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="c98e2-133">Uma entrada **Adicionar/remover programas** deve ser criada para cada suplemento instalado.</span><span class="sxs-lookup"><span data-stu-id="c98e2-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="c98e2-134">O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.</span><span class="sxs-lookup"><span data-stu-id="c98e2-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="c98e2-135">Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.</span><span class="sxs-lookup"><span data-stu-id="c98e2-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="c98e2-136">Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo ou armazenar novamente.</span><span class="sxs-lookup"><span data-stu-id="c98e2-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c98e2-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c98e2-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c98e2-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c98e2-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c98e2-139">Desenvolvendo suplementos do IFilter</span><span class="sxs-lookup"><span data-stu-id="c98e2-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="c98e2-140">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c98e2-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="c98e2-141">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="c98e2-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c98e2-142">**Visio**</span><span class="sxs-lookup"><span data-stu-id="c98e2-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
