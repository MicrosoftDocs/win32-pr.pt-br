---
title: Exemplo de animação de Application-Driven
description: Mostra a animação do Windows na configuração controlada por aplicativo usando Direct2D para animar a cor do plano de fundo de uma janela e sincronizar com a taxa de atualização.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "105810423"
---
# <a name="application-driven-animation-sample"></a><span data-ttu-id="061c4-103">Exemplo de animação de Application-Driven</span><span class="sxs-lookup"><span data-stu-id="061c4-103">Application-Driven Animation Sample</span></span>

<span data-ttu-id="061c4-104">Mostra a animação do Windows na configuração controlada por aplicativo usando Direct2D para animar a cor do plano de fundo de uma janela e sincronizar com a taxa de atualização.</span><span class="sxs-lookup"><span data-stu-id="061c4-104">Shows Windows Animation in the application-driven configuration by using Direct2D to animate the background color of a window and syncing to the refresh rate.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="061c4-105">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="061c4-105">Downloading the Sample</span></span>

<span data-ttu-id="061c4-106">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="061c4-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="061c4-107">Local</span><span class="sxs-lookup"><span data-stu-id="061c4-107">Location</span></span>                               | <span data-ttu-id="061c4-108">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="061c4-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061c4-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="061c4-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="061c4-110">Kit de desenvolvimento de software do Microsoft Windows 7,0</span><span class="sxs-lookup"><span data-stu-id="061c4-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="061c4-111">Galeria de código</span><span class="sxs-lookup"><span data-stu-id="061c4-111">Code Gallery</span></span>                           | [<span data-ttu-id="061c4-112">Código de exemplo do Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="061c4-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="061c4-113">Depois de baixar e instalar o SDK do Windows, você encontrará os exemplos no diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="061c4-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="061c4-114">Por exemplo, se você usar o caminho de instalação padrão para o SDK do Windows para o Windows 7, os exemplos serão instalados em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos.</span><span class="sxs-lookup"><span data-stu-id="061c4-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="061c4-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="061c4-115">Building the Sample</span></span>

<span data-ttu-id="061c4-116">Use um dos métodos a seguir para criar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="061c4-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="061c4-117">**Para criar o exemplo no prompt de comando**</span><span class="sxs-lookup"><span data-stu-id="061c4-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="061c4-118">Abra a janela do prompt de comando e navegue até o diretório do projeto AppDriven.</span><span class="sxs-lookup"><span data-stu-id="061c4-118">Open the Command Prompt window and navigate to the AppDriven project directory.</span></span> <span data-ttu-id="061c4-119">Por exemplo, o caminho de instalação padrão para este exemplo é C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ exemplos \\ multimídia \\ WindowsAnimation \\ AppDriven.</span><span class="sxs-lookup"><span data-stu-id="061c4-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\AppDriven.</span></span>

2.  <span data-ttu-id="061c4-120">Execute o seguinte comando: **MSBuild AppDriven. sln**</span><span class="sxs-lookup"><span data-stu-id="061c4-120">Run the following command: **msbuild AppDriven.sln**</span></span>

<span data-ttu-id="061c4-121">**Para criar o exemplo usando Microsoft Visual Studio (preferencial)**</span><span class="sxs-lookup"><span data-stu-id="061c4-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="061c4-122">Abra o Windows Explorer e navegue até o diretório do projeto AppDriven.</span><span class="sxs-lookup"><span data-stu-id="061c4-122">Open Windows Explorer and navigate to the AppDriven project directory.</span></span>

2.  <span data-ttu-id="061c4-123">Clique duas vezes no ícone do arquivo AppDriven. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="061c4-123">Double-click the icon for the AppDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="061c4-124">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="061c4-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="061c4-125">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="061c4-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="061c4-126">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="061c4-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="061c4-127">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="061c4-127">Running the Sample</span></span>

<span data-ttu-id="061c4-128">Para executar o exemplo:</span><span class="sxs-lookup"><span data-stu-id="061c4-128">To run the sample:</span></span>

1.  <span data-ttu-id="061c4-129">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="061c4-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="061c4-130">Execute **AppDriven.exe** no prompt de comando ou clique duas vezes no ícone para AppDriven.exe no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="061c4-130">Run **AppDriven.exe** at the command prompt, or double-click the icon for AppDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="061c4-131">Clique em qualquer lugar na área do cliente e a cor do plano de fundo da janela será alterada para uma cor aleatória.</span><span class="sxs-lookup"><span data-stu-id="061c4-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




