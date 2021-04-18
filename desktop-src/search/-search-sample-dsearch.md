---
description: O exemplo de código DSearch demonstra como criar uma classe para um aplicativo de console estático para consultar o Windows Search usando o assembly Microsoft. Search. Interop para ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813524"
---
# <a name="dsearch"></a><span data-ttu-id="37d32-103">DSearch</span><span class="sxs-lookup"><span data-stu-id="37d32-103">DSearch</span></span>

<span data-ttu-id="37d32-104">O exemplo de código DSearch demonstra como criar uma classe para um aplicativo de console estático para consultar o Windows Search usando o assembly Microsoft. Search. Interop para [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="37d32-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="37d32-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="37d32-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="37d32-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="37d32-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="37d32-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="37d32-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="37d32-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="37d32-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="37d32-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="37d32-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="37d32-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37d32-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="37d32-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37d32-111">Requirements</span></span>

| <span data-ttu-id="37d32-112">Produto</span><span class="sxs-lookup"><span data-stu-id="37d32-112">Product</span></span>     | <span data-ttu-id="37d32-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="37d32-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="37d32-114">Windows</span><span class="sxs-lookup"><span data-stu-id="37d32-114">Windows</span></span>     | <span data-ttu-id="37d32-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="37d32-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="37d32-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="37d32-116">Windows SDK</span></span> | <span data-ttu-id="37d32-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="37d32-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="37d32-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="37d32-118">Downloading the Sample</span></span>

<span data-ttu-id="37d32-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="37d32-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="37d32-120">Local</span><span class="sxs-lookup"><span data-stu-id="37d32-120">Location</span></span>      | <span data-ttu-id="37d32-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="37d32-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="37d32-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="37d32-122">GitHub</span></span>        | [<span data-ttu-id="37d32-123">Exemplo de DSearch</span><span class="sxs-lookup"><span data-stu-id="37d32-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="37d32-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="37d32-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="37d32-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="37d32-125">Building the Sample</span></span>

1. <span data-ttu-id="37d32-126">Abra o Windows Explorer e navegue até o diretório do projeto **DSearch** .</span><span class="sxs-lookup"><span data-stu-id="37d32-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="37d32-127">Clique duas vezes no ícone do arquivo DSearch. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37d32-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="37d32-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="37d32-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="37d32-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="37d32-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="37d32-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="37d32-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="37d32-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="37d32-131">Running the Sample</span></span>

1. <span data-ttu-id="37d32-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="37d32-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="37d32-133">No prompt de comando, digite `DSearch.exe` ou, no Windows Explorer, clique duas vezes no ícone para DSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="37d32-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37d32-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37d32-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="37d32-135">Referência</span><span class="sxs-lookup"><span data-stu-id="37d32-135">Reference</span></span>

[<span data-ttu-id="37d32-136">**ISearchQueryHelper**</span><span class="sxs-lookup"><span data-stu-id="37d32-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="37d32-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="37d32-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="37d32-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="37d32-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="37d32-139">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="37d32-139">Other Samples</span></span>

[<span data-ttu-id="37d32-140">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="37d32-140">Search Code Samples</span></span>](-search-samples-ovw.md)
