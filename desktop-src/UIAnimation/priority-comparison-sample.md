---
title: Exemplo de comparação de prioridade
description: Mostra como usar a animação do Windows com sua própria comparação de prioridade, usando Direct2D para renderização.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104084419"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="3ab29-103">Exemplo de comparação de prioridade</span><span class="sxs-lookup"><span data-stu-id="3ab29-103">Priority Comparison Sample</span></span>

<span data-ttu-id="3ab29-104">Mostra como usar a animação do Windows com sua própria comparação de prioridade, usando Direct2D para renderização.</span><span class="sxs-lookup"><span data-stu-id="3ab29-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3ab29-105">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3ab29-105">Downloading the Sample</span></span>

<span data-ttu-id="3ab29-106">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ab29-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="3ab29-107">Local</span><span class="sxs-lookup"><span data-stu-id="3ab29-107">Location</span></span>                               | <span data-ttu-id="3ab29-108">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="3ab29-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab29-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="3ab29-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="3ab29-110">Kit de desenvolvimento de software do Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="3ab29-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="3ab29-111">Galeria de código</span><span class="sxs-lookup"><span data-stu-id="3ab29-111">Code Gallery</span></span>                           | [<span data-ttu-id="3ab29-112">Código de exemplo do Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="3ab29-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="3ab29-113">Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="3ab29-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="3ab29-114">Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para o Windows 7, os exemplos serão instalados em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos.</span><span class="sxs-lookup"><span data-stu-id="3ab29-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="3ab29-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3ab29-115">Building the Sample</span></span>

<span data-ttu-id="3ab29-116">Use um dos métodos a seguir para criar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="3ab29-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="3ab29-117">**Para criar o exemplo no prompt de comando**</span><span class="sxs-lookup"><span data-stu-id="3ab29-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="3ab29-118">Abra a janela do prompt de comando e navegue até o diretório do projeto PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="3ab29-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="3ab29-119">Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="3ab29-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="3ab29-120">Execute o seguinte comando: **MSBuild PriorityComparison. sln**</span><span class="sxs-lookup"><span data-stu-id="3ab29-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="3ab29-121">**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**</span><span class="sxs-lookup"><span data-stu-id="3ab29-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="3ab29-122">Abra o Windows Explorer e navegue até o diretório do projeto PriorityComparison.</span><span class="sxs-lookup"><span data-stu-id="3ab29-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="3ab29-123">Clique duas vezes no ícone do arquivo PriorityComparison. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ab29-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="3ab29-124">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="3ab29-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="3ab29-125">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="3ab29-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="3ab29-126">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="3ab29-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3ab29-127">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3ab29-127">Running the Sample</span></span>

<span data-ttu-id="3ab29-128">Para executar o exemplo:</span><span class="sxs-lookup"><span data-stu-id="3ab29-128">To run the sample:</span></span>

1.  <span data-ttu-id="3ab29-129">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ab29-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="3ab29-130">Execute **PriorityComparison.exe** no prompt de comando ou clique duas vezes no ícone para PriorityComparison.exe no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ab29-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="3ab29-131">As imagens de exemplo são carregadas da biblioteca de imagens.</span><span class="sxs-lookup"><span data-stu-id="3ab29-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="3ab29-132">Redimensione a janela ou pressione a barra de espaços e as imagens serão movidas para o centro.</span><span class="sxs-lookup"><span data-stu-id="3ab29-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="3ab29-133">Use as teclas de seta para a esquerda e para a direita para selecionar imagens diferentes (quanto mais rápida a chave for pressionada, mais rapidamente a seleção será alterada).</span><span class="sxs-lookup"><span data-stu-id="3ab29-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="3ab29-134">Use as teclas de seta para cima e para baixo para criar uma onda por meio das imagens (quanto mais rápida for pressionada, mais rápida será a onda).</span><span class="sxs-lookup"><span data-stu-id="3ab29-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 




