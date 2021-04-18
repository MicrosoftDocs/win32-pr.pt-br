---
description: O exemplo de código CrawlScopeCommandLine demonstra como definir opções de linha de comando para operações de indexação do Gerenciador de escopo de rastreamento (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788719"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="7438e-103">CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="7438e-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="7438e-104">O exemplo de código CrawlScopeCommandLine demonstra como definir opções de linha de comando para operações de indexação do Gerenciador de escopo de rastreamento (CSM).</span><span class="sxs-lookup"><span data-stu-id="7438e-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="7438e-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7438e-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="7438e-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="7438e-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="7438e-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7438e-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="7438e-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7438e-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="7438e-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7438e-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="7438e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7438e-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="7438e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7438e-111">Requirements</span></span>

| <span data-ttu-id="7438e-112">Produto</span><span class="sxs-lookup"><span data-stu-id="7438e-112">Product</span></span>     | <span data-ttu-id="7438e-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="7438e-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="7438e-114">Windows</span><span class="sxs-lookup"><span data-stu-id="7438e-114">Windows</span></span>     | <span data-ttu-id="7438e-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="7438e-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="7438e-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="7438e-116">Windows SDK</span></span> | <span data-ttu-id="7438e-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="7438e-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="7438e-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7438e-118">Downloading the Sample</span></span>

<span data-ttu-id="7438e-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="7438e-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="7438e-120">Local</span><span class="sxs-lookup"><span data-stu-id="7438e-120">Location</span></span> | <span data-ttu-id="7438e-121">Caminho ou URL</span><span class="sxs-lookup"><span data-stu-id="7438e-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="7438e-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="7438e-122">GitHub</span></span>   |    [<span data-ttu-id="7438e-123">Exemplo de CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="7438e-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="7438e-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="7438e-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="7438e-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7438e-125">Building the Sample</span></span>

1. <span data-ttu-id="7438e-126">Abra o Windows Explorer e navegue até o diretório do projeto **CrawlScopeCommandLine** .</span><span class="sxs-lookup"><span data-stu-id="7438e-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="7438e-127">Clique duas vezes no ícone do arquivo csmcmd. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7438e-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="7438e-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="7438e-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="7438e-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="7438e-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="7438e-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="7438e-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7438e-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7438e-131">Running the Sample</span></span>

1. <span data-ttu-id="7438e-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7438e-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="7438e-133">No prompt de comando, digite `csmcmd.exe` ou, no Windows Explorer, clique duas vezes no ícone para csmcmd.exe.</span><span class="sxs-lookup"><span data-stu-id="7438e-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7438e-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7438e-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="7438e-135">Referência</span><span class="sxs-lookup"><span data-stu-id="7438e-135">Reference</span></span>

[<span data-ttu-id="7438e-136">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="7438e-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="7438e-137">**IEnumSearchScopeRules**</span><span class="sxs-lookup"><span data-stu-id="7438e-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="7438e-138">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="7438e-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="7438e-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="7438e-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="7438e-140">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="7438e-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="7438e-141">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="7438e-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="7438e-142">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="7438e-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="7438e-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="7438e-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="7438e-144">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="7438e-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="7438e-145">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="7438e-145">Other Samples</span></span>

[<span data-ttu-id="7438e-146">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="7438e-146">Search Code Samples</span></span>](-search-samples-ovw.md)
