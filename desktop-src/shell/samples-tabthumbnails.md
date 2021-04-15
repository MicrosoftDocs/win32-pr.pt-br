---
description: Demonstra como um aplicativo pode expor vários destinos de comutador (como para guias) em um Taskband e como fornecer suas miniaturas.
title: Exemplo de TabThumbnails
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968199"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="41dd9-103">Exemplo de TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="41dd9-103">TabThumbnails Sample</span></span>

<span data-ttu-id="41dd9-104">Demonstra como um aplicativo pode expor vários destinos de comutador (como para guias) em um Taskband e como fornecer suas miniaturas.</span><span class="sxs-lookup"><span data-stu-id="41dd9-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="41dd9-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="41dd9-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="41dd9-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41dd9-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="41dd9-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="41dd9-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="41dd9-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="41dd9-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="41dd9-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="41dd9-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="41dd9-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41dd9-110">Requirements</span></span>



| <span data-ttu-id="41dd9-111">Produto</span><span class="sxs-lookup"><span data-stu-id="41dd9-111">Product</span></span>                                | <span data-ttu-id="41dd9-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="41dd9-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="41dd9-113">Windows</span><span class="sxs-lookup"><span data-stu-id="41dd9-113">Windows</span></span>                                | <span data-ttu-id="41dd9-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="41dd9-114">Windows 7</span></span>               |
| <span data-ttu-id="41dd9-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="41dd9-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="41dd9-116">7.0</span><span class="sxs-lookup"><span data-stu-id="41dd9-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="41dd9-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="41dd9-117">Downloading the Sample</span></span>

| <span data-ttu-id="41dd9-118">Localização</span><span class="sxs-lookup"><span data-stu-id="41dd9-118">Location</span></span>      | <span data-ttu-id="41dd9-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="41dd9-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41dd9-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="41dd9-120">GitHub</span></span>  | [<span data-ttu-id="41dd9-121">Exemplo de TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="41dd9-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="41dd9-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="41dd9-122">Building the Sample</span></span>

<span data-ttu-id="41dd9-123">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="41dd9-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="41dd9-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="41dd9-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="41dd9-125">Digite `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="41dd9-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="41dd9-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="41dd9-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="41dd9-127">Abra o Windows Explorer e navegue até o diretório do projeto **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="41dd9-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="41dd9-128">Clique duas vezes no ícone do arquivo TabThumbnails. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="41dd9-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="41dd9-129">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="41dd9-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="41dd9-130">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="41dd9-130">Running the Sample</span></span>

1.  <span data-ttu-id="41dd9-131">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="41dd9-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="41dd9-132">Na linha de comando, digite `TabThumbnails.exe` .</span><span class="sxs-lookup"><span data-stu-id="41dd9-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="41dd9-133">Como alternativa, no Windows Explorer, clique duas vezes no ícone para TabThumbnails.exe.</span><span class="sxs-lookup"><span data-stu-id="41dd9-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 



