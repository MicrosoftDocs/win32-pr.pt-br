---
description: O exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e o Windows Search por meio de linguagem SQL (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826910"
---
# <a name="wssql"></a><span data-ttu-id="290bf-103">WSSQL</span><span class="sxs-lookup"><span data-stu-id="290bf-103">WSSQL</span></span>

<span data-ttu-id="290bf-104">O exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e o Windows Search por meio de linguagem SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="290bf-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="290bf-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="290bf-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="290bf-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="290bf-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="290bf-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="290bf-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="290bf-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="290bf-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="290bf-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="290bf-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="290bf-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="290bf-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="290bf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="290bf-111">Requirements</span></span>

| <span data-ttu-id="290bf-112">Produto</span><span class="sxs-lookup"><span data-stu-id="290bf-112">Product</span></span>     | <span data-ttu-id="290bf-113">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="290bf-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="290bf-114">Windows</span><span class="sxs-lookup"><span data-stu-id="290bf-114">Windows</span></span>     | <span data-ttu-id="290bf-115">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="290bf-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="290bf-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="290bf-116">Windows SDK</span></span> | <span data-ttu-id="290bf-117">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="290bf-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="290bf-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="290bf-118">Downloading the Sample</span></span>

<span data-ttu-id="290bf-119">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="290bf-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="290bf-120">Local</span><span class="sxs-lookup"><span data-stu-id="290bf-120">Location</span></span>      | <span data-ttu-id="290bf-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="290bf-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="290bf-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="290bf-122">GitHub</span></span>        | [<span data-ttu-id="290bf-123">Exemplo de WSSQL</span><span class="sxs-lookup"><span data-stu-id="290bf-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="290bf-124">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="290bf-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="290bf-125">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="290bf-125">Building the Sample</span></span>

1. <span data-ttu-id="290bf-126">Abra o Windows Explorer e navegue até o diretório do projeto **WSSQL** .</span><span class="sxs-lookup"><span data-stu-id="290bf-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="290bf-127">Clique duas vezes no ícone do arquivo WSSQL. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="290bf-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="290bf-128">O arquivo sln foi criado em uma versão mais antiga do Visual Studio, portanto, a atualização será necessária se você estiver executando o Visual Studio 2012 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="290bf-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="290bf-129">Isso não afetará o comportamento do exemplo.</span><span class="sxs-lookup"><span data-stu-id="290bf-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="290bf-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="290bf-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="290bf-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="290bf-131">Running the Sample</span></span>

1. <span data-ttu-id="290bf-132">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="290bf-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="290bf-133">No prompt de comando, digite `WSSQL.exe` ou, no Windows Explorer, clique duas vezes no ícone para WSSQL.exe.</span><span class="sxs-lookup"><span data-stu-id="290bf-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="290bf-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="290bf-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="290bf-135">Conceitual</span><span class="sxs-lookup"><span data-stu-id="290bf-135">Conceptual</span></span>

[<span data-ttu-id="290bf-136">Usando a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="290bf-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="290bf-137">Informações gerais da linguagem de consulta</span><span class="sxs-lookup"><span data-stu-id="290bf-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="290bf-138">Visão geral da programação de OLE DB</span><span class="sxs-lookup"><span data-stu-id="290bf-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="290bf-139">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="290bf-139">Other Samples</span></span>

[<span data-ttu-id="290bf-140">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="290bf-140">Search Code Samples</span></span>](-search-samples-ovw.md)
