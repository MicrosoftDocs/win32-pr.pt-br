---
description: Demonstra como implementar um verbo do shell usando os métodos ExplorerCommand e ExplorerCommandState.
title: Exemplo de verbo de comando do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837032"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="d9408-103">Exemplo de verbo de comando do Explorer</span><span class="sxs-lookup"><span data-stu-id="d9408-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="d9408-104">Demonstra como implementar um verbo do shell usando os métodos ExplorerCommand e ExplorerCommandState.</span><span class="sxs-lookup"><span data-stu-id="d9408-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="d9408-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9408-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d9408-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9408-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d9408-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9408-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d9408-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9408-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d9408-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9408-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="d9408-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9408-110">Requirements</span></span>



| <span data-ttu-id="d9408-111">Produto</span><span class="sxs-lookup"><span data-stu-id="d9408-111">Product</span></span>                                | <span data-ttu-id="d9408-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="d9408-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d9408-113">Windows</span><span class="sxs-lookup"><span data-stu-id="d9408-113">Windows</span></span>                                | <span data-ttu-id="d9408-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9408-114">Windows Vista</span></span>           |
| <span data-ttu-id="d9408-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="d9408-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d9408-116">7.0</span><span class="sxs-lookup"><span data-stu-id="d9408-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d9408-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9408-117">Downloading the Sample</span></span>

| <span data-ttu-id="d9408-118">Localização</span><span class="sxs-lookup"><span data-stu-id="d9408-118">Location</span></span>      | <span data-ttu-id="d9408-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="d9408-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9408-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="d9408-120">GitHub</span></span>  | [<span data-ttu-id="d9408-121">Exemplo de ExplorerCommandVerb</span><span class="sxs-lookup"><span data-stu-id="d9408-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="d9408-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9408-122">Building the Sample</span></span>

<span data-ttu-id="d9408-123">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="d9408-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d9408-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="d9408-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="d9408-125">Digite `msbuild ExplorerCommandVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="d9408-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="d9408-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="d9408-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="d9408-127">Abra o Windows Explorer e navegue até o diretório do projeto **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="d9408-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="d9408-128">Clique duas vezes no ícone do arquivo ExplorerCommandVerb. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d9408-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d9408-129">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="d9408-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d9408-130">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="d9408-130">Running the Sample</span></span>

1.  <span data-ttu-id="d9408-131">Navegue até o diretório que contém o ExplorerCommandVerb.dll, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d9408-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="d9408-132">Certifique-se de usar o arquivo DLL de 64 bits no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d9408-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="d9408-133">Na linha de comando, digite `regsvr32.exe ExplorerCommandVerb.dll` .</span><span class="sxs-lookup"><span data-stu-id="d9408-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="d9408-134">Dois novos verbos serão mostrados no menu de contexto quando você clicar com o botão direito do mouse em um arquivo. txt.</span><span class="sxs-lookup"><span data-stu-id="d9408-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 



