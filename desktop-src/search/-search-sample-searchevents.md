---
description: O exemplo de código SearchEvents demonstra como priorizar eventos de indexação.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788936"
---
# <a name="searchevents"></a><span data-ttu-id="0017b-103">SearchEvents</span><span class="sxs-lookup"><span data-stu-id="0017b-103">SearchEvents</span></span>

<span data-ttu-id="0017b-104">O exemplo de código SearchEvents demonstra como priorizar eventos de indexação.</span><span class="sxs-lookup"><span data-stu-id="0017b-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="0017b-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0017b-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="0017b-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="0017b-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="0017b-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0017b-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="0017b-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0017b-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="0017b-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0017b-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="0017b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0017b-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0017b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0017b-111">Requirements</span></span>

| <span data-ttu-id="0017b-112">Produto</span><span class="sxs-lookup"><span data-stu-id="0017b-112">Product</span></span>     | <span data-ttu-id="0017b-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="0017b-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="0017b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0017b-114">Windows</span></span>     | <span data-ttu-id="0017b-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="0017b-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="0017b-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="0017b-116">Windows SDK</span></span> | <span data-ttu-id="0017b-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="0017b-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="0017b-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0017b-118">Downloading the Sample</span></span>

<span data-ttu-id="0017b-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="0017b-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="0017b-120">Local</span><span class="sxs-lookup"><span data-stu-id="0017b-120">Location</span></span>      | <span data-ttu-id="0017b-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="0017b-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0017b-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="0017b-122">GitHub</span></span>        | [<span data-ttu-id="0017b-123">Exemplo de SearchEvents</span><span class="sxs-lookup"><span data-stu-id="0017b-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="0017b-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="0017b-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="0017b-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0017b-125">Building the Sample</span></span>

1. <span data-ttu-id="0017b-126">Abra o Windows Explorer e navegue até o diretório do projeto **SearchEvents** .</span><span class="sxs-lookup"><span data-stu-id="0017b-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="0017b-127">Clique duas vezes no ícone do arquivo Eventing. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0017b-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="0017b-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="0017b-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="0017b-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="0017b-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="0017b-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="0017b-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0017b-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="0017b-131">Running the Sample</span></span>

1. <span data-ttu-id="0017b-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="0017b-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="0017b-133">No prompt de comando, digite `Eventing.exe` ou, no Windows Explorer, clique duas vezes no ícone para Eventing.exe.</span><span class="sxs-lookup"><span data-stu-id="0017b-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0017b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0017b-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="0017b-135">Referência</span><span class="sxs-lookup"><span data-stu-id="0017b-135">Reference</span></span>

[<span data-ttu-id="0017b-136">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="0017b-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="0017b-137">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="0017b-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="0017b-138">**nível de prioridade \_**</span><span class="sxs-lookup"><span data-stu-id="0017b-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="0017b-139">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="0017b-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="0017b-140">**tipo de ROWSETEVENT \_**</span><span class="sxs-lookup"><span data-stu-id="0017b-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="0017b-141">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="0017b-141">Other Samples</span></span>

[<span data-ttu-id="0017b-142">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0017b-142">Search Code Samples</span></span>](-search-samples-ovw.md)
