---
description: Demonstra uma barra de ferramentas de miniatura, um controle de barra de ferramentas ativo inserido na visualização em miniatura de uma janela, usado para fornecer acesso aos comandos de chave de uma janela sem fazer com que o usuário restaure ou ative a janela do aplicativo.
title: Exemplo da barra de ferramentas em miniatura da barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968093"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="3990f-103">Exemplo da barra de ferramentas em miniatura da barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="3990f-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="3990f-104">Demonstra uma barra de ferramentas de miniatura, um controle de barra de ferramentas ativo inserido na visualização em miniatura de uma janela, usado para fornecer acesso aos comandos de chave de uma janela sem fazer com que o usuário restaure ou ative a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3990f-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="3990f-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="3990f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3990f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3990f-106">Description</span></span>](#description)
-   [<span data-ttu-id="3990f-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3990f-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3990f-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3990f-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3990f-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3990f-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3990f-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3990f-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="3990f-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3990f-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="3990f-112">Description</span><span class="sxs-lookup"><span data-stu-id="3990f-112">Description</span></span>

<span data-ttu-id="3990f-113">Este exemplo mostra como fornecer uma barra de ferramentas simples para uma visualização de miniaturas da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3990f-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="3990f-114">A barra de ferramentas consiste em três botões.</span><span class="sxs-lookup"><span data-stu-id="3990f-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="3990f-115">Clicar em um botão exibe uma janela para confirmar que o botão foi ativado.</span><span class="sxs-lookup"><span data-stu-id="3990f-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="3990f-116">As seguintes APIs são demonstradas:</span><span class="sxs-lookup"><span data-stu-id="3990f-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="3990f-117">**ITaskbarList3::ThumbBarAddButtons**</span><span class="sxs-lookup"><span data-stu-id="3990f-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="3990f-118">**ITaskbarList3::ThumbBarSetImageList**</span><span class="sxs-lookup"><span data-stu-id="3990f-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="3990f-119">Estrutura [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)</span><span class="sxs-lookup"><span data-stu-id="3990f-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="3990f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3990f-120">Requirements</span></span>



| <span data-ttu-id="3990f-121">Produto</span><span class="sxs-lookup"><span data-stu-id="3990f-121">Product</span></span>                                | <span data-ttu-id="3990f-122">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="3990f-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3990f-123">Windows</span><span class="sxs-lookup"><span data-stu-id="3990f-123">Windows</span></span>                                | <span data-ttu-id="3990f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3990f-124">Windows 7</span></span>               |
| <span data-ttu-id="3990f-125">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="3990f-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3990f-126">7.0</span><span class="sxs-lookup"><span data-stu-id="3990f-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3990f-127">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3990f-127">Downloading the Sample</span></span>

| <span data-ttu-id="3990f-128">Localização</span><span class="sxs-lookup"><span data-stu-id="3990f-128">Location</span></span>      | <span data-ttu-id="3990f-129">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="3990f-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3990f-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="3990f-130">GitHub</span></span>  | [<span data-ttu-id="3990f-131">Exemplo de TaskbarThumbnailToolbar</span><span class="sxs-lookup"><span data-stu-id="3990f-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="3990f-132">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3990f-132">Building the Sample</span></span>

<span data-ttu-id="3990f-133">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="3990f-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="3990f-134">Abra a janela do prompt de comando e navegue até o diretório do projeto **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="3990f-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="3990f-135">Digite `msbuild ThumbnailToolbar.sln`.</span><span class="sxs-lookup"><span data-stu-id="3990f-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="3990f-136">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="3990f-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="3990f-137">Abra o Windows Explorer e navegue até o diretório do projeto **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="3990f-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="3990f-138">Clique duas vezes no ícone do arquivo ThumbnailToolbar. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3990f-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3990f-139">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="3990f-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3990f-140">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="3990f-140">Running the Sample</span></span>

1.  <span data-ttu-id="3990f-141">Navegue até o diretório que contém o novo arquivo executável (por exemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="3990f-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="3990f-142">Se estiver usando a linha de comando, digite `ThumbnailToolbar.exe` .</span><span class="sxs-lookup"><span data-stu-id="3990f-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="3990f-143">Se estiver usando o Windows Explorer, clique duas vezes no ícone para ThumbnailToolbar.exe.</span><span class="sxs-lookup"><span data-stu-id="3990f-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="3990f-144">Uma nova janela será aberta, com um botão da barra de tarefas associado.</span><span class="sxs-lookup"><span data-stu-id="3990f-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="3990f-145">Focalize o cursor sobre o botão da barra de tarefas **ThumbnailToolbar** para que a visualização seja exibida.</span><span class="sxs-lookup"><span data-stu-id="3990f-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="3990f-146">Clique em um dos três botões (verde, amarelo, vermelho) mostrado na barra de ferramentas da visualização.</span><span class="sxs-lookup"><span data-stu-id="3990f-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="3990f-147">Escolha **sair** no menu **arquivo** da janela para encerrar o programa.</span><span class="sxs-lookup"><span data-stu-id="3990f-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3990f-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3990f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3990f-149">Extensões da barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="3990f-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



