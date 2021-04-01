---
description: Esta seção fornece informações conceituais necessárias para a implementação, a extensão e o teste de manipuladores de protocolo.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Desenvolvendo manipuladores de protocolo para o Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646881"
---
# <a name="developing-protocol-handlers-for-windows-search"></a><span data-ttu-id="57228-103">Desenvolvendo manipuladores de protocolo para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="57228-103">Developing Protocol Handlers for Windows Search</span></span>

<span data-ttu-id="57228-104">Esta seção fornece informações conceituais necessárias para a implementação, a extensão e o teste de manipuladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="57228-104">This section provides conceptual information necessary for the implementation, extension and testing of protocol handlers.</span></span>

-   [<span data-ttu-id="57228-105">Noções básicas sobre manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="57228-105">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
-   [<span data-ttu-id="57228-106">Notificando o índice das alterações</span><span class="sxs-lookup"><span data-stu-id="57228-106">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
-   [<span data-ttu-id="57228-107">Adicionando ícones e menus de contexto</span><span class="sxs-lookup"><span data-stu-id="57228-107">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
-   [<span data-ttu-id="57228-108">Exemplo de código: extensões de Shell para manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="57228-108">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
-   [<span data-ttu-id="57228-109">Instalando e Registrando manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="57228-109">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
-   [<span data-ttu-id="57228-110">Criando um conector de pesquisa para um manipulador de protocolo</span><span class="sxs-lookup"><span data-stu-id="57228-110">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
-   [<span data-ttu-id="57228-111">Depuração de manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="57228-111">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a><span data-ttu-id="57228-112">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="57228-112">Additional Resources</span></span>

<span data-ttu-id="57228-113">Para obter informações conceituais sobre indexação, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="57228-113">For conceptual background on indexing, see the following topics:</span></span>

-   <span data-ttu-id="57228-114">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="57228-114">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="57228-115">Para estender o Windows Search para indexar o conteúdo e as propriedades de novos formatos de arquivo e armazenamentos de dados, consulte [estendendo o índice](-search-3x-wds-extidx-overview.md).</span><span class="sxs-lookup"><span data-stu-id="57228-115">To extend Windows Search to index the contents and properties of new file formats and data stores, see [Extending the Index](-search-3x-wds-extidx-overview.md).</span></span>
-   <span data-ttu-id="57228-116">Para obter visões gerais do Gerenciador de catálogo e do CSM (Gerenciador de pesquisa de catálogo), consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="57228-116">For overviews of the Catalog Manager and Catalog Search Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

<span data-ttu-id="57228-117">Para obter um plano de fundo conceitual sobre os tipos de arquivo e manipuladores, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="57228-117">For conceptual background on file types and handlers, see the following topics:</span></span>

-   <span data-ttu-id="57228-118">Para estender o shell com manipuladores de tipo de arquivo, consulte [criando manipuladores de extensão de shell](../shell/handlers.md).</span><span class="sxs-lookup"><span data-stu-id="57228-118">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](../shell/handlers.md).</span></span>
-   <span data-ttu-id="57228-119">Para obter informações conceituais sobre manipuladores de filtro, consulte [desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md).</span><span class="sxs-lookup"><span data-stu-id="57228-119">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>
-   <span data-ttu-id="57228-120">Para obter informações sobre como criar manipuladores, consulte [introdução a associações de arquivos](../shell/fa-intro.md), [registro de extensões de shell](../shell/reg-shell-exts.md), criação de [manipuladores de extensão de shell](../shell/handlers.md), menu de [contexto](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [gerenciadores de visualização](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="57228-120">For information about creating handlers, see [Introduction to File Associations](../shell/fa-intro.md), [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [Preview Handlers](../shell/preview-handlers.md).</span></span>

<span data-ttu-id="57228-121">Para obter informações sobre tecnologias relacionadas e sobre como implementar um armazenamento de dados, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="57228-121">For background on related technologies and on implementing a data store, see the following topics:</span></span>

-   <span data-ttu-id="57228-122">Os manipuladores de protocolo de pesquisa do Windows usam especificações de design semelhantes ao SharePoint Server e, em geral, podem ser usados de maneira intercambiável.</span><span class="sxs-lookup"><span data-stu-id="57228-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="57228-123">Para obter mais informações, consulte [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span><span class="sxs-lookup"><span data-stu-id="57228-123">For more information, see [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span></span>
-   <span data-ttu-id="57228-124">No Windows 7 e posterior, o SharePoint Search Server 2008 e o MOSS 2007 SP2 também oferecem suporte à pesquisa federada.</span><span class="sxs-lookup"><span data-stu-id="57228-124">In Windows 7 and later, SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search.</span></span> <span data-ttu-id="57228-125">Para obter mais informações sobre a pesquisa federada e a implantação do servidor de pesquisa 2008 com o Office SharePoint Server 2007, consulte [servidor de pesquisa de pesquisa federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="57228-125">For more information about federated search and Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>
-   <span data-ttu-id="57228-126">Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57228-126">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="57228-127">Para obter exemplos de código, consulte as seguintes páginas do portal:</span><span class="sxs-lookup"><span data-stu-id="57228-127">For code samples, see the following portal pages:</span></span>

-   <span data-ttu-id="57228-128">Para obter exemplos de código de pesquisa, consulte [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="57228-128">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="57228-129">Para obter exemplos de código de Shell, consulte [shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57228-129">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

 

 
