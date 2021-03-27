---
description: Demonstra como criar um verbo que opera em itens de shell e contêineres que reproduz itens ou adiciona itens a uma fila.
title: Exemplo de verbo do player
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169908"
---
# <a name="player-verb-sample"></a><span data-ttu-id="74b6b-103">Exemplo de verbo do player</span><span class="sxs-lookup"><span data-stu-id="74b6b-103">Player Verb Sample</span></span>

<span data-ttu-id="74b6b-104">Demonstra como criar um verbo que opera em itens de shell e contêineres que reproduz itens ou adiciona itens a uma fila.</span><span class="sxs-lookup"><span data-stu-id="74b6b-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="74b6b-105">Este exemplo é particularmente útil para aplicativos de mídia.</span><span class="sxs-lookup"><span data-stu-id="74b6b-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="74b6b-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="74b6b-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="74b6b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b6b-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="74b6b-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="74b6b-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="74b6b-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="74b6b-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="74b6b-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="74b6b-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="74b6b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b6b-111">Requirements</span></span>



| <span data-ttu-id="74b6b-112">Produto</span><span class="sxs-lookup"><span data-stu-id="74b6b-112">Product</span></span>                                | <span data-ttu-id="74b6b-113">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="74b6b-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="74b6b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="74b6b-114">Windows</span></span>                                | <span data-ttu-id="74b6b-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74b6b-115">Windows Vista</span></span>           |
| <span data-ttu-id="74b6b-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="74b6b-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="74b6b-117">7.0</span><span class="sxs-lookup"><span data-stu-id="74b6b-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="74b6b-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="74b6b-118">Downloading the Sample</span></span>

| <span data-ttu-id="74b6b-119">Localização</span><span class="sxs-lookup"><span data-stu-id="74b6b-119">Location</span></span>      | <span data-ttu-id="74b6b-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="74b6b-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b6b-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="74b6b-121">GitHub</span></span>  | [<span data-ttu-id="74b6b-122">Exemplo de PlayerVerb</span><span class="sxs-lookup"><span data-stu-id="74b6b-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="74b6b-123">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="74b6b-123">Building the Sample</span></span>

<span data-ttu-id="74b6b-124">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="74b6b-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="74b6b-125">Abra a janela do prompt de comando e navegue até o diretório do projeto **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="74b6b-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="74b6b-126">Digite `msbuild PlayerVerbSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="74b6b-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="74b6b-127">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="74b6b-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="74b6b-128">Abra o Windows Explorer e navegue até o diretório do projeto **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="74b6b-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="74b6b-129">Clique duas vezes no ícone do arquivo PlayerVerbSample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="74b6b-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="74b6b-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="74b6b-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="74b6b-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="74b6b-131">Running the Sample</span></span>

1.  <span data-ttu-id="74b6b-132">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="74b6b-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="74b6b-133">Na linha de comando, digite `PlayerVerbSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="74b6b-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="74b6b-134">Como alternativa, no Windows Explorer, clique duas vezes no ícone para PlayerVerbSample.exe.</span><span class="sxs-lookup"><span data-stu-id="74b6b-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="74b6b-135">Selecione `Register Verbs` na caixa de diálogo **exemplo de verbo do Player** .</span><span class="sxs-lookup"><span data-stu-id="74b6b-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="74b6b-136">Clique com o botão direito do mouse em itens de imagem (arquivo, pasta ou pilha) no Windows Explorer para adicioná-los a uma fila ou reproduzi-los no aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="74b6b-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="74b6b-137">Use itens de música quando alterar o exemplo para trabalhar com música.</span><span class="sxs-lookup"><span data-stu-id="74b6b-137">Use music items when you change the sample to work with music.</span></span>

 

 



