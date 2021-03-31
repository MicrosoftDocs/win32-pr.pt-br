---
title: Sobre MIDI
description: Sobre MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Multimídia do Windows, MIDI (interface digital de instrumentos musicais)
- multimídia, MIDI (interface digital de instrumentos musicais)
- áudio multimídia, MIDI (interface digital de instrumentos musicais)
- áudio, MIDI (interface digital de instrumento musical)
- MIDI (interface digital de instrumento musical), sobre
- MIDI (interface digital de instrumentos musicais), sobre
- MIDI (interface digital de instrumento musical), MCI (interface de controle de mídia)
- MIDI (interface digital de instrumentos musicais), MCI (interface de controle de mídia)
- MIDI (interface digital de instrumento musical), buffers de fluxo
- MIDI (interface digital de instrumentos musicais), buffers de fluxo
- MIDI (interface digital de instrumento musical), serviços de MIDI
- MIDI (interface digital de instrumentos musicais), serviços de MIDI
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- MCI (interface de controle de mídia), MIDI (interface digital de instrumento musical)
- buffers de fluxo, sobre
- Serviços de MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635377"
---
# <a name="about-midi"></a><span data-ttu-id="7dcff-119">Sobre MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-119">About MIDI</span></span>

<span data-ttu-id="7dcff-120">A API (interface de programação de aplicativo) do Microsoft Win32 fornece os seguintes métodos para que os aplicativos funcionem com dados MIDI:</span><span class="sxs-lookup"><span data-stu-id="7dcff-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="7dcff-121">A interface de controle de mídia (MCI).</span><span class="sxs-lookup"><span data-stu-id="7dcff-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="7dcff-122">Embora a maneira mais simples de reproduzir um arquivo MIDI seja usar a classe Window MCIWnd, você também pode usar comandos MCI para criar uma interface personalizada para um dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dcff-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="7dcff-123">Para obter mais informações sobre a classe de janela MCIWnd, consulte [classe de janela MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="7dcff-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="7dcff-124">Para obter mais informações sobre o MCI, consulte [MCI](mci.md)ou [MCI (interface de controle de mídia)](media-control-interface--mci.md).</span><span class="sxs-lookup"><span data-stu-id="7dcff-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="7dcff-125">[Buffers de fluxo](stream-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="7dcff-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="7dcff-126">Esse formato permite que um aplicativo manipule buffers de dados MIDI com carimbo de data/hora para reprodução.</span><span class="sxs-lookup"><span data-stu-id="7dcff-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="7dcff-127">Os buffers de fluxo são úteis para aplicativos que exigem um controle mais preciso sobre a saída do que as ofertas MCI.</span><span class="sxs-lookup"><span data-stu-id="7dcff-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="7dcff-128">[Serviços de Midi](midi-services.md).</span><span class="sxs-lookup"><span data-stu-id="7dcff-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="7dcff-129">Os aplicativos que precisam do controle mais preciso de dados MIDI normalmente usam esses serviços de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="7dcff-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="7dcff-130">Os tópicos a seguir abordam cada um desses métodos e fornecem uma visão geral do mapeador de MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dcff-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="7dcff-131">O mapeador de MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="7dcff-132">MCI (interface de controle de mídia)</span><span class="sxs-lookup"><span data-stu-id="7dcff-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="7dcff-133">Buffers de fluxo</span><span class="sxs-lookup"><span data-stu-id="7dcff-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="7dcff-134">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="7dcff-135">Executando arquivos MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="7dcff-136">Gravando áudio MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="7dcff-137">Processando dados MIDI de duas fontes MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="7dcff-138">Criando arquivos MIDI</span><span class="sxs-lookup"><span data-stu-id="7dcff-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 




