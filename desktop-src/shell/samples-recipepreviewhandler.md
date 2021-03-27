---
description: Demonstra como escrever um manipulador usado para exibir uma visualização de arquivo dentro do painel de visualização do Windows Explorer ou outros hosts do Gerenciador de visualização.
title: Exemplo do manipulador de visualização de receitas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968074"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="f901b-103">Exemplo do manipulador de visualização de receitas</span><span class="sxs-lookup"><span data-stu-id="f901b-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="f901b-104">Demonstra como escrever um manipulador usado para exibir uma visualização de arquivo dentro do painel de visualização do Windows Explorer ou outros hosts do Gerenciador de visualização.</span><span class="sxs-lookup"><span data-stu-id="f901b-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="f901b-105">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="f901b-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f901b-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f901b-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f901b-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f901b-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f901b-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f901b-110">Cancelando o registro da DLL do Gerenciador de visualização de exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="f901b-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f901b-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="f901b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f901b-112">Requirements</span></span>



| <span data-ttu-id="f901b-113">Produto</span><span class="sxs-lookup"><span data-stu-id="f901b-113">Product</span></span>                                | <span data-ttu-id="f901b-114">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="f901b-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f901b-115">Windows</span><span class="sxs-lookup"><span data-stu-id="f901b-115">Windows</span></span>                                | <span data-ttu-id="f901b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f901b-116">Windows Vista</span></span>           |
| <span data-ttu-id="f901b-117">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f901b-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f901b-118">7.0</span><span class="sxs-lookup"><span data-stu-id="f901b-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f901b-119">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-119">Downloading the Sample</span></span>

| <span data-ttu-id="f901b-120">Localização</span><span class="sxs-lookup"><span data-stu-id="f901b-120">Location</span></span>      | <span data-ttu-id="f901b-121">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="f901b-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f901b-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="f901b-122">GitHub</span></span>  | [<span data-ttu-id="f901b-123">Exemplo de RecipePreviewHandler</span><span class="sxs-lookup"><span data-stu-id="f901b-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="f901b-124">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-124">Building the Sample</span></span>

<span data-ttu-id="f901b-125">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="f901b-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="f901b-126">Abra a janela do prompt de comando e navegue até o diretório do projeto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="f901b-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="f901b-127">Por exemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="f901b-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="f901b-128">Digite `msbuild PreviewHandlerSDKSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="f901b-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="f901b-129">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="f901b-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="f901b-130">Abra o Windows Explorer e navegue até o diretório do projeto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="f901b-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="f901b-131">Clique duas vezes no ícone do arquivo PreviewHandlerSDKSample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f901b-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="f901b-132">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="f901b-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="f901b-133">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="f901b-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="f901b-134">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="f901b-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="f901b-135">Se o sistema de destino for de 64 bits (x64), esse Gerenciador de visualização de exemplo deve ser criado como um aplicativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f901b-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="f901b-136">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-136">Running the Sample</span></span>

1.  <span data-ttu-id="f901b-137">Abra a janela do prompt de comando e navegue até o diretório do projeto **RecipePreviewHandler** criado.</span><span class="sxs-lookup"><span data-stu-id="f901b-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="f901b-138">Por exemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="f901b-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="f901b-139">Insira `regsvr32.exe PreviewHandlerSDKSample.dll` para registrar o manipulador.</span><span class="sxs-lookup"><span data-stu-id="f901b-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="f901b-140">Abra o Windows Explorer e mostre o painel de visualização se ele ainda não estiver sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="f901b-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="f901b-141">**Windows 7**: clique no botão painel de visualização.</span><span class="sxs-lookup"><span data-stu-id="f901b-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="f901b-142">**Windows Vista**: clique no menu **organizar** , vá para o submenu **layout** e selecione **painel de visualização**.</span><span class="sxs-lookup"><span data-stu-id="f901b-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="f901b-143">Use o Windows Explorer para navegar até o diretório do projeto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="f901b-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="f901b-144">Selecione o arquivo. recipe de exemplo.</span><span class="sxs-lookup"><span data-stu-id="f901b-144">Select the example .recipe file.</span></span>

<span data-ttu-id="f901b-145">Para fazer com que a saída de 32 bits (x86) e 64 bits (x64) funcione em uma versão de 64 bits do Windows, defina o valor **AppID** para o host substituto do WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f901b-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="f901b-146">Cancelando o registro da DLL do Gerenciador de visualização de exemplo</span><span class="sxs-lookup"><span data-stu-id="f901b-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="f901b-147">Abra a janela de prompt de comando e insira `regsvr32.exe /u PreviewHandlerSDKSample.dll` para cancelar o registro do manipulador.</span><span class="sxs-lookup"><span data-stu-id="f901b-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f901b-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f901b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f901b-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="f901b-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="f901b-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="f901b-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="f901b-151">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="f901b-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
