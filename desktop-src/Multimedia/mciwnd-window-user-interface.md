---
title: Interface do usuário da janela do MCIWnd
description: Interface do usuário da janela do MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005134"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="ccef7-103">Interface do usuário da janela do MCIWnd</span><span class="sxs-lookup"><span data-stu-id="ccef7-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="ccef7-104">O MCIWnd fornece recursos adicionais para ajustar a aparência da janela MCIWnd, personalizar o comportamento do seu aplicativo e ajustar o desempenho da reprodução.</span><span class="sxs-lookup"><span data-stu-id="ccef7-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="ccef7-105">Os seguintes recursos estão incluídos na janela MCIWnd:</span><span class="sxs-lookup"><span data-stu-id="ccef7-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="ccef7-106">Uma barra de ferramentas com botões **reproduzir**, **parar**, **gravar** e **menu**</span><span class="sxs-lookup"><span data-stu-id="ccef7-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="ccef7-107">Um TrackBar que controla o posicionamento dentro do conteúdo de reprodução</span><span class="sxs-lookup"><span data-stu-id="ccef7-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="ccef7-108">Um menu pop-up contendo comandos comuns</span><span class="sxs-lookup"><span data-stu-id="ccef7-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="ccef7-109">Uma área de reprodução para vídeo e outros dispositivos que exibem imagens</span><span class="sxs-lookup"><span data-stu-id="ccef7-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="ccef7-110">A ilustração a seguir mostra o estado inicial da reprodução de vídeo controlada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ccef7-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="ccef7-111">O arquivo de exemplo usado é CLOCK.AVI.</span><span class="sxs-lookup"><span data-stu-id="ccef7-111">The sample file used is CLOCK.AVI.</span></span>

![clock.avi imagem](images/mciwnd1.gif)

<span data-ttu-id="ccef7-113">A janela MCIWnd inclui uma área de reprodução para vídeo e outros dispositivos que exibem imagens durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="ccef7-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="ccef7-114">MCIWnd omite a área de reprodução de dispositivos de onda-áudio, seqüenciadores MIDI e outros dispositivos que não gravam na exibição.</span><span class="sxs-lookup"><span data-stu-id="ccef7-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="ccef7-115">A ilustração a seguir mostra a área de reprodução de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="ccef7-115">The following illustration shows the waveform-audio playback area.</span></span>

![imagem da janela MCIWnd](images/mciwnd4.gif)

<span data-ttu-id="ccef7-117">O botão **Play** está localizado no canto inferior esquerdo da janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ccef7-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="ccef7-118">Ele aparece quando o conteúdo é interrompido.</span><span class="sxs-lookup"><span data-stu-id="ccef7-118">It appears when the content is stopped.</span></span> <span data-ttu-id="ccef7-119">O usuário pode reproduzir o conteúdo das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="ccef7-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="ccef7-120">Para reproduzir o conteúdo da posição de reprodução atual, selecione o botão **reproduzir** .</span><span class="sxs-lookup"><span data-stu-id="ccef7-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="ccef7-121">Para reproduzir o conteúdo em tela inteira da posição de reprodução atual, selecione o botão **reproduzir** enquanto mantém a tecla Ctrl pressionada.</span><span class="sxs-lookup"><span data-stu-id="ccef7-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="ccef7-122">Para reproduzir o conteúdo para trás da posição de reprodução atual, selecione o botão **reproduzir** enquanto mantém a tecla Shift pressionada.</span><span class="sxs-lookup"><span data-stu-id="ccef7-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="ccef7-123">O botão de **menu** , localizado ao lado do botão **reproduzir** , ativa um menu que permite ao usuário abrir e fechar arquivos AVI (áudio-video intercalado) e ajustar o tamanho da imagem, a velocidade de reprodução e o volume.</span><span class="sxs-lookup"><span data-stu-id="ccef7-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="ccef7-124">(O usuário também pode ativar o menu clicando com o botão direito do mouse sempre que o cursor estiver na área do cliente da janela.) O menu também inclui comandos para alterar a configuração do dispositivo atual, para copiar o conteúdo de reprodução para a área de transferência e para emitir comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="ccef7-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="ccef7-125">O TrackBar à direita do botão de **menu** representa a duração do conteúdo de reprodução (ou gravado).</span><span class="sxs-lookup"><span data-stu-id="ccef7-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="ccef7-126">O controle deslizante no TrackBar representa a posição de reprodução atual dentro do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ccef7-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="ccef7-127">Quando o controle deslizante está posicionado na extremidade esquerda do TrackBar, a posição de reprodução atual é o início do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ccef7-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="ccef7-128">O usuário pode mudar para locais diferentes no conteúdo, arrastando o controle deslizante ao longo do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="ccef7-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="ccef7-129">O botão **parar** está localizado no canto inferior esquerdo da janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ccef7-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="ccef7-130">Ele aparece quando o conteúdo é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="ccef7-130">It appears when the content is played.</span></span> <span data-ttu-id="ccef7-131">A ilustração a seguir mostra a reprodução de vídeo em andamento.</span><span class="sxs-lookup"><span data-stu-id="ccef7-131">The following illustration shows video playback in progress.</span></span>

![imagem de reprodução de vídeo](images/mciwnd2.gif)

<span data-ttu-id="ccef7-133">Os controles MCIWnd também podem incluir um botão de **registro** para dispositivos que podem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="ccef7-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="ccef7-134">O botão **gravar** é marcado com um círculo vermelho e aparece somente quando o dispositivo é capaz de gravar.</span><span class="sxs-lookup"><span data-stu-id="ccef7-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="ccef7-135">A janela de reprodução deve estar alinhada a um limite de quatro pixels para obter o melhor desempenho de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ccef7-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="ccef7-136">Normalmente, o Windows alinha a janela automaticamente quando ela é criada.</span><span class="sxs-lookup"><span data-stu-id="ccef7-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="ccef7-137">Se um usuário mover ou alongar a janela de sua posição inicial, a velocidade de reprodução do vídeo poderá ser reduzida pela metade.</span><span class="sxs-lookup"><span data-stu-id="ccef7-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




