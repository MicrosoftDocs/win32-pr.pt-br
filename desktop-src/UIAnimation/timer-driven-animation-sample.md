---
title: Exemplo de animação de Timer-Driven
description: Mostra como usar a animação do Windows com o temporizador de animação, ao usar o GDI+ para animar a cor do plano de fundo de uma janela.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104293876"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="20497-103">Exemplo de animação de Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="20497-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="20497-104">Mostra como usar a animação do Windows com o temporizador de animação, ao usar o GDI+ para animar a cor do plano de fundo de uma janela.</span><span class="sxs-lookup"><span data-stu-id="20497-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="20497-105">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="20497-105">Downloading the Sample</span></span>

<span data-ttu-id="20497-106">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="20497-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="20497-107">Local</span><span class="sxs-lookup"><span data-stu-id="20497-107">Location</span></span>                               | <span data-ttu-id="20497-108">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="20497-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20497-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="20497-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="20497-110">Kit de desenvolvimento de software do Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="20497-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="20497-111">Galeria de código</span><span class="sxs-lookup"><span data-stu-id="20497-111">Code Gallery</span></span>                           | [<span data-ttu-id="20497-112">Código de exemplo do Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="20497-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="20497-113">Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="20497-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="20497-114">Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para o Windows 7, os exemplos serão instalados em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos.</span><span class="sxs-lookup"><span data-stu-id="20497-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="20497-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="20497-115">Building the Sample</span></span>

<span data-ttu-id="20497-116">Use um dos métodos a seguir para criar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="20497-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="20497-117">**Para criar o exemplo no prompt de comando**</span><span class="sxs-lookup"><span data-stu-id="20497-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="20497-118">Abra a janela do prompt de comando e navegue até o diretório do projeto TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="20497-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="20497-119">Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="20497-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="20497-120">Execute o seguinte comando: **MSBuild TimerDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="20497-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="20497-121">**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**</span><span class="sxs-lookup"><span data-stu-id="20497-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="20497-122">Abra o Windows Explorer e navegue até o diretório do projeto TimerDriven.</span><span class="sxs-lookup"><span data-stu-id="20497-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="20497-123">Clique duas vezes no ícone do arquivo TimerDriven. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="20497-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="20497-124">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="20497-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="20497-125">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="20497-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="20497-126">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="20497-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="20497-127">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="20497-127">Running the Sample</span></span>

<span data-ttu-id="20497-128">Para executar o exemplo:</span><span class="sxs-lookup"><span data-stu-id="20497-128">To run the sample:</span></span>

1.  <span data-ttu-id="20497-129">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="20497-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="20497-130">Execute **TimerDriven.exe** no prompt de comando ou clique duas vezes no ícone para TimerDriven.exe no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="20497-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="20497-131">Clique em qualquer lugar na área do cliente e a cor do plano de fundo da janela será alterada para uma cor aleatória.</span><span class="sxs-lookup"><span data-stu-id="20497-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




