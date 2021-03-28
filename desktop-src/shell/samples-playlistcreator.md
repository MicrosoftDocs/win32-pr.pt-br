---
description: Demonstra como criar um verbo que opera em um contêiner ou item de shell selecionado para criar uma lista de reprodução.
title: Exemplo de criador de playlist
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968243"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="7ea62-103">Exemplo de criador de playlist</span><span class="sxs-lookup"><span data-stu-id="7ea62-103">Playlist Creator Sample</span></span>

<span data-ttu-id="7ea62-104">Demonstra como criar um verbo que opera em um contêiner ou item de shell selecionado para criar uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7ea62-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="7ea62-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ea62-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7ea62-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ea62-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7ea62-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea62-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7ea62-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea62-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7ea62-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea62-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="7ea62-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ea62-110">Requirements</span></span>



| <span data-ttu-id="7ea62-111">Produto</span><span class="sxs-lookup"><span data-stu-id="7ea62-111">Product</span></span>                                | <span data-ttu-id="7ea62-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="7ea62-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="7ea62-113">Windows</span><span class="sxs-lookup"><span data-stu-id="7ea62-113">Windows</span></span>                                | <span data-ttu-id="7ea62-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ea62-114">Windows Vista</span></span>           |
| <span data-ttu-id="7ea62-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="7ea62-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="7ea62-116">7.0</span><span class="sxs-lookup"><span data-stu-id="7ea62-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7ea62-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea62-117">Downloading the Sample</span></span>

| <span data-ttu-id="7ea62-118">Localização</span><span class="sxs-lookup"><span data-stu-id="7ea62-118">Location</span></span>      | <span data-ttu-id="7ea62-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="7ea62-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea62-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="7ea62-120">GitHub</span></span>  | [<span data-ttu-id="7ea62-121">Exemplo de PlaylistCreator</span><span class="sxs-lookup"><span data-stu-id="7ea62-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="7ea62-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea62-122">Building the Sample</span></span>

<span data-ttu-id="7ea62-123">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="7ea62-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="7ea62-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="7ea62-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="7ea62-125">Digite `msbuild PlaylistCreator.sln`.</span><span class="sxs-lookup"><span data-stu-id="7ea62-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="7ea62-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="7ea62-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="7ea62-127">Esse exemplo também pode ser usado com o Visual C++ Express Edition se o Visual Studio completo não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="7ea62-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="7ea62-128">Abra o Windows Explorer e navegue até o diretório do projeto **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="7ea62-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="7ea62-129">Clique duas vezes no ícone do arquivo PlaylistCreator. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7ea62-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="7ea62-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="7ea62-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="7ea62-131">Se você estiver compilando 64 bits usando o Visual C++ Express Edition, deverá usar o compilador cruzado x64 fornecido com o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7ea62-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="7ea62-132">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7ea62-132">Running the Sample</span></span>

1.  <span data-ttu-id="7ea62-133">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="7ea62-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="7ea62-134">Na linha de comando, digite `PlaylistCreator.exe` .</span><span class="sxs-lookup"><span data-stu-id="7ea62-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="7ea62-135">Como alternativa, no Windows Explorer, clique duas vezes no ícone para PlaylistCreator.exe.</span><span class="sxs-lookup"><span data-stu-id="7ea62-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="7ea62-136">Clique com o botão direito do mouse em qualquer arquivo ou pasta de música que contenha arquivos de música no Windows Explorer para criar uma lista de reprodução para abrir o menu de contexto</span><span class="sxs-lookup"><span data-stu-id="7ea62-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="7ea62-137">Você pode criar uma lista de reprodução. m3u ou. wpl.</span><span class="sxs-lookup"><span data-stu-id="7ea62-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="7ea62-138">As listas de reprodução são criadas na `%userprofile%\Music\Playlists` pasta.</span><span class="sxs-lookup"><span data-stu-id="7ea62-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="7ea62-139">Novos verbos no menu de contexto podem ser encontrados na pasta **música** , pilhas de músicas, pilhas na **biblioteca de músicas** e coleções de arquivos de música.</span><span class="sxs-lookup"><span data-stu-id="7ea62-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 



