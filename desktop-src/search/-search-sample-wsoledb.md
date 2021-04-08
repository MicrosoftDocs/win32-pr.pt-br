---
description: O exemplo de código WSOleDB demonstra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e demonstra dois métodos adicionais para recuperar os resultados do Windows Search.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826911"
---
# <a name="wsoledb"></a><span data-ttu-id="ade90-103">WSOleDB</span><span class="sxs-lookup"><span data-stu-id="ade90-103">WSOleDB</span></span>

<span data-ttu-id="ade90-104">O exemplo de código WSOleDB demonstra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e demonstra dois métodos adicionais para recuperar os resultados do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="ade90-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="ade90-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ade90-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="ade90-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="ade90-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="ade90-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ade90-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="ade90-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ade90-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="ade90-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ade90-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="ade90-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ade90-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="ade90-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade90-111">Requirements</span></span>

| <span data-ttu-id="ade90-112">Produto</span><span class="sxs-lookup"><span data-stu-id="ade90-112">Product</span></span>     | <span data-ttu-id="ade90-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="ade90-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="ade90-114">Windows</span><span class="sxs-lookup"><span data-stu-id="ade90-114">Windows</span></span>     | <span data-ttu-id="ade90-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="ade90-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="ade90-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="ade90-116">Windows SDK</span></span> | <span data-ttu-id="ade90-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="ade90-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="ade90-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ade90-118">Downloading the Sample</span></span>

<span data-ttu-id="ade90-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="ade90-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="ade90-120">Local</span><span class="sxs-lookup"><span data-stu-id="ade90-120">Location</span></span>      | <span data-ttu-id="ade90-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="ade90-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ade90-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="ade90-122">GitHub</span></span>        | [<span data-ttu-id="ade90-123">Exemplo de WSOleDB</span><span class="sxs-lookup"><span data-stu-id="ade90-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="ade90-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="ade90-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="ade90-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ade90-125">Building the Sample</span></span>

1. <span data-ttu-id="ade90-126">Abra o Windows Explorer e navegue até o diretório do projeto **WSOleDB** .</span><span class="sxs-lookup"><span data-stu-id="ade90-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="ade90-127">Clique duas vezes no ícone do arquivo WSOleDB. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ade90-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="ade90-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="ade90-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="ade90-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="ade90-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="ade90-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="ade90-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ade90-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ade90-131">Running the Sample</span></span>

1. <span data-ttu-id="ade90-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="ade90-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="ade90-133">No prompt de comando, digite `WSOleDB.exe` ou, no Windows Explorer, clique duas vezes no ícone para WSOleDB.exe.</span><span class="sxs-lookup"><span data-stu-id="ade90-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ade90-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ade90-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="ade90-135">Referência</span><span class="sxs-lookup"><span data-stu-id="ade90-135">Reference</span></span>

[<span data-ttu-id="ade90-136">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="ade90-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="ade90-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="ade90-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="ade90-138">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="ade90-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="ade90-139">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="ade90-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="ade90-140">Conceitual</span><span class="sxs-lookup"><span data-stu-id="ade90-140">Conceptual</span></span>

[<span data-ttu-id="ade90-141">Visão geral da programação de OLE DB</span><span class="sxs-lookup"><span data-stu-id="ade90-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="ade90-142">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="ade90-142">Other Samples</span></span>

[<span data-ttu-id="ade90-143">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="ade90-143">Search Code Samples</span></span>](-search-samples-ovw.md)
