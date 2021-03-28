---
description: Demonstra como implementar um verbo do shell usando o método DropTarget.
title: Exemplo de verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967996"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="cf255-103">Exemplo de verbo DropTarget</span><span class="sxs-lookup"><span data-stu-id="cf255-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="cf255-104">Demonstra como implementar um verbo do shell usando o método DropTarget.</span><span class="sxs-lookup"><span data-stu-id="cf255-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="cf255-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf255-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cf255-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf255-106">Description</span></span>](#description)
-   [<span data-ttu-id="cf255-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf255-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cf255-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="cf255-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="cf255-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="cf255-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="cf255-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="cf255-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="cf255-111">Description</span><span class="sxs-lookup"><span data-stu-id="cf255-111">Description</span></span>

<span data-ttu-id="cf255-112">Este exemplo mostra como implementar um verbo do shell usando o método DropTarget.</span><span class="sxs-lookup"><span data-stu-id="cf255-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="cf255-113">Esse método é preferido para implementações de verbo que devem funcionar no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf255-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="cf255-114">Este exemplo implementa um objeto COM (servidor local Component Object Model) autônomo, mas espera-se que a implementação do verbo seja integrada aos aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="cf255-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="cf255-115">Para fazer isso, o objeto de aplicativo principal registra uma fábrica de classes para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="cf255-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="cf255-116">Esse objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para verbos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cf255-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="cf255-117">Observe que COM inicia seu aplicativo se ele ainda não estiver em execução, mas se conectará a uma instância em execução do seu aplicativo, se houver um.</span><span class="sxs-lookup"><span data-stu-id="cf255-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf255-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf255-118">Requirements</span></span>



| <span data-ttu-id="cf255-119">Produto</span><span class="sxs-lookup"><span data-stu-id="cf255-119">Product</span></span>                                | <span data-ttu-id="cf255-120">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="cf255-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="cf255-121">Windows</span><span class="sxs-lookup"><span data-stu-id="cf255-121">Windows</span></span>                                | <span data-ttu-id="cf255-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf255-122">Windows Vista</span></span>           |
| <span data-ttu-id="cf255-123">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="cf255-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="cf255-124">7.0</span><span class="sxs-lookup"><span data-stu-id="cf255-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="cf255-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="cf255-125">Downloading the Sample</span></span>

| <span data-ttu-id="cf255-126">Localização</span><span class="sxs-lookup"><span data-stu-id="cf255-126">Location</span></span>      | <span data-ttu-id="cf255-127">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="cf255-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf255-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="cf255-128">GitHub</span></span>  | [<span data-ttu-id="cf255-129">Exemplo de DropTargetVerb</span><span class="sxs-lookup"><span data-stu-id="cf255-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="cf255-130">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="cf255-130">Building the Sample</span></span>

<span data-ttu-id="cf255-131">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="cf255-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="cf255-132">Abra a janela do prompt de comando e navegue até o diretório do projeto **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="cf255-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="cf255-133">Digite `msbuild DropTargetVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="cf255-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="cf255-134">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="cf255-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="cf255-135">Abra o Windows Explorer e navegue até o diretório do projeto **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="cf255-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="cf255-136">Clique duas vezes no ícone do arquivo DropTargetVerb. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cf255-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="cf255-137">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="cf255-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cf255-138">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="cf255-138">Running the Sample</span></span>

1.  <span data-ttu-id="cf255-139">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="cf255-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="cf255-140">Na linha de comando, digite `DropTargetVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="cf255-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="cf255-141">Como alternativa, no Windows Explorer, clique duas vezes no ícone para DropTargetVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="cf255-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="cf255-142">Siga as instruções na caixa de diálogo exibida</span><span class="sxs-lookup"><span data-stu-id="cf255-142">Follow the instructions in the displayed dialog</span></span>

 

 
