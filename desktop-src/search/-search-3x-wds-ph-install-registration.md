---
description: A instalação de um manipulador de protocolo envolve a cópia das DLLs para um local apropriado no diretório arquivos de programas e, em seguida, o registro do manipulador de protocolo por meio do registro.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Instalando e Registrando manipuladores de protocolo (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761782"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="8a8f5-103">Instalando e Registrando manipuladores de protocolo (pesquisa do Windows)</span><span class="sxs-lookup"><span data-stu-id="8a8f5-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="8a8f5-104">A instalação de um manipulador de protocolo envolve a cópia das DLLs para um local apropriado no diretório arquivos de programas e, em seguida, o registro do manipulador de protocolo por meio do registro.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="8a8f5-105">O aplicativo de instalação também pode adicionar uma raiz de pesquisa e regras de escopo para definir um escopo de rastreamento padrão para a fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="8a8f5-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="8a8f5-107">Sobre URLs</span><span class="sxs-lookup"><span data-stu-id="8a8f5-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="8a8f5-108">Implementando interfaces de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="8a8f5-109">ISearchProtocol e ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="8a8f5-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="8a8f5-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="8a8f5-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="8a8f5-111">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="8a8f5-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="8a8f5-112">Implementando manipuladores de filtro para contêineres</span><span class="sxs-lookup"><span data-stu-id="8a8f5-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="8a8f5-113">Instalando e registrando um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="8a8f5-114">Diretrizes para registrar um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="8a8f5-115">Registrando um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="8a8f5-116">Registrando o manipulador de tipo de arquivo do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="8a8f5-117">Garantindo que seus itens sejam indexados</span><span class="sxs-lookup"><span data-stu-id="8a8f5-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="8a8f5-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a8f5-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="8a8f5-119">Sobre URLs</span><span class="sxs-lookup"><span data-stu-id="8a8f5-119">About URLs</span></span>

<span data-ttu-id="8a8f5-120">O Windows Search usa URLs para identificar exclusivamente os itens na hierarquia da fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="8a8f5-121">A URL que é o primeiro nó na hierarquia é chamada de [raiz de pesquisa](-search-3x-wds-extidx-csm-searchroots.md); O Windows Search começará a indexação na raiz da pesquisa, solicitando que o manipulador de protocolo enumere links filho para cada URL.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="8a8f5-122">A estrutura de URL típica é:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="8a8f5-123">A sintaxe da URL é descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="8a8f5-124">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a8f5-124">Syntax</span></span>           | <span data-ttu-id="8a8f5-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a8f5-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="8a8f5-126">Identifica qual manipulador de protocolo deve ser invocado para a URL.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="8a8f5-127">{SID de usuário}</span><span class="sxs-lookup"><span data-stu-id="8a8f5-127">{user SID}</span></span>       | <span data-ttu-id="8a8f5-128">Identifica o contexto de segurança do usuário sob o qual o manipulador de protocolo é chamado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="8a8f5-129">Se nenhum SID (identificador de segurança do usuário) for identificado, o manipulador de protocolo será chamado no contexto de segurança do serviço do sistema.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="8a8f5-130">Define a hierarquia do repositório, em que cada barra ('/') é um separador entre nomes de pasta.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="8a8f5-131">Representa uma cadeia de caracteres exclusiva que identifica o item filho (por exemplo, o nome do arquivo).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="8a8f5-132">O indexador de pesquisa do Windows corta a barra final de URLs.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="8a8f5-133">Como resultado, você não pode contar com a existência de uma barra final para identificar um diretório em vez de um item.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="8a8f5-134">Seu manipulador de protocolo deve ser capaz de lidar com essa sintaxe de URL.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="8a8f5-135">Verifique se o nome do protocolo que você selecionou para identificar a fonte de dados do shell não está em conflito com os atuais.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="8a8f5-136">Recomendamos esta Convenção de nomenclatura: `companyName.scheme` .</span><span class="sxs-lookup"><span data-stu-id="8a8f5-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="8a8f5-137">Para obter mais informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="8a8f5-138">Implementando interfaces de manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="8a8f5-139">A criação de um manipulador de protocolo requer a implementação das três interfaces a seguir:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="8a8f5-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) para gerenciar objetos UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="8a8f5-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) para expor propriedades e identificar os filtros apropriados para itens na fonte de dados do Shell.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="8a8f5-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para filtrar arquivos proprietários ou para enumerar e filtrar arquivos armazenados hierarquicamente.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="8a8f5-143">Além das três interfaces obrigatórias listadas, as outras interfaces são opcionais e você está no Liberty para implementar qualquer interface opcional que seja mais apropriada para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="8a8f5-144">ISearchProtocol e ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="8a8f5-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="8a8f5-145">As interfaces SearchProtocol inicializam e gerenciam seus objetos UrlAccessor do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="8a8f5-146">A interface [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) é uma extensão opcional de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e inclui um método extra para especificar mais informações sobre o usuário e o item.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="8a8f5-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="8a8f5-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="8a8f5-148">As interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="8a8f5-149">Interface</span><span class="sxs-lookup"><span data-stu-id="8a8f5-149">Interface</span></span>                                                 | <span data-ttu-id="8a8f5-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a8f5-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a8f5-151">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="8a8f5-152">Para uma URL especificada, a interface [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fornece acesso às propriedades do item que é exposto na URL.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="8a8f5-153">Ele também pode associar essas propriedades a um filtro específico do manipulador de protocolo (ou seja, um filtro diferente daquele associado ao nome do arquivo).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="8a8f5-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (opcional)</span><span class="sxs-lookup"><span data-stu-id="8a8f5-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="8a8f5-155">A interface [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) estende o [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) com métodos que obtêm uma página de código para as propriedades do item e sua URL de exibição e que obtêm o tipo de item na URL (documento ou diretório).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="8a8f5-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (opcional)</span><span class="sxs-lookup"><span data-stu-id="8a8f5-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="8a8f5-157">A interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) estende o [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) com um método que obtém uma matriz de SIDs de usuário, permitindo que o host de protocolo de pesquisa represente esses usuários para indexar o item.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="8a8f5-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (opcional)</span><span class="sxs-lookup"><span data-stu-id="8a8f5-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="8a8f5-159">A interface [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) estende a funcionalidade da interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) com um método que identifica se o conteúdo do item deve ser indexado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="8a8f5-160">O objeto UrlAccessor é instanciado e inicializado por um objeto SearchProtocol.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="8a8f5-161">As interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fornecem acesso a informações importantes por meio dos métodos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="8a8f5-162">Método</span><span class="sxs-lookup"><span data-stu-id="8a8f5-162">Method</span></span>                                                                                        | <span data-ttu-id="8a8f5-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a8f5-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a8f5-164">**IUrlAccessor:: GetLastModified**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="8a8f5-165">Retorna a hora em que a URL foi modificada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="8a8f5-166">Se esse tempo for mais recente do que a última vez que o indexador processou essa URL, os manipuladores de filtro (implementações da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) serão chamados para extrair os dados alterados (possivelmente) para esse item.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="8a8f5-167">Os horários modificados para diretórios são ignorados.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="8a8f5-168">**IUrlAccessor:: IsDirectory**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="8a8f5-169">Identifica se a URL representa uma pasta que contém URLs filho.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="8a8f5-170">**IUrlAccessor::BindToStream**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="8a8f5-171">Associa a uma [interface IStream](/windows/win32/api/objidl/nn-objidl-istream) que representa os dados de um arquivo em um repositório de dados personalizado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="8a8f5-172">**IUrlAccessor::BindToFilter**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="8a8f5-173">Associa a um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)específico do manipulador de protocolo, que pode expor propriedades para o item.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="8a8f5-174">**IUrlAccessor4::ShouldIndexItemContent**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="8a8f5-175">Identifica se o conteúdo do item deve ser indexado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="8a8f5-176">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="8a8f5-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="8a8f5-177">A interface [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) é usada para criar uma instância de um manipulador de filtro, que é hospedado em um processo isolado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="8a8f5-178">O manipulador de filtro apropriado é obtido para um CLSID (identificador de classe persistente) especificado, uma classe de armazenamento de documentos ou uma extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="8a8f5-179">O benefício de fazer com que o processo de host se vincule ao [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é que o processo de host pode gerenciar o processo de localização de um manipulador de filtro apropriado e controlar a segurança envolvida na chamada do manipulador.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="8a8f5-180">Implementando manipuladores de filtro para contêineres</span><span class="sxs-lookup"><span data-stu-id="8a8f5-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="8a8f5-181">Se você estiver implementando um manipulador de protocolo hierárquico, deverá implementar um manipulador de filtro para um contêiner que enumere URLs filho.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="8a8f5-182">Um manipulador de filtro é uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="8a8f5-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="8a8f5-183">O processo de enumeração é um loop pelos métodos [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) e [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) da interface **IFilter** ; cada URL filho é exposta como o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="8a8f5-184">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retorna as propriedades do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="8a8f5-185">Para enumerar URLs filho, **IFilter:: GetChunk** retorna um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="8a8f5-186">[PKEY \_ Pesquisar \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="8a8f5-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="8a8f5-187">A URL para o item sem a hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="8a8f5-188">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retorna um PROPVARIANT que contém a URL filho.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="8a8f5-189">[PKEY \_ Pesquisar \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span><span class="sxs-lookup"><span data-stu-id="8a8f5-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="8a8f5-190">A URL e a hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-190">The URL and the last modified time.</span></span> <span data-ttu-id="8a8f5-191">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retorna um PROPVARIANT contendo um vetor da URL filho e a hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="8a8f5-192">Retornar [PKEY \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) é mais eficiente porque o indexador pode determinar imediatamente se o item precisa ser indexado sem chamar os métodos [**ISearchProtocol:: createaccess**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) e [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .</span><span class="sxs-lookup"><span data-stu-id="8a8f5-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="8a8f5-193">O código de exemplo a seguir demonstra como retornar a propriedade [ \_ \_ UrlToIndexWithModificationTime de pesquisa PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="8a8f5-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8a8f5-194">Copyright (c) Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="8a8f5-195">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> <span data-ttu-id="8a8f5-196">Um componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) do contêiner sempre deve enumerar todas as URLs filho, mesmo que as URLs filho não tenham sido alteradas, pois o indexador detecta as exclusões por meio do processo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="8a8f5-197">Se a saída de data em um [PKEY de \_ pesquisa \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicar que os dados não foram alterados, o indexador não atualizará os dados dessa URL.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="8a8f5-198">Instalando e registrando um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="8a8f5-199">A instalação de manipuladores de protocolo envolve copiar as DLLs para um local apropriado no diretório arquivos de programas e, em seguida, registrar as DLLs.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="8a8f5-200">Os manipuladores de protocolo devem implementar o auto-registro para instalação.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="8a8f5-201">O aplicativo de instalação também pode adicionar uma raiz de pesquisa e regras de escopo para definir um escopo de rastreamento padrão para a fonte de dados do Shell, que é discutido para [garantir que seus itens sejam indexados](#ensuring-that-your-items-are-indexed) no final deste tópico.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="8a8f5-202">Diretrizes para registrar um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="8a8f5-203">Você deve seguir estas diretrizes ao registrar um manipulador de protocolo:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="8a8f5-204">O instalador deve usar o EXE ou o instalador MSI.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="8a8f5-205">As notas de versão devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="8a8f5-206">Uma entrada adicionar/remover programas deve ser criada para cada suplemento instalado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="8a8f5-207">O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="8a8f5-208">Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="8a8f5-209">Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo novamente.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="8a8f5-210">O instalador deve definir um escopo de rastreamento padrão para o indexador adicionando uma raiz de pesquisa e regras de escopo usando o Gerenciador de escopo de rastreamento (CSM).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="8a8f5-211">Registrando um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="8a8f5-212">Você precisa fazer quatorze entradas no registro para registrar o componente de manipulador de protocolo, em que:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="8a8f5-213">*Ver \_ IND \_ ProgID* é o ProgID independente de versão da implementação do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="8a8f5-214">*Ver \_ O Dep \_ ProgID* é o ProgID dependente da versão da implementação do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="8a8f5-215">*CLSID \_ 1* é o CLSID da implementação do manipulador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="8a8f5-216">**Para registrar um manipulador de protocolo:**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="8a8f5-217">Registre o ProgID independente de versão com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="8a8f5-218">Registre o ProgID dependente de versão com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="8a8f5-219">Registre o CLSID do manipulador de protocolo com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="8a8f5-220">Registre o manipulador de protocolo no Windows Search.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="8a8f5-221">No exemplo a seguir, <Protocol Name> é o nome do próprio protocolo, como arquivo, MAPI e assim por diante:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="8a8f5-222">Antes do Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="8a8f5-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="8a8f5-223">Registrando o manipulador de tipo de arquivo do manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="8a8f5-224">Você precisa fazer duas entradas no registro para registrar o manipulador de tipo de arquivo do manipulador de protocolo (que também é conhecido como extensão do Shell).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="8a8f5-225">Garantindo que seus itens sejam indexados</span><span class="sxs-lookup"><span data-stu-id="8a8f5-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="8a8f5-226">Depois de implementar o manipulador de protocolo, você deve especificar quais itens do Shell seu manipulador de protocolo será indexado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="8a8f5-227">Você pode usar o Gerenciador de catálogo para iniciar a reindexação (para obter mais informações, consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md)).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="8a8f5-228">Ou você também pode usar o Gerenciador de escopo de rastreamento (CSM) para configurar regras padrão indicando as URLs que você deseja que o indexador rastreie (para obter mais informações, consulte [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md) e [regras de escopo de gerenciamento](-search-3x-wds-extidx-csm-scoperules.md)).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="8a8f5-229">Você também pode adicionar uma raiz de pesquisa (para obter mais informações, consulte [Gerenciando raízes de pesquisa](-search-3x-wds-extidx-csm-searchroots.md)).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="8a8f5-230">Outra opção disponível para você é seguir o procedimento no exemplo reindexar em [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="8a8f5-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="8a8f5-231">A interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fornece métodos que notificam o mecanismo de pesquisa de contêineres para rastreamento e/ou inspeção e itens sob esses contêineres para incluir ou excluir ao rastrear ou assistir.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="8a8f5-232">No Windows 7 e posterior, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende **ISearchCrawlScopeManager** com o método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) que obtém a versão, que informa aos clientes se o estado do CSM foi alterado.</span><span class="sxs-lookup"><span data-stu-id="8a8f5-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a8f5-233">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a8f5-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8a8f5-234">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8a8f5-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8a8f5-235">Noções básicas sobre manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="8a8f5-236">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="8a8f5-237">Notificando o índice das alterações</span><span class="sxs-lookup"><span data-stu-id="8a8f5-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="8a8f5-238">Adicionando ícones e menus de contexto</span><span class="sxs-lookup"><span data-stu-id="8a8f5-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="8a8f5-239">Exemplo de código: extensões de Shell para manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="8a8f5-240">Criando um conector de pesquisa para um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="8a8f5-241">Depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a8f5-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
