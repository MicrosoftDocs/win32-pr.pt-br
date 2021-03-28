---
description: Demonstra como implementar um verbo do shell usando o método CreateProcess.
title: Exemplo de verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968095"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="10b44-103">Exemplo de verbo CreateProcess</span><span class="sxs-lookup"><span data-stu-id="10b44-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="10b44-104">Demonstra como implementar um verbo do shell usando o método CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="10b44-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="10b44-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="10b44-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="10b44-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="10b44-106">Description</span></span>](#description)
-   [<span data-ttu-id="10b44-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b44-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="10b44-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="10b44-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="10b44-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="10b44-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="10b44-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="10b44-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="10b44-111">Description</span><span class="sxs-lookup"><span data-stu-id="10b44-111">Description</span></span>

<span data-ttu-id="10b44-112">Os verbos baseados em CreateProcess dependem da execução de um executável e da passagem de um argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="10b44-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="10b44-113">Esse método não é tão potente quanto os métodos DropTarget e ExecuteCommand, mas alcança o comportamento de fora do processo desejado.</span><span class="sxs-lookup"><span data-stu-id="10b44-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b44-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b44-114">Requirements</span></span>



| <span data-ttu-id="10b44-115">Produto</span><span class="sxs-lookup"><span data-stu-id="10b44-115">Product</span></span>                                | <span data-ttu-id="10b44-116">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="10b44-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="10b44-117">Windows</span><span class="sxs-lookup"><span data-stu-id="10b44-117">Windows</span></span>                                | <span data-ttu-id="10b44-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10b44-118">Windows Vista</span></span>           |
| <span data-ttu-id="10b44-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="10b44-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="10b44-120">7.0</span><span class="sxs-lookup"><span data-stu-id="10b44-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="10b44-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="10b44-121">Downloading the Sample</span></span>

| <span data-ttu-id="10b44-122">Localização</span><span class="sxs-lookup"><span data-stu-id="10b44-122">Location</span></span>      | <span data-ttu-id="10b44-123">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="10b44-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b44-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="10b44-124">GitHub</span></span>  | [<span data-ttu-id="10b44-125">Exemplo de CreateProcessVerb</span><span class="sxs-lookup"><span data-stu-id="10b44-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="10b44-126">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="10b44-126">Building the Sample</span></span>

<span data-ttu-id="10b44-127">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="10b44-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="10b44-128">Abra a janela do prompt de comando e navegue até o diretório do projeto **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="10b44-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="10b44-129">Digite `msbuild CreateProcessVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="10b44-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="10b44-130">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="10b44-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="10b44-131">Abra o Windows Explorer e navegue até o diretório do projeto **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="10b44-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="10b44-132">Clique duas vezes no ícone do arquivo CreateProcessVerb. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="10b44-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="10b44-133">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="10b44-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="10b44-134">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="10b44-134">Running the Sample</span></span>

1.  <span data-ttu-id="10b44-135">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="10b44-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="10b44-136">Na linha de comando, digite `CreateProcessVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="10b44-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="10b44-137">Como alternativa, no Windows Explorer, clique duas vezes no ícone para CreateProcessVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="10b44-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="10b44-138">Siga as instruções na caixa de diálogo exibida</span><span class="sxs-lookup"><span data-stu-id="10b44-138">Follow the instructions in the displayed dialog</span></span>

 

 



