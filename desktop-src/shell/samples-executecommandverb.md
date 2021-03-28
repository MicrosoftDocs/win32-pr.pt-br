---
description: Demonstra como implementar um verbo do shell usando o método ExecuteCommand.
title: Exemplo do verbo de comando executar
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172197"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="eed46-103">Exemplo do verbo de comando executar</span><span class="sxs-lookup"><span data-stu-id="eed46-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="eed46-104">Demonstra como implementar um verbo do shell usando o método ExecuteCommand.</span><span class="sxs-lookup"><span data-stu-id="eed46-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="eed46-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="eed46-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eed46-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="eed46-106">Description</span></span>](#description)
-   [<span data-ttu-id="eed46-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed46-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="eed46-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="eed46-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="eed46-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="eed46-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="eed46-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="eed46-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="eed46-111">Description</span><span class="sxs-lookup"><span data-stu-id="eed46-111">Description</span></span>

<span data-ttu-id="eed46-112">Esse método é preferido para implementações de verbo, pois fornece mais flexibilidade, é simples e dá suporte à ativação fora do processo.</span><span class="sxs-lookup"><span data-stu-id="eed46-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="eed46-113">Este exemplo implementa um objeto COM (servidor local Component Object Model) autônomo, mas é esperado que a implementação do verbo seja integrada aos aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="eed46-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="eed46-114">Para fazer isso, seu objeto de aplicativo principal deve registrar uma fábrica de classes para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="eed46-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="eed46-115">Esse objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para verbos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eed46-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="eed46-116">Observe que COM inicia seu aplicativo se ele ainda não estiver em execução, mas se conectará a uma instância em execução do seu aplicativo, se houver um.</span><span class="sxs-lookup"><span data-stu-id="eed46-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed46-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed46-117">Requirements</span></span>



| <span data-ttu-id="eed46-118">Produto</span><span class="sxs-lookup"><span data-stu-id="eed46-118">Product</span></span>                                | <span data-ttu-id="eed46-119">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="eed46-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="eed46-120">Windows</span><span class="sxs-lookup"><span data-stu-id="eed46-120">Windows</span></span>                                | <span data-ttu-id="eed46-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eed46-121">Windows 7</span></span>               |
| <span data-ttu-id="eed46-122">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="eed46-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="eed46-123">7.0</span><span class="sxs-lookup"><span data-stu-id="eed46-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="eed46-124">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="eed46-124">Downloading the Sample</span></span>

| <span data-ttu-id="eed46-125">Localização</span><span class="sxs-lookup"><span data-stu-id="eed46-125">Location</span></span>      | <span data-ttu-id="eed46-126">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="eed46-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed46-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="eed46-127">GitHub</span></span>  | [<span data-ttu-id="eed46-128">Exemplo de ExecuteCommandVerb</span><span class="sxs-lookup"><span data-stu-id="eed46-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="eed46-129">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="eed46-129">Building the Sample</span></span>

<span data-ttu-id="eed46-130">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="eed46-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="eed46-131">Abra a janela do prompt de comando e navegue até o diretório do projeto **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="eed46-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="eed46-132">Digite `msbuild ExecuteCommand.sln`.</span><span class="sxs-lookup"><span data-stu-id="eed46-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="eed46-133">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="eed46-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="eed46-134">Abra o Windows Explorer e navegue até o diretório do projeto **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="eed46-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="eed46-135">Clique duas vezes no ícone do arquivo ExecuteCommand. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="eed46-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="eed46-136">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="eed46-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="eed46-137">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="eed46-137">Running the Sample</span></span>

1.  <span data-ttu-id="eed46-138">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="eed46-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="eed46-139">Na linha de comando, digite `ExecuteCommand.exe` .</span><span class="sxs-lookup"><span data-stu-id="eed46-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="eed46-140">Como alternativa, no Windows Explorer, clique duas vezes no ícone para ExecuteCommand.exe.</span><span class="sxs-lookup"><span data-stu-id="eed46-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="eed46-141">Siga as instruções na caixa de diálogo exibida</span><span class="sxs-lookup"><span data-stu-id="eed46-141">Follow the instructions in the displayed dialog</span></span>

 

 
