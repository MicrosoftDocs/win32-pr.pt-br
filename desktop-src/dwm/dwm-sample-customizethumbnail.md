---
title: Personalizar uma miniatura icônica e um bitmap de versão prévia dinâmica
description: Mostra como personalizar uma miniatura de icônico e um bitmap de visualização dinâmica (também chamado de visualização de inspeção).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105787670"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="8bed0-103">Personalizar uma miniatura icônica e um bitmap de versão prévia dinâmica</span><span class="sxs-lookup"><span data-stu-id="8bed0-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="8bed0-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bed0-104">Description</span></span>

<span data-ttu-id="8bed0-105">Você pode personalizar uma miniatura de icônico e um bitmap de *Visualização dinâmica* (ou *visualização de inspeção*) usando funções e mensagens que são introduzidas nas APIs do Windows 7 Gerenciador de janelas da área de trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="8bed0-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="8bed0-106">Especificamente, você usa a função [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) e a [**mensagem \_ SENDICONICTHUMBNAILBITMAP do WM**](wm-dwmsendiconicthumbnail.md) para personalizar uma miniatura icônico.</span><span class="sxs-lookup"><span data-stu-id="8bed0-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="8bed0-107">Você também pode usar a função [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) e a mensagem do [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) para definir um bitmap de visualização dinâmica do icônico.</span><span class="sxs-lookup"><span data-stu-id="8bed0-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="8bed0-108">Para um aplicativo de exemplo que usa a função **DwmSetIconicThumbnail** , consulte o [exemplo TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span><span class="sxs-lookup"><span data-stu-id="8bed0-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="8bed0-109">A ilustração a seguir mostra uma miniatura padrão transformada em uma miniatura personalizada.</span><span class="sxs-lookup"><span data-stu-id="8bed0-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![ilustração de uma imagem em miniatura original e uma imagem em miniatura modificada com um bitmap personalizado](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="8bed0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bed0-111">Requirements</span></span>

| <span data-ttu-id="8bed0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bed0-112">Requirement</span></span> | <span data-ttu-id="8bed0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8bed0-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bed0-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bed0-114">Minimum supported client</span></span> | <span data-ttu-id="8bed0-115">Windows 7 ou Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bed0-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="8bed0-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bed0-116">Minimum supported server</span></span> | <span data-ttu-id="8bed0-117">Windows Server 2008 R2 ou Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bed0-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="8bed0-118">SDK do Windows mínimo</span><span class="sxs-lookup"><span data-stu-id="8bed0-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="8bed0-119">SDK (Software Development Kit) do Windows para Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bed0-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="8bed0-120">Criando o exemplo de TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="8bed0-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="8bed0-121">**Para compilar o exemplo usando Microsoft Visual Studio (método preferencial)**</span><span class="sxs-lookup"><span data-stu-id="8bed0-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="8bed0-122">Abra o Windows Explorer e navegue até a pasta onde o arquivo TabThumbnails. sln está localizado.</span><span class="sxs-lookup"><span data-stu-id="8bed0-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="8bed0-123">Clique duas vezes no arquivo de solução (. sln) para abrir o arquivo em Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8bed0-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="8bed0-124">No menu **Compilar**, clique em **Compilar Solução**.</span><span class="sxs-lookup"><span data-stu-id="8bed0-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="8bed0-125">O aplicativo é criado no diretório de \\ depuração ou de \\ lançamento padrão.</span><span class="sxs-lookup"><span data-stu-id="8bed0-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="8bed0-126">**Para criar o exemplo usando o prompt de comando**</span><span class="sxs-lookup"><span data-stu-id="8bed0-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="8bed0-127">Abra uma janela de prompt de comando e navegue até o diretório de exemplo.</span><span class="sxs-lookup"><span data-stu-id="8bed0-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="8bed0-128">Digite `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="8bed0-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bed0-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bed0-129">Related topics</span></span>

[<span data-ttu-id="8bed0-130">Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8bed0-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="8bed0-131">Desenvolvimento em Windows</span><span class="sxs-lookup"><span data-stu-id="8bed0-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
