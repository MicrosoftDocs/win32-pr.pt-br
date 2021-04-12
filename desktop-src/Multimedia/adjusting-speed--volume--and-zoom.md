---
title: Ajustando a velocidade, o volume e o zoom
description: Ajustando a velocidade, o volume e o zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Macro MCIWndSetSpeed
- Macro MCIWndGetSpeed
- Macro MCIWndSetVolume
- Macro MCIWndGetVolume
- Macro MCIWndSetZoom
- Macro MCIWndGetZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364041"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="4be0d-109">Ajustando a velocidade, o volume e o zoom</span><span class="sxs-lookup"><span data-stu-id="4be0d-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="4be0d-110">A velocidade, o volume e as macros de zoom fornecem a funcionalidade dos comandos de **exibição**, **volume** e **velocidade** no menu MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="4be0d-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="4be0d-111">As macros descritas nesta seção geralmente são usadas com vídeo e outros dispositivos que exibem imagens durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="4be0d-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="4be0d-112">Alguns dispositivos dão suporte a várias alterações na velocidade de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4be0d-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="4be0d-113">Você pode definir a velocidade de reprodução para esses dispositivos usando a macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="4be0d-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="4be0d-114">Essa macro define a velocidade de reprodução como 1000.</span><span class="sxs-lookup"><span data-stu-id="4be0d-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="4be0d-115">Valores mais altos indicam velocidades mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="4be0d-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="4be0d-116">Valores mais baixos indicam velocidades mais lentas.</span><span class="sxs-lookup"><span data-stu-id="4be0d-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="4be0d-117">Você pode recuperar a velocidade de reprodução atual usando a macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="4be0d-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="4be0d-118">Essa macro usa os mesmos valores e intervalos usados pelo **MCIWndSetSpeed**.</span><span class="sxs-lookup"><span data-stu-id="4be0d-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="4be0d-119">Alguns dispositivos dão suporte a alterações de volume.</span><span class="sxs-lookup"><span data-stu-id="4be0d-119">Some devices support volume changes.</span></span> <span data-ttu-id="4be0d-120">Você pode ajustar ou definir o volume usando a macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="4be0d-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="4be0d-121">Essa macro define o nível de volume normal como 1000.</span><span class="sxs-lookup"><span data-stu-id="4be0d-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="4be0d-122">Valores mais altos indicam volumes mais altos.</span><span class="sxs-lookup"><span data-stu-id="4be0d-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="4be0d-123">Valores mais baixos indicam volumes mais silenciosos.</span><span class="sxs-lookup"><span data-stu-id="4be0d-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="4be0d-124">Você pode recuperar o nível de volume atual usando a macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="4be0d-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="4be0d-125">Essa macro usa os mesmos valores numéricos e o intervalo usado pelo **MCIWndSetVolume**.</span><span class="sxs-lookup"><span data-stu-id="4be0d-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="4be0d-126">Para dispositivos que usam uma janela de reprodução, o MCIWnd dá suporte a um recurso de zoom que define o tamanho da imagem de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4be0d-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="4be0d-127">Você pode definir o tamanho da imagem de reprodução usando a macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="4be0d-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="4be0d-128">A macro redefine o tamanho da imagem de reprodução enquanto mantém uma taxa de proporção constante para a imagem.</span><span class="sxs-lookup"><span data-stu-id="4be0d-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="4be0d-129">O valor de zoom é definido como uma porcentagem do tamanho da imagem original.</span><span class="sxs-lookup"><span data-stu-id="4be0d-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="4be0d-130">Assim, 100 representa o tamanho original da imagem, 50 indica que a imagem mostrada é metade do tamanho original e 200 indica que a imagem mostrada é duas vezes seu tamanho original.</span><span class="sxs-lookup"><span data-stu-id="4be0d-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="4be0d-131">Você pode recuperar o valor de zoom atual usando a macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="4be0d-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="4be0d-132">Essa macro usa os mesmos valores e intervalos usados pelo **MCIWndSetZoom**.</span><span class="sxs-lookup"><span data-stu-id="4be0d-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="4be0d-133">Os drivers áudio de CD MCI e Wave-audio padrão não dão suporte a alterações de volume ou velocidade.</span><span class="sxs-lookup"><span data-stu-id="4be0d-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




