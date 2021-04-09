---
description: Este exemplo usa as APIs de áudio principais para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é executado por meio do dispositivo de ponto de extremidade de renderização de áudio padrão.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD Feature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010220"
---
# <a name="osd"></a><span data-ttu-id="4d800-103">OSD Feature</span><span class="sxs-lookup"><span data-stu-id="4d800-103">OSD</span></span>

<span data-ttu-id="4d800-104">Este exemplo usa as APIs de áudio principais para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é executado por meio do dispositivo de ponto de extremidade de renderização de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="4d800-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="4d800-105">A exibição na tela é exibida quando o usuário ajusta o nível de volume no programa de controle de volume do Windows, Sndvol.exe e desaparece depois que o nível do volume permanece inalterado por um curto período de tempo.</span><span class="sxs-lookup"><span data-stu-id="4d800-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="4d800-106">Este tópico contém as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d800-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="4d800-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d800-107">Description</span></span>](#description)
-   [<span data-ttu-id="4d800-108">Requirements</span><span class="sxs-lookup"><span data-stu-id="4d800-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4d800-109">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4d800-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4d800-110">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4d800-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4d800-111">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4d800-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="4d800-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d800-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="4d800-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d800-113">Description</span></span>

<span data-ttu-id="4d800-114">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d800-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="4d800-115">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="4d800-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="4d800-116">[API EndpointVolume](endpointvolume-api.md) de áudio</span><span class="sxs-lookup"><span data-stu-id="4d800-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="4d800-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d800-117">Requirements</span></span>



| <span data-ttu-id="4d800-118">Produto</span><span class="sxs-lookup"><span data-stu-id="4d800-118">Product</span></span>                                                        | <span data-ttu-id="4d800-119">Versão</span><span class="sxs-lookup"><span data-stu-id="4d800-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="4d800-120">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="4d800-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="4d800-121">Windows Vista ou posterior</span><span class="sxs-lookup"><span data-stu-id="4d800-121">Windows Vista or later</span></span> |
| <span data-ttu-id="4d800-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4d800-122">Visual Studio</span></span>                                                  | <span data-ttu-id="4d800-123">2005 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4d800-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4d800-124">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4d800-124">Downloading the Sample</span></span>

<span data-ttu-id="4d800-125">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d800-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="4d800-126">Local</span><span class="sxs-lookup"><span data-stu-id="4d800-126">Location</span></span>    | <span data-ttu-id="4d800-127">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="4d800-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d800-128">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="4d800-128">Windows SDK</span></span> | <span data-ttu-id="4d800-129">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ OSD \\ ...</span><span class="sxs-lookup"><span data-stu-id="4d800-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="4d800-130">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4d800-130">Building the Sample</span></span>

1.  <span data-ttu-id="4d800-131">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo OSD.</span><span class="sxs-lookup"><span data-stu-id="4d800-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="4d800-132">Execute o comando "Start OSD. sln" no diretório OSD para abrir o projeto OSD na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4d800-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="4d800-133">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="4d800-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="4d800-134">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="4d800-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="4d800-135">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, OSD. vcproj.</span><span class="sxs-lookup"><span data-stu-id="4d800-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4d800-136">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4d800-136">Running the Sample</span></span>

1.  <span data-ttu-id="4d800-137">Execute o arquivo executável OSD, OSD.exe, no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4d800-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="4d800-138">Observe que você não verá um ícone de bandeja do sistema ou uma janela para o aplicativo, mas poderá ver o processo em execução usando TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="4d800-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="4d800-139">Execute sndvol.exe para alterar o volume ou mudo, ou altere o volume usando controles de teclado ou um controle HID.</span><span class="sxs-lookup"><span data-stu-id="4d800-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="4d800-140">A interface do usuário do OSD é exibida.</span><span class="sxs-lookup"><span data-stu-id="4d800-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="4d800-141">Para sair do aplicativo, execute TaskMgr.exe, realce o processo de OSD.exe e clique em **encerrar processo**.</span><span class="sxs-lookup"><span data-stu-id="4d800-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d800-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d800-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d800-143">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="4d800-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



