---
description: Demonstra como determinar o status de associação do grupo doméstico, enumerar itens de nível superior na pasta do shell do grupo doméstico e iniciar o assistente de compartilhamento do grupo doméstico.
title: Exemplo de HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011184"
---
# <a name="homegroup-sample"></a><span data-ttu-id="26233-103">Exemplo de HomeGroup</span><span class="sxs-lookup"><span data-stu-id="26233-103">HomeGroup Sample</span></span>

<span data-ttu-id="26233-104">Demonstra como determinar o status de associação do grupo doméstico, enumerar itens de nível superior na pasta do shell do **grupo doméstico** e iniciar o **Assistente de compartilhamento do grupo doméstico**.</span><span class="sxs-lookup"><span data-stu-id="26233-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="26233-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="26233-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="26233-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26233-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="26233-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="26233-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="26233-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="26233-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="26233-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="26233-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="26233-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26233-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="26233-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26233-111">Requirements</span></span>



| <span data-ttu-id="26233-112">Produto</span><span class="sxs-lookup"><span data-stu-id="26233-112">Product</span></span>                                | <span data-ttu-id="26233-113">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="26233-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="26233-114">Windows</span><span class="sxs-lookup"><span data-stu-id="26233-114">Windows</span></span>                                | <span data-ttu-id="26233-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26233-115">Windows 7</span></span>               |
| <span data-ttu-id="26233-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="26233-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="26233-117">7.0</span><span class="sxs-lookup"><span data-stu-id="26233-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="26233-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="26233-118">Downloading the Sample</span></span>

| <span data-ttu-id="26233-119">Localização</span><span class="sxs-lookup"><span data-stu-id="26233-119">Location</span></span>      | <span data-ttu-id="26233-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="26233-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26233-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="26233-121">GitHub</span></span>  | [<span data-ttu-id="26233-122">Exemplo de grupo doméstico</span><span class="sxs-lookup"><span data-stu-id="26233-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="26233-123">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="26233-123">Building the Sample</span></span>

<span data-ttu-id="26233-124">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="26233-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="26233-125">Abra a janela do prompt de comando e navegue até o diretório do projeto do **grupo doméstico** .</span><span class="sxs-lookup"><span data-stu-id="26233-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="26233-126">Digite `msbuild HomeGroup.sln`.</span><span class="sxs-lookup"><span data-stu-id="26233-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="26233-127">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="26233-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="26233-128">Abra o Windows Explorer e navegue até o diretório do projeto do **grupo doméstico** .</span><span class="sxs-lookup"><span data-stu-id="26233-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="26233-129">Clique duas vezes no ícone do arquivo. sln do grupo doméstico para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="26233-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="26233-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="26233-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="26233-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="26233-131">Running the Sample</span></span>

1.  <span data-ttu-id="26233-132">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="26233-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="26233-133">Na linha de comando, digite `HomeGroup.exe` .</span><span class="sxs-lookup"><span data-stu-id="26233-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="26233-134">Como alternativa, no Windows Explorer, clique duas vezes no ícone para HomeGroup.exe.</span><span class="sxs-lookup"><span data-stu-id="26233-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26233-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26233-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26233-136">**IHomeGroup**</span><span class="sxs-lookup"><span data-stu-id="26233-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="26233-137">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="26233-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 



