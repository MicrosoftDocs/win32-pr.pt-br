---
title: Parando, pausando e reiniciando a reprodução
description: Parando, pausando e reiniciando a reprodução
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- áudio de onda, parando a reprodução
- Wave-interface de áudio, parando a reprodução
- executando a onda-arquivos de áudio, parando a reprodução
- áudio de onda, pausando reprodução
- Wave-interface de áudio, pausando reprodução
- executando a onda-arquivos de áudio, pausando a reprodução
- áudio de onda, reiniciando a reprodução
- Wave-interface de áudio, reiniciando a reprodução
- executando a onda-arquivos de áudio, reiniciando a reprodução
- função waveOutPause
- função waveOutReset
- função waveOutRestart
- parando a onda-reprodução de áudio
- Pausando a onda-reprodução de áudio
- Reiniciando a onda-reprodução de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084469"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="22981-118">Parando, pausando e reiniciando a reprodução</span><span class="sxs-lookup"><span data-stu-id="22981-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="22981-119">Você pode parar ou pausar a reprodução enquanto o áudio da onda está sendo tocado.</span><span class="sxs-lookup"><span data-stu-id="22981-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="22981-120">Depois que a reprodução tiver sido pausada, você poderá reiniciá-la.</span><span class="sxs-lookup"><span data-stu-id="22981-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="22981-121">O Windows fornece as seguintes funções para controlar a reprodução de formato wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="22981-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="22981-122">Função</span><span class="sxs-lookup"><span data-stu-id="22981-122">Function</span></span>                                 | <span data-ttu-id="22981-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="22981-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22981-124">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="22981-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="22981-125">Pausa a reprodução em um dispositivo de saída de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="22981-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="22981-126">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="22981-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="22981-127">Interrompe a reprodução em um dispositivo de saída de wave-áudio e marca todos os blocos de dados pendentes como concluído.</span><span class="sxs-lookup"><span data-stu-id="22981-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="22981-128">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="22981-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="22981-129">Retoma a reprodução em um dispositivo de saída de wave-áudio em pausa.</span><span class="sxs-lookup"><span data-stu-id="22981-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="22981-130">Pausar uma wave-dispositivo de áudio usando [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) pode não ser instantâneo; o driver pode terminar de reproduzir o bloco atual antes de pausar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="22981-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="22981-131">Em geral, assim que o primeiro bloco de dados de wave-áudio é enviado usando a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , o dispositivo de forma de onda-áudio começa a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="22981-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="22981-132">Se você não quiser que o som comece a ser reproduzido imediatamente, chame **waveOutPause** antes de chamar **waveOutWrite**.</span><span class="sxs-lookup"><span data-stu-id="22981-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="22981-133">Em seguida, quando você quiser começar a reproduzir dados de formato de onda-áudio, chame [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span><span class="sxs-lookup"><span data-stu-id="22981-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="22981-134">Não é possível usar **waveOutRestart** para reiniciar um dispositivo que foi interrompido com [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); Você deve usar **waveOutWrite** para enviar o primeiro bloco de dados para retomar a reprodução no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22981-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 