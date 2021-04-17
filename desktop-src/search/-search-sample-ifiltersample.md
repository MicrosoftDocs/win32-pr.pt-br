---
description: O exemplo de código IFilterSample demonstra como criar uma classe base IFilter para implementar a interface IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785054"
---
# <a name="ifiltersample"></a><span data-ttu-id="d9311-103">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="d9311-103">IFilterSample</span></span>

<span data-ttu-id="d9311-104">O exemplo de código IFilterSample demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="d9311-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="d9311-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9311-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="d9311-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="d9311-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="d9311-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9311-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="d9311-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9311-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="d9311-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9311-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="d9311-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9311-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="d9311-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9311-111">Requirements</span></span>

| <span data-ttu-id="d9311-112">Produto</span><span class="sxs-lookup"><span data-stu-id="d9311-112">Product</span></span>     | <span data-ttu-id="d9311-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="d9311-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="d9311-114">Windows</span><span class="sxs-lookup"><span data-stu-id="d9311-114">Windows</span></span>     | <span data-ttu-id="d9311-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="d9311-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="d9311-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="d9311-116">Windows SDK</span></span> | <span data-ttu-id="d9311-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="d9311-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="d9311-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9311-118">Downloading the Sample</span></span>

<span data-ttu-id="d9311-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9311-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="d9311-120">Local</span><span class="sxs-lookup"><span data-stu-id="d9311-120">Location</span></span>      | <span data-ttu-id="d9311-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="d9311-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d9311-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="d9311-122">GitHub</span></span>        | [<span data-ttu-id="d9311-123">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="d9311-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="d9311-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="d9311-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="d9311-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9311-125">Building the Sample</span></span>

1. <span data-ttu-id="d9311-126">Abra o Windows Explorer e navegue até o diretório do projeto **FilterBase** .</span><span class="sxs-lookup"><span data-stu-id="d9311-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="d9311-127">Clique duas vezes no ícone do arquivo FilterBase. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d9311-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="d9311-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="d9311-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="d9311-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="d9311-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="d9311-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="d9311-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d9311-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9311-131">Running the Sample</span></span>

1. <span data-ttu-id="d9311-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d9311-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="d9311-133">No prompt de comando, digite `FilterBase.exe` ou, no Windows Explorer, clique duas vezes no ícone para FilterBase.exe.</span><span class="sxs-lookup"><span data-stu-id="d9311-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9311-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9311-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="d9311-135">Referência</span><span class="sxs-lookup"><span data-stu-id="d9311-135">Reference</span></span>

[<span data-ttu-id="d9311-136">**Visio**</span><span class="sxs-lookup"><span data-stu-id="d9311-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="d9311-137">Conceitual</span><span class="sxs-lookup"><span data-stu-id="d9311-137">Conceptual</span></span>

[<span data-ttu-id="d9311-138">Desenvolvendo manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="d9311-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="d9311-139">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="d9311-139">Other Samples</span></span>

[<span data-ttu-id="d9311-140">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="d9311-140">Search Code Samples</span></span>](-search-samples-ovw.md)
