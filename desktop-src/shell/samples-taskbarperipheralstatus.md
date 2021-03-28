---
description: Demonstra sobreposições de ícone da barra de tarefas e barras de progresso.
title: Exemplo de status periférico da barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989074"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="77dd5-103">Exemplo de status periférico da barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="77dd5-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="77dd5-104">Demonstra sobreposições de ícone da barra de tarefas e barras de progresso.</span><span class="sxs-lookup"><span data-stu-id="77dd5-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="77dd5-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="77dd5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="77dd5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="77dd5-106">Description</span></span>](#description)
-   [<span data-ttu-id="77dd5-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77dd5-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="77dd5-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="77dd5-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="77dd5-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="77dd5-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="77dd5-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="77dd5-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="77dd5-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77dd5-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="77dd5-112">Description</span><span class="sxs-lookup"><span data-stu-id="77dd5-112">Description</span></span>

<span data-ttu-id="77dd5-113">Este exemplo cria um botão de barra de tarefas de exemplo no qual ele demonstra o uso de [**ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) permitindo que você aplique várias sobreposições escolhidas em um menu.</span><span class="sxs-lookup"><span data-stu-id="77dd5-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="77dd5-114">O exemplo também fornece a opção de simular um indicador de progresso no botão, demonstrando o uso de [**ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) e [**ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) mostrando a primeira um indicador de progresso indeterminado (TBPF \_ indeterminado) e, em seguida, um indicador proporcional normal (TBPF \_ normal).</span><span class="sxs-lookup"><span data-stu-id="77dd5-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="77dd5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77dd5-115">Requirements</span></span>



| <span data-ttu-id="77dd5-116">Produto</span><span class="sxs-lookup"><span data-stu-id="77dd5-116">Product</span></span>                                | <span data-ttu-id="77dd5-117">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="77dd5-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="77dd5-118">Windows</span><span class="sxs-lookup"><span data-stu-id="77dd5-118">Windows</span></span>                                | <span data-ttu-id="77dd5-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77dd5-119">Windows 7</span></span>               |
| <span data-ttu-id="77dd5-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="77dd5-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="77dd5-121">7.0</span><span class="sxs-lookup"><span data-stu-id="77dd5-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="77dd5-122">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="77dd5-122">Downloading the Sample</span></span>

| <span data-ttu-id="77dd5-123">Localização</span><span class="sxs-lookup"><span data-stu-id="77dd5-123">Location</span></span>      | <span data-ttu-id="77dd5-124">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="77dd5-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dd5-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="77dd5-125">GitHub</span></span>  | [<span data-ttu-id="77dd5-126">Exemplo de TaskBarPeripheralStatus</span><span class="sxs-lookup"><span data-stu-id="77dd5-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="77dd5-127">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="77dd5-127">Building the Sample</span></span>

<span data-ttu-id="77dd5-128">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="77dd5-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="77dd5-129">Abra a janela do prompt de comando e navegue até o diretório do projeto **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="77dd5-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="77dd5-130">Digite `msbuild PeripheralStatus.sln`.</span><span class="sxs-lookup"><span data-stu-id="77dd5-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="77dd5-131">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="77dd5-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="77dd5-132">Abra o Windows Explorer e navegue até o diretório do projeto **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="77dd5-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="77dd5-133">Clique duas vezes no ícone do arquivo PeripheralStatus. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="77dd5-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="77dd5-134">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="77dd5-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="77dd5-135">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="77dd5-135">Running the Sample</span></span>

1.  <span data-ttu-id="77dd5-136">Navegue até o diretório que contém o novo arquivo executável (por exemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="77dd5-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="77dd5-137">Se estiver usando a linha de comando, digite `PeripheralStatus.exe` .</span><span class="sxs-lookup"><span data-stu-id="77dd5-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="77dd5-138">Se estiver usando o Windows Explorer, clique duas vezes no ícone para PeripheralStatus.exe.</span><span class="sxs-lookup"><span data-stu-id="77dd5-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="77dd5-139">Uma nova janela será aberta, com um botão da barra de tarefas associado.</span><span class="sxs-lookup"><span data-stu-id="77dd5-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="77dd5-140">Para demonstrar sobreposições, escolha **sobreposição 1** ou **sobreposição 2** no menu de **status periférico** da janela.</span><span class="sxs-lookup"><span data-stu-id="77dd5-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="77dd5-141">A sobreposição escolhida aparece no botão da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="77dd5-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="77dd5-142">Para remover a sobreposição, escolha **limpar sobreposição**.</span><span class="sxs-lookup"><span data-stu-id="77dd5-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="77dd5-143">Para demonstrar a barra de progresso, escolha **simular progresso** no menu de **status periférico** da janela.</span><span class="sxs-lookup"><span data-stu-id="77dd5-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="77dd5-144">O botão da barra de tarefas mostrará um indicador de progresso indeterminado e alternará para um indicador normal.</span><span class="sxs-lookup"><span data-stu-id="77dd5-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="77dd5-145">Escolha **sair** no menu **arquivo** da janela para encerrar o programa.</span><span class="sxs-lookup"><span data-stu-id="77dd5-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77dd5-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77dd5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77dd5-147">Extensões da barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="77dd5-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



