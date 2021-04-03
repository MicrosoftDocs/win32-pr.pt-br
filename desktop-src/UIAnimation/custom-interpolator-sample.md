---
title: Exemplo de interpolador personalizado
description: Mostra como usar a animação do Windows com seu próprio interpolador personalizado, com Direct2D usado para renderização.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104084420"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="585fa-103">Exemplo de interpolador personalizado</span><span class="sxs-lookup"><span data-stu-id="585fa-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="585fa-104">Mostra como usar a animação do Windows com seu próprio interpolador personalizado, com Direct2D usado para renderização.</span><span class="sxs-lookup"><span data-stu-id="585fa-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="585fa-105">As imagens de exemplo são carregadas da biblioteca de imagens.</span><span class="sxs-lookup"><span data-stu-id="585fa-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="585fa-106">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="585fa-106">Downloading the Sample</span></span>

<span data-ttu-id="585fa-107">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="585fa-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="585fa-108">Local</span><span class="sxs-lookup"><span data-stu-id="585fa-108">Location</span></span>                               | <span data-ttu-id="585fa-109">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="585fa-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="585fa-110">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="585fa-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="585fa-111">Kit de desenvolvimento de software do Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="585fa-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="585fa-112">Galeria de código</span><span class="sxs-lookup"><span data-stu-id="585fa-112">Code Gallery</span></span>                           | [<span data-ttu-id="585fa-113">Código de exemplo do Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="585fa-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="585fa-114">Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="585fa-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="585fa-115">Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para o Windows 7, os exemplos serão instalados em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos.</span><span class="sxs-lookup"><span data-stu-id="585fa-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="585fa-116">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="585fa-116">Building the Sample</span></span>

<span data-ttu-id="585fa-117">Use um dos métodos a seguir para criar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="585fa-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="585fa-118">**Para criar o exemplo no prompt de comando**</span><span class="sxs-lookup"><span data-stu-id="585fa-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="585fa-119">Abra a janela do prompt de comando e navegue até o diretório do projeto CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="585fa-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="585fa-120">Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ CustomInterpolator</span><span class="sxs-lookup"><span data-stu-id="585fa-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="585fa-121">Execute o seguinte comando: **MSBuild CustomInterpolator. sln**</span><span class="sxs-lookup"><span data-stu-id="585fa-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="585fa-122">**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**</span><span class="sxs-lookup"><span data-stu-id="585fa-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="585fa-123">Abra o Windows Explorer e navegue até o diretório do projeto CustomInterpolator.</span><span class="sxs-lookup"><span data-stu-id="585fa-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="585fa-124">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="585fa-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="585fa-125">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="585fa-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="585fa-126">Clique duas vezes no ícone do arquivo CustomInterpolator. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="585fa-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="585fa-127">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="585fa-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="585fa-128">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="585fa-128">Running the Sample</span></span>

<span data-ttu-id="585fa-129">Para executar o exemplo:</span><span class="sxs-lookup"><span data-stu-id="585fa-129">To run the sample:</span></span>

1.  <span data-ttu-id="585fa-130">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="585fa-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="585fa-131">Execute **CustomInterpolator.exe** no prompt de comando ou clique duas vezes no ícone para CustomInterpolator.exe no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="585fa-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="585fa-132">Redimensione a janela ou pressione a barra de espaços e as imagens serão organizadas aleatoriamente no meio da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="585fa-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="585fa-133">Pressione a seta para cima ou para baixo e as imagens serão aceleradas em direção à parte superior ou inferior da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="585fa-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 




