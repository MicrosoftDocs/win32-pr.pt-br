---
description: O Gerenciador de escopo de rastreamento (CSM) permite adicionar e remover raízes de pesquisa para os armazenamentos de dados de e para o escopo de rastreamento do Windows Search.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Gerenciando raízes de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164344"
---
# <a name="managing-search-roots"></a><span data-ttu-id="b1649-103">Gerenciando raízes de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b1649-103">Managing Search Roots</span></span>

<span data-ttu-id="b1649-104">O Gerenciador de escopo de rastreamento (CSM) permite adicionar e remover raízes de pesquisa para os armazenamentos de dados de e para o escopo de rastreamento do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="b1649-104">The Crawl Scope Manager (CSM) enables you to add and remove search roots for your data stores to and from the Windows Search crawl scope.</span></span>

<span data-ttu-id="b1649-105">Este tópico abrange os seguintes assuntos:</span><span class="sxs-lookup"><span data-stu-id="b1649-105">This topic includes the following subjects:</span></span>

-   [<span data-ttu-id="b1649-106">Sobre raízes de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b1649-106">About Search Roots</span></span>](#about-search-roots)
-   [<span data-ttu-id="b1649-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="b1649-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="b1649-108">Windows 7: nova API do Gerenciador de escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-108">Windows 7: New Crawl Scope Manager API</span></span>](#windows-7-new-crawl-scope-manager-api)
-   [<span data-ttu-id="b1649-109">Adicionando raízes ao escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-109">Adding Roots to the Crawl Scope</span></span>](#adding-roots-to-the-crawl-scope)
-   [<span data-ttu-id="b1649-110">Removendo raízes do escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-110">Removing Roots from the Crawl Scope</span></span>](#removing-roots-from-the-crawl-scope)
-   [<span data-ttu-id="b1649-111">Enumerando raízes no escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-111">Enumerating Roots in the Crawl Scope</span></span>](#enumerating-roots-in-the-crawl-scope)
-   [<span data-ttu-id="b1649-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1649-112">Related topics</span></span>](#related-topics)

 

## <a name="about-search-roots"></a><span data-ttu-id="b1649-113">Sobre raízes de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b1649-113">About Search Roots</span></span>

<span data-ttu-id="b1649-114">Uma raiz de pesquisa define a base de um namespace de Shell em que escopos específicos podem ser incluídos ou excluídos e geralmente é o contêiner de nível mais alto em um protocolo que pode ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="b1649-114">A search root defines the base of a Shell namespace where specific scopes could be included or excluded, and is usually the highest level container in a protocol that can be enumerated.</span></span> <span data-ttu-id="b1649-115">Ele não especifica quais partes desse armazenamento devem ou não ser indexadas; Ele simplesmente sinaliza que um repositório de conteúdo existe e está associado a um manipulador de protocolo registrado.</span><span class="sxs-lookup"><span data-stu-id="b1649-115">It does not specify which parts of this store should or should not be indexed; it merely signals that a content store exists and is associated with a registered protocol handler.</span></span> <span data-ttu-id="b1649-116">A sintaxe para identificar uma URL raiz de pesquisa inclui o protocolo, o identificador de segurança do repositório ou do usuário, o caminho e, opcionalmente, um item específico (como um arquivo).</span><span class="sxs-lookup"><span data-stu-id="b1649-116">The syntax for identifying a search root URL includes the protocol, the store or user's security identifier, the path, and optionally a specific item (like a file).</span></span> <span data-ttu-id="b1649-117">Os exemplos a seguir mostram duas formas da sintaxe para uma raiz de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b1649-117">The following examples show two forms of the syntax for a search root.</span></span>


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



<span data-ttu-id="b1649-118">O <protocol> segmento deve ser seguido de duas (2) barras "/" ("/"), a menos que seja o protocolo file:, que requer três barras (file:///).</span><span class="sxs-lookup"><span data-stu-id="b1649-118">The <protocol> segment must be followed by two (2) forward slashes ('/') unless it is the file: protocol, which requires three slashes (file:///).</span></span> <span data-ttu-id="b1649-119">O <site or SID> segmento representa um repositório de conteúdo ou um identificador de segurança de usuário se a raiz de pesquisa for destinada a ser específica ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b1649-119">The <site or SID> segment represents either a content store or a user security identifier if the search root is meant to be specific to the user.</span></span> <span data-ttu-id="b1649-120">O <path> segmento é um conjunto de contêineres, como diretórios ou pastas, e pode incluir o caractere curinga ' \* '.</span><span class="sxs-lookup"><span data-stu-id="b1649-120">The <path> segment is a set of containers, like directories or folders, and can include the wildcard character '\*'.</span></span> <span data-ttu-id="b1649-121">O</span><span class="sxs-lookup"><span data-stu-id="b1649-121">The</span></span> <item> <span data-ttu-id="b1649-122">o segmento é opcional e também pode incluir o caractere curinga ' \* '.</span><span class="sxs-lookup"><span data-stu-id="b1649-122">segment is optional and can also include the wildcard character '\*'.</span></span> <span data-ttu-id="b1649-123">Se você não incluir um item, certifique-se de concluir o segmento de caminho com uma barra ou o indexador irá pressupor que o último subcontêiner é um item.</span><span class="sxs-lookup"><span data-stu-id="b1649-123">If you do not include an item, be sure to finish your path segment with a slash or the indexer will assume that the last subcontainer is an item.</span></span>

<span data-ttu-id="b1649-124">Por exemplo, suponha que você implementou um manipulador de protocolo (myPH) para manipular arquivos do tipo \* . myext para um aplicativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b1649-124">For example, suppose you have implemented a protocol handler (myPH) to handle files of type \*.myext for a custom application.</span></span> <span data-ttu-id="b1649-125">Todos esses arquivos estarão localizados na pasta WorkteamA \\ ProjectFiles em um computador local.</span><span class="sxs-lookup"><span data-stu-id="b1649-125">All of these files will be located in the folder WorkteamA\\ProjectFiles on a local computer.</span></span> <span data-ttu-id="b1649-126">A raiz de pesquisa para isso pode ser assim:</span><span class="sxs-lookup"><span data-stu-id="b1649-126">The search root for that might look like this:</span></span>

-   <span data-ttu-id="b1649-127">myPH:///C: \\ WorkteamA \\ ProjectFiles</span><span class="sxs-lookup"><span data-stu-id="b1649-127">myPH:///C:\\WorkteamA\\ProjectFiles</span></span>\\

<span data-ttu-id="b1649-128">Suponha que você esteja planejando incluir todos os arquivos. myext, mas nada mais desse contêiner no índice.</span><span class="sxs-lookup"><span data-stu-id="b1649-128">Suppose you are planning to include all .myext files but nothing else from that container in the index.</span></span> <span data-ttu-id="b1649-129">A raiz de pesquisa para isso pode ser assim:</span><span class="sxs-lookup"><span data-stu-id="b1649-129">The search root for that might look like this:</span></span>

-   <span data-ttu-id="b1649-130">myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* . myext.</span><span class="sxs-lookup"><span data-stu-id="b1649-130">myPH:///C:\\WorkteamA\\ProjectFiles\\\*.myext.</span></span>

<span data-ttu-id="b1649-131">Os padrões de caractere curinga definem URLs usando o caractere curinga " \* " e são considerados um padrão em vez de uma URL, mas a terminologia geralmente é usada de forma intercambiável.</span><span class="sxs-lookup"><span data-stu-id="b1649-131">Wildcard patterns define URLs by using the wildcard character '\*' and are considered a pattern rather than a URL, but the terminology is often used interchangeably.</span></span> <span data-ttu-id="b1649-132">Por exemplo, file:///C: os \\ \\ \* \\ dados do projecta \\ corresponderão às seguintes URLs:</span><span class="sxs-lookup"><span data-stu-id="b1649-132">For example, file:///C:\\ProjectA\\\*\\data\\ would match the following URLs:</span></span>

-   <span data-ttu-id="b1649-133">C: \\ dados do projecta \\ **versão** </span><span class="sxs-lookup"><span data-stu-id="b1649-133">C:\\ProjectA\\**version1**\\data</span></span>\\\\
-   <span data-ttu-id="b1649-134">C: \\ dados do projecta \\ **Version2** </span><span class="sxs-lookup"><span data-stu-id="b1649-134">C:\\ProjectA\\**version2**\\data</span></span>\\\\

<span data-ttu-id="b1649-135">Mas esse padrão não corresponde a essa URL:</span><span class="sxs-lookup"><span data-stu-id="b1649-135">But that pattern would not match this URL:</span></span>

-   <span data-ttu-id="b1649-136">C: \\ \\ **dados \\ temporários** do projecta versão </span><span class="sxs-lookup"><span data-stu-id="b1649-136">C:\\ProjectA\\**version1\\temp**\\data</span></span>\\\\

<span data-ttu-id="b1649-137">Você deve criar novas raízes de pesquisa para contêineres que ainda não estão no escopo de rastreamento do indexador.</span><span class="sxs-lookup"><span data-stu-id="b1649-137">You should create new search roots for containers that are not already in the crawl scope of the indexer.</span></span> <span data-ttu-id="b1649-138">Se o caminho C: \\ ParentScope já estiver incluído no escopo de rastreamento, você não precisará adicionar uma nova raiz de pesquisa para C: \\ ParentScope \\ ChildScope, a menos que você saiba que o escopo filho foi excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b1649-138">If path C:\\ParentScope is already included in the crawl scope, you do not need to add a new search root for C:\\ParentScope\\ChildScope unless you know that the child scope was previously excluded.</span></span>

<span data-ttu-id="b1649-139">A interface do usuário para definir as opções de pesquisa do Windows exibe raízes de pesquisa para os usuários para que eles possam refinar as regras de escopo para suas pesquisas.</span><span class="sxs-lookup"><span data-stu-id="b1649-139">The user interface for setting Windows Search options displays search roots to users so they can refine the scope rules for their searches.</span></span> <span data-ttu-id="b1649-140">Como parte do processo de instalação para seu manipulador de protocolo, contêiner e/ou aplicativo personalizado, você pode definir um escopo de rastreamento padrão, com regras de inclusão e exclusão.</span><span class="sxs-lookup"><span data-stu-id="b1649-140">As part of the installation process for your custom protocol handler, container, and/or application, you might define a default crawl scope, with inclusion and exclusion rules.</span></span> <span data-ttu-id="b1649-141">Essas regras são apresentadas aos usuários finais como locais.</span><span class="sxs-lookup"><span data-stu-id="b1649-141">These rules are presented to end users as locations.</span></span> <span data-ttu-id="b1649-142">Os usuários podem navegar dentro dos subdiretórios de sua raiz de pesquisa predefinida e selecionar aqueles que desejam incluir nas pesquisas ou desmarcar aqueles que desejam excluir.</span><span class="sxs-lookup"><span data-stu-id="b1649-142">Users can navigate within the subdirectories of your predefined search root and select the ones they want to include in searches or clear the ones they want to exclude.</span></span>

 

## <a name="before-you-begin"></a><span data-ttu-id="b1649-143">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="b1649-143">Before You Begin</span></span>

<span data-ttu-id="b1649-144">Antes de poder usar qualquer uma das interfaces do CSM (Gerenciador de escopo de rastreamento), você deve executar as seguintes etapas de pré-requisito:</span><span class="sxs-lookup"><span data-stu-id="b1649-144">Before you can use any of the Crawl Scope Manager (CSM) interfaces, you must perform the following prerequisite steps:</span></span>

1.  <span data-ttu-id="b1649-145">Crie o objeto **CrawlSearchManager** e obtenha sua interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .</span><span class="sxs-lookup"><span data-stu-id="b1649-145">Create the **CrawlSearchManager** object and obtain its [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) interface.</span></span>
2.  <span data-ttu-id="b1649-146">Chame [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) para "SystemIndex" para obter uma instância de uma interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="b1649-146">Call [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) for "SystemIndex" to obtain an instance of an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface.</span></span>
3.  <span data-ttu-id="b1649-147">Chame [**ISearchCatalogManager:: GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) para obter uma instância da interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .</span><span class="sxs-lookup"><span data-stu-id="b1649-147">Call [**ISearchCatalogManager::GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) to obtain an instance of [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.</span></span>

<span data-ttu-id="b1649-148">Depois de fazer alterações no Gerenciador de escopo de rastreamento (CSM), você deve chamar [**ISearchCrawlScopeManager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall).</span><span class="sxs-lookup"><span data-stu-id="b1649-148">After making any changes to the Crawl Scope Manager (CSM), you must call [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall).</span></span> <span data-ttu-id="b1649-149">Esse método não usa parâmetros e retorna S \_ OK em caso de êxito.</span><span class="sxs-lookup"><span data-stu-id="b1649-149">This method takes no parameters and returns S\_OK on success.</span></span>

 

## <a name="windows-7-new-crawl-scope-manager-api"></a><span data-ttu-id="b1649-150">Windows 7: nova API do Gerenciador de escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-150">Windows 7: New Crawl Scope Manager API</span></span>

<span data-ttu-id="b1649-151">No **Windows 7 e posterior**, o [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende a funcionalidade da interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .</span><span class="sxs-lookup"><span data-stu-id="b1649-151">In **Windows 7 and later**, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends the functionality of the [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface.</span></span> <span data-ttu-id="b1649-152">O método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) Obtém a versão do CSM (Gerenciador de escopo de rastreamento), que informa os clientes se o estado do CSM foi alterado.</span><span class="sxs-lookup"><span data-stu-id="b1649-152">The [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method gets the Crawl Scope Manager (CSM) version, which informs clients if the state of the CSM has changed.</span></span> <span data-ttu-id="b1649-153">**ISearchCrawlScopeManager2:: GetVersion** não resulta em uma chamada de processo cruzado.</span><span class="sxs-lookup"><span data-stu-id="b1649-153">**ISearchCrawlScopeManager2::GetVersion** does not result in a cross-process call.</span></span> <span data-ttu-id="b1649-154">Se a função for bem sucedido, o ponteiro retornado permanecerá válido até que o cliente chame **UnmapViewOfFile** no ponteiro e **CloseHandle** no identificador retornado.</span><span class="sxs-lookup"><span data-stu-id="b1649-154">If the function succeeds, then the pointer that is returned remains valid until the client calls **UnmapViewOfFile** on the pointer and **CloseHandle** on the returned handle.</span></span>

 

## <a name="adding-roots-to-the-crawl-scope"></a><span data-ttu-id="b1649-155">Adicionando raízes ao escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-155">Adding Roots to the Crawl Scope</span></span>

<span data-ttu-id="b1649-156">O [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) informa ao mecanismo de pesquisa sobre contêineres para rastreamento e/ou inspeção e itens sob esses contêineres para incluir ou excluir.</span><span class="sxs-lookup"><span data-stu-id="b1649-156">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) tells the search engine about containers to crawl and/or watch, and items under those containers to include or exclude.</span></span> <span data-ttu-id="b1649-157">Para adicionar uma nova raiz de pesquisa, crie uma instância de um objeto [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) , defina os atributos raiz e, em seguida, chame [**ISearchCrawlScopeManager:: addroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) e passe-o para um ponteiro para o objeto **ISearchRoot** .</span><span class="sxs-lookup"><span data-stu-id="b1649-157">To add a new search root, instantiate an [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) object, set the root attributes, and then call [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) and pass it a pointer to your **ISearchRoot** object.</span></span> <span data-ttu-id="b1649-158">A URL da raiz de pesquisa tem a mesma forma que a raiz de pesquisa descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b1649-158">The search root URL takes the same form as the search root described earlier.</span></span>

<span data-ttu-id="b1649-159">A tabela a seguir descreve os métodos Put relevantes para [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); os outros métodos Put da interface não são usados atualmente pelo Windows Search.</span><span class="sxs-lookup"><span data-stu-id="b1649-159">The following table describes the relevant put methods for [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); the interface's other put methods are not used currently by Windows Search.</span></span> <span data-ttu-id="b1649-160">É recomendável incluir os SIDs (identificadores de segurança) dos usuários em todas as raízes para melhorar a segurança.</span><span class="sxs-lookup"><span data-stu-id="b1649-160">We recommend including the users' security identifiers (SIDs) in all roots for better security.</span></span> <span data-ttu-id="b1649-161">As raízes por usuário são mais seguras conforme as consultas são executadas em um processo por usuário, garantindo que um usuário não possa ver itens indexados da caixa de entrada de outro usuário, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="b1649-161">Per-user roots are more secure as queries are run in a per-user process, ensuring that one user cannot see items indexed from another user's inbox, for example.</span></span>



| <span data-ttu-id="b1649-162">Método</span><span class="sxs-lookup"><span data-stu-id="b1649-162">Method</span></span>                     | <span data-ttu-id="b1649-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1649-163">Description</span></span>                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1649-164">colocar \_ ProvidesNotifications</span><span class="sxs-lookup"><span data-stu-id="b1649-164">put\_ProvidesNotifications</span></span> | <span data-ttu-id="b1649-165">Defina como **true** se um manipulador de protocolo ou outro aplicativo notificará o mecanismo de pesquisa sobre as alterações nas URLs na raiz de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b1649-165">Set to **TRUE** if a protocol handler or other application will notify the search engine about changes to the URLs under the search root.</span></span> <span data-ttu-id="b1649-166">A notificação indica que as URLs precisam de reindexação.</span><span class="sxs-lookup"><span data-stu-id="b1649-166">The notification indicates that the URLs need reindexing.</span></span> |
| <span data-ttu-id="b1649-167">colocar \_ RootURL</span><span class="sxs-lookup"><span data-stu-id="b1649-167">put\_RootURL</span></span>               | <span data-ttu-id="b1649-168">Define a URL raiz da pesquisa atual.</span><span class="sxs-lookup"><span data-stu-id="b1649-168">Sets the root URL of the current search.</span></span> <span data-ttu-id="b1649-169">A URL usa o formulário raiz de pesquisa descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b1649-169">The URL takes the search root form described earlier.</span></span>                                                                                                      |



 

 

<span data-ttu-id="b1649-170">Por padrão, o indexador não rastreia um escopo quando você adiciona uma raiz de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b1649-170">By default, the indexer does not crawl a scope when you add a search root.</span></span> <span data-ttu-id="b1649-171">Você também deve adicionar uma regra de inclusão para a raiz.</span><span class="sxs-lookup"><span data-stu-id="b1649-171">You must also add an include rule for the root.</span></span> <span data-ttu-id="b1649-172">Se você quiser adicionar uma raiz específica do usuário para um aplicativo, esse aplicativo deverá adicionar as raízes apropriadas para novos usuários quando o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="b1649-172">If you want to add a user-specific root for an application, that application should add the appropriate roots for new users when the application starts.</span></span>

<span data-ttu-id="b1649-173">Para adicionar as raízes apropriadas para novos usuários:</span><span class="sxs-lookup"><span data-stu-id="b1649-173">To add the appropriate roots for new users:</span></span>

1.  <span data-ttu-id="b1649-174">Obtenha o SID do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1649-174">Get the user's SID.</span></span>
2.  <span data-ttu-id="b1649-175">Enumere todas as raízes para verificar se existe uma para esse SID.</span><span class="sxs-lookup"><span data-stu-id="b1649-175">Enumerate all roots to check whether one exists for this SID.</span></span>
3.  <span data-ttu-id="b1649-176">Adicione uma nova raiz, usando o SID, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b1649-176">Add a new root, using the SID, if necessary.</span></span>

 

## <a name="removing-roots-from-the-crawl-scope"></a><span data-ttu-id="b1649-177">Removendo raízes do escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-177">Removing Roots from the Crawl Scope</span></span>

<span data-ttu-id="b1649-178">Você pode usar [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para remover uma raiz do escopo de rastreamento quando não quiser mais que a URL seja indexada.</span><span class="sxs-lookup"><span data-stu-id="b1649-178">You can use [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) to remove a root from the crawl scope when you no longer want that URL indexed.</span></span> <span data-ttu-id="b1649-179">A remoção de uma raiz também exclui todas as regras de escopo dessa URL.</span><span class="sxs-lookup"><span data-stu-id="b1649-179">Removing a root also deletes all scope rules for that URL.</span></span> <span data-ttu-id="b1649-180">Por exemplo, suponha que você deseja desinstalar um repositório de conteúdo e/ou seu manipulador de protocolo de um sistema.</span><span class="sxs-lookup"><span data-stu-id="b1649-180">For example, suppose you want to uninstall a content store and/or its protocol handler from a system.</span></span> <span data-ttu-id="b1649-181">Você pode desinstalar o aplicativo, remover todos os dados e, em seguida, remover a raiz de pesquisa do escopo de rastreamento, e o Gerenciador de escopo de rastreamento removerá a raiz e todas as regras de escopo associadas à raiz.</span><span class="sxs-lookup"><span data-stu-id="b1649-181">You can uninstall the application, remove all data, and then remove the search root from the crawl scope, and the Crawl Scope Manager will remove the root and all scope rules associated with the root.</span></span>

<span data-ttu-id="b1649-182">Para remover uma raiz de pesquisa existente, chame [**ISearchCrawlScopeManager:: RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) com a raiz de pesquisa que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="b1649-182">To remove an existing search root, call [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) with the search root you want to remove.</span></span> <span data-ttu-id="b1649-183">A URL da raiz de pesquisa tem a mesma forma que a raiz de pesquisa descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b1649-183">The search root URL takes the same form as the search root described earlier.</span></span> <span data-ttu-id="b1649-184">Esse método retornará S \_ false se a raiz não for encontrada e um código de erro se houvesse um erro ao remover uma raiz que foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="b1649-184">This method returns S\_FALSE if the root is not found and an error code if there was an error removing a root that was found.</span></span>

<span data-ttu-id="b1649-185">A remoção de uma raiz de pesquisa também remove a URL da interface do usuário para as opções de pesquisa do Windows, para que os usuários não possam adicionar novamente esse contêiner ou local usando a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1649-185">Removing a search root also removes the URL from the user interface for Windows Search options, so users may not be able to re-add that container or location using the user interface.</span></span> <span data-ttu-id="b1649-186">Também é possível remover todas as substituições do conjunto de usuários de uma raiz de pesquisa e reverter para as regras raiz de pesquisa original e escopo.</span><span class="sxs-lookup"><span data-stu-id="b1649-186">It is also possible to remove all user-set overrides of a search root and revert to the original search root and scope rules.</span></span> <span data-ttu-id="b1649-187">Para obter mais informações, consulte [Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-187">For more information, see [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md).</span></span>

> [!Note]  
> <span data-ttu-id="b1649-188">No Windows Vista, se os usuários forem removidos por meio de perfis de usuário no painel de controle, CSM removerá todas as regras e raízes com seu SID e removerá seus itens indexados do catálogo.</span><span class="sxs-lookup"><span data-stu-id="b1649-188">On Windows Vista, if users are removed through User Profiles in Control Panel, CSM removes all rules and roots with their SID and removes their indexed items from the catalog.</span></span> <span data-ttu-id="b1649-189">No Windows XP, você precisa remover as raízes e as regras dos usuários manualmente.</span><span class="sxs-lookup"><span data-stu-id="b1649-189">On Windows XP, you need to remove the users' roots and rules manually.</span></span>

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a><span data-ttu-id="b1649-190">Enumerando raízes no escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-190">Enumerating Roots in the Crawl Scope</span></span>

<span data-ttu-id="b1649-191">O CSM enumera raízes de pesquisa usando uma interface de enumerador de estilo COM padrão, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots).</span><span class="sxs-lookup"><span data-stu-id="b1649-191">The CSM enumerates search roots using a standard COM-style enumerator interface, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots).</span></span> <span data-ttu-id="b1649-192">Você pode usar essa interface para enumerar raízes de pesquisa para várias finalidades.</span><span class="sxs-lookup"><span data-stu-id="b1649-192">You can use this interface to enumerate search roots for a number of purposes.</span></span> <span data-ttu-id="b1649-193">Por exemplo, talvez você queira exibir todo o escopo de rastreamento em uma interface do usuário ou descobrir se uma raiz específica ou o filho de uma raiz já está no escopo do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="b1649-193">For example, you might want to display the entire crawl scope in a user interface, or discover whether a particular root or the child of a root is already in the crawl scope.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b1649-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1649-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b1649-195">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b1649-195">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1649-196">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="b1649-196">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[<span data-ttu-id="b1649-197">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="b1649-197">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[<span data-ttu-id="b1649-198">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="b1649-198">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

<span data-ttu-id="b1649-199">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b1649-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1649-200">Usando o Gerenciador de escopo de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b1649-200">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[<span data-ttu-id="b1649-201">Gerenciando regras de escopo</span><span class="sxs-lookup"><span data-stu-id="b1649-201">Managing Scope Rules</span></span>](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



