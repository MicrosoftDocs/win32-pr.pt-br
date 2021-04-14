---
description: 'O exemplo de código ReindexMatchingUrls demonstra como fornecer três maneiras de especificar os arquivos a serem reindexados: URLs que correspondem a um tipo de arquivo, tipo MIME ou uma cláusula WHERE especificada.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460984"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="e0537-103">ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="e0537-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="e0537-104">O exemplo de código ReindexMatchingUrls demonstra como fornecer três maneiras de especificar os arquivos a serem reindexados: URLs que correspondem a um tipo de arquivo, tipo MIME ou uma cláusula WHERE especificada.</span><span class="sxs-lookup"><span data-stu-id="e0537-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="e0537-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0537-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="e0537-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="e0537-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="e0537-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e0537-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="e0537-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e0537-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="e0537-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e0537-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="e0537-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0537-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="e0537-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0537-111">Requirements</span></span>

| <span data-ttu-id="e0537-112">Produto</span><span class="sxs-lookup"><span data-stu-id="e0537-112">Product</span></span>     | <span data-ttu-id="e0537-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="e0537-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="e0537-114">Windows</span><span class="sxs-lookup"><span data-stu-id="e0537-114">Windows</span></span>     | <span data-ttu-id="e0537-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="e0537-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="e0537-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="e0537-116">Windows SDK</span></span> | <span data-ttu-id="e0537-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="e0537-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="e0537-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e0537-118">Downloading the Sample</span></span>

<span data-ttu-id="e0537-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0537-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="e0537-120">Local</span><span class="sxs-lookup"><span data-stu-id="e0537-120">Location</span></span>      | <span data-ttu-id="e0537-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="e0537-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="e0537-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="e0537-122">GitHub</span></span>  | [<span data-ttu-id="e0537-123">Exemplo de ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="e0537-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="e0537-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="e0537-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="e0537-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e0537-125">Building the Sample</span></span>

1. <span data-ttu-id="e0537-126">Abra o Windows Explorer e navegue até o diretório do projeto **ReindexMatchingUrls** .</span><span class="sxs-lookup"><span data-stu-id="e0537-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="e0537-127">Por exemplo, o caminho de instalação padrão completo é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .</span><span class="sxs-lookup"><span data-stu-id="e0537-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="e0537-128">Clique duas vezes no ícone do arquivo REINDEX. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e0537-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="e0537-129">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="e0537-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="e0537-130">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="e0537-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="e0537-131">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="e0537-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="e0537-132">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="e0537-132">Running the Sample</span></span>

1. <span data-ttu-id="e0537-133">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e0537-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="e0537-134">No prompt de comando, digite `Reindex.exe` ou, no Windows Explorer, clique duas vezes no ícone para Reindex.exe.</span><span class="sxs-lookup"><span data-stu-id="e0537-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0537-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0537-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="e0537-136">Referência</span><span class="sxs-lookup"><span data-stu-id="e0537-136">Reference</span></span>

[<span data-ttu-id="e0537-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="e0537-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="e0537-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="e0537-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="e0537-139">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="e0537-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="e0537-140">**ISearchPersistentItemsChangedSink**</span><span class="sxs-lookup"><span data-stu-id="e0537-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="e0537-141">**ISearchViewChangedSink**</span><span class="sxs-lookup"><span data-stu-id="e0537-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="e0537-142">**PRIORIZAr \_ sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="e0537-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="e0537-143">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="e0537-143">Other Samples</span></span>

[<span data-ttu-id="e0537-144">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="e0537-144">Search Code Samples</span></span>](-search-samples-ovw.md)
