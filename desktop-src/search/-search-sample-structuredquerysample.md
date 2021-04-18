---
description: O exemplo de código StructuredQuerySample demonstra como ler linhas do console, analisá-las usando o esquema do sistema e exibir as árvores de condição resultantes.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760495"
---
# <a name="structuredquerysample"></a><span data-ttu-id="1bc2a-103">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="1bc2a-103">StructuredQuerySample</span></span>

<span data-ttu-id="1bc2a-104">O exemplo de código StructuredQuerySample demonstra como ler linhas do console, analisá-las usando o esquema do sistema e exibir as árvores de condição resultantes.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="1bc2a-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="1bc2a-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="1bc2a-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="1bc2a-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1bc2a-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="1bc2a-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1bc2a-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="1bc2a-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1bc2a-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="1bc2a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bc2a-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="1bc2a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bc2a-111">Requirements</span></span>

| <span data-ttu-id="1bc2a-112">Produto</span><span class="sxs-lookup"><span data-stu-id="1bc2a-112">Product</span></span>     | <span data-ttu-id="1bc2a-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="1bc2a-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="1bc2a-114">Windows</span><span class="sxs-lookup"><span data-stu-id="1bc2a-114">Windows</span></span>     | <span data-ttu-id="1bc2a-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="1bc2a-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="1bc2a-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="1bc2a-116">Windows SDK</span></span> | <span data-ttu-id="1bc2a-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="1bc2a-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="1bc2a-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1bc2a-118">Downloading the Sample</span></span>

<span data-ttu-id="1bc2a-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="1bc2a-120">Local</span><span class="sxs-lookup"><span data-stu-id="1bc2a-120">Location</span></span>      | <span data-ttu-id="1bc2a-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="1bc2a-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="1bc2a-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="1bc2a-122">GitHub</span></span>        | [<span data-ttu-id="1bc2a-123">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="1bc2a-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="1bc2a-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="1bc2a-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1bc2a-125">Building the Sample</span></span>

1. <span data-ttu-id="1bc2a-126">Abra o Windows Explorer e navegue até o diretório do projeto **StructuredQuerySample** .</span><span class="sxs-lookup"><span data-stu-id="1bc2a-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="1bc2a-127">Clique duas vezes no ícone do arquivo StructuredQuerySample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="1bc2a-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="1bc2a-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="1bc2a-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1bc2a-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1bc2a-131">Running the Sample</span></span>

1. <span data-ttu-id="1bc2a-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="1bc2a-133">No prompt de comando, digite `StructuredQuerySample.exe` ou, no Windows Explorer, clique duas vezes no ícone para StructuredQuerySample.exe.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bc2a-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bc2a-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="1bc2a-135">Referência</span><span class="sxs-lookup"><span data-stu-id="1bc2a-135">Reference</span></span>

[<span data-ttu-id="1bc2a-136">**ICondition**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="1bc2a-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="1bc2a-138">**IConditionFactory**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="1bc2a-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="1bc2a-140">**IConditionGenerator**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="1bc2a-141">**IQueryParser**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="1bc2a-142">**IQueryParserManager**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="1bc2a-143">**IQuerySolution**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="1bc2a-144">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="1bc2a-144">Other Samples</span></span>

[<span data-ttu-id="1bc2a-145">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1bc2a-145">Search Code Samples</span></span>](-search-samples-ovw.md)
