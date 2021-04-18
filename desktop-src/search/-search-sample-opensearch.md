---
description: O exemplo de código OpenSearch demonstra como criar um serviço de pesquisa federado usando o protocolo OpenSearch e um arquivo de descritor de OpenSearch (. osdx) (um conector de pesquisa).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370620"
---
# <a name="opensearch"></a><span data-ttu-id="a1ba1-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="a1ba1-103">OpenSearch</span></span>

<span data-ttu-id="a1ba1-104">O exemplo de código OpenSearch demonstra como criar um serviço de pesquisa federado usando o protocolo [OpenSearch](https://github.com/dewitt/opensearch) e um arquivo de descritor de OpenSearch (. osdx) (um conector de pesquisa).</span><span class="sxs-lookup"><span data-stu-id="a1ba1-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="a1ba1-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a1ba1-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="a1ba1-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a1ba1-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a1ba1-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a1ba1-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a1ba1-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a1ba1-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a1ba1-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="a1ba1-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1ba1-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="a1ba1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1ba1-111">Requirements</span></span>



| <span data-ttu-id="a1ba1-112">Produto</span><span class="sxs-lookup"><span data-stu-id="a1ba1-112">Product</span></span>     | <span data-ttu-id="a1ba1-113">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="a1ba1-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="a1ba1-114">Windows</span><span class="sxs-lookup"><span data-stu-id="a1ba1-114">Windows</span></span>     | <span data-ttu-id="a1ba1-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a1ba1-115">Windows 7</span></span>               |
| <span data-ttu-id="a1ba1-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="a1ba1-116">Windows SDK</span></span> | <span data-ttu-id="a1ba1-117">7.0</span><span class="sxs-lookup"><span data-stu-id="a1ba1-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a1ba1-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a1ba1-118">Downloading the Sample</span></span>

<span data-ttu-id="a1ba1-119">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="a1ba1-120">Local</span><span class="sxs-lookup"><span data-stu-id="a1ba1-120">Location</span></span>      | <span data-ttu-id="a1ba1-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="a1ba1-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a1ba1-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="a1ba1-122">GitHub</span></span>  | [<span data-ttu-id="a1ba1-123">Exemplo de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="a1ba1-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="a1ba1-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="a1ba1-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a1ba1-125">Building the Sample</span></span>

<span data-ttu-id="a1ba1-126">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="a1ba1-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="a1ba1-127">Abra a janela do prompt de comando e navegue até o diretório do projeto **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="a1ba1-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="a1ba1-128">Digite `msbuild AdventureSearch.sln`.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="a1ba1-129">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="a1ba1-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="a1ba1-130">Abra o Windows Explorer e navegue até o diretório do projeto **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="a1ba1-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="a1ba1-131">Clique duas vezes no ícone do arquivo AdventureSearch. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="a1ba1-132">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="a1ba1-133">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="a1ba1-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="a1ba1-134">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a1ba1-135">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a1ba1-135">Running the Sample</span></span>

1.  <span data-ttu-id="a1ba1-136">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="a1ba1-137">No prompt de comando, digite `AdventureSearch.exe` ou, no Windows Explorer, clique duas vezes no ícone para AdventureSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="a1ba1-138">No prompt de comando, digite `GetOSDX.exe` ou, no Windows Explorer, clique duas vezes no ícone para GetOSDX.exe.</span><span class="sxs-lookup"><span data-stu-id="a1ba1-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1ba1-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1ba1-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a1ba1-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a1ba1-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a1ba1-141">Visão geral do esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a1ba1-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="a1ba1-142">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a1ba1-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a1ba1-143">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="a1ba1-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="a1ba1-144">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a1ba1-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="a1ba1-145">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="a1ba1-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a1ba1-146">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1ba1-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 
