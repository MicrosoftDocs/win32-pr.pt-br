---
title: Erros de Waveform-Audio
description: Erros de Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valores de retorno de MCIERR, formato de onda-erros de áudio
- referência de multimídia, erros de wave-áudio
- referência para multimídia, erros de wave-áudio
- MCI (Media Control interface), erros de wave-áudio
- MCI (interface de controle de mídia), erros de formato de onda-áudio
- referência de erros MCI, wave-áudio
- Referência MCI, erros de áudio de onda
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- formato de onda-erros de áudio
- Formato de onda MCI-erros de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005113"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="e240e-116">Erros de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="e240e-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="e240e-117">Os seguintes valores de retorno adicionais são definidos para dispositivos MCI Wave-Audio:</span><span class="sxs-lookup"><span data-stu-id="e240e-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="e240e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e240e-118">Value</span></span>                             | <span data-ttu-id="e240e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="e240e-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e240e-120">MCIERR \_ Wave \_ INPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="e240e-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="e240e-121">Todos os dispositivos de forma de onda que podem gravar arquivos no formato atual estão em uso.</span><span class="sxs-lookup"><span data-stu-id="e240e-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="e240e-122">Aguarde até que um desses dispositivos seja gratuito; em seguida, tente novamente.</span><span class="sxs-lookup"><span data-stu-id="e240e-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="e240e-123">MCIERR \_ Wave \_ INPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="e240e-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="e240e-124">Nenhum dispositivo de forma de onda instalado pode gravar arquivos no formato atual.</span><span class="sxs-lookup"><span data-stu-id="e240e-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="e240e-125">Use a opção drivers do painel de controle para instalar um dispositivo de gravação de formato de onda adequado.</span><span class="sxs-lookup"><span data-stu-id="e240e-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="e240e-126">MCIERR \_ Wave \_ INPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="e240e-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="e240e-127">Você pode especificar qualquer dispositivo de gravação de formato de onda compatível.</span><span class="sxs-lookup"><span data-stu-id="e240e-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="e240e-128">MCIERR \_ Wave \_ OUTPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="e240e-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="e240e-129">Todos os dispositivos de forma de onda que podem reproduzir arquivos no formato atual estão em uso.</span><span class="sxs-lookup"><span data-stu-id="e240e-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="e240e-130">Aguarde até que um desses dispositivos seja gratuito; em seguida, tente novamente.</span><span class="sxs-lookup"><span data-stu-id="e240e-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="e240e-131">MCIERR \_ Wave \_ OUTPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="e240e-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="e240e-132">Nenhum dispositivo de forma de onda instalado pode reproduzir arquivos no formato atual.</span><span class="sxs-lookup"><span data-stu-id="e240e-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="e240e-133">Use a opção drivers do painel de controle para instalar um dispositivo de formato de onda adequado.</span><span class="sxs-lookup"><span data-stu-id="e240e-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="e240e-134">MCIERR \_ Wave \_ OUTPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="e240e-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="e240e-135">Você pode especificar qualquer dispositivo de reprodução de formato de onda compatível.</span><span class="sxs-lookup"><span data-stu-id="e240e-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="e240e-136">MCIERR \_ Wave \_ SETINPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="e240e-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="e240e-137">O dispositivo de formato de onda atual está em uso.</span><span class="sxs-lookup"><span data-stu-id="e240e-137">The current waveform device is in use.</span></span> <span data-ttu-id="e240e-138">Aguarde até que o dispositivo seja gratuito; em seguida, tente definir o dispositivo novamente para gravação.</span><span class="sxs-lookup"><span data-stu-id="e240e-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="e240e-139">MCIERR \_ Wave \_ SETINPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="e240e-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="e240e-140">O dispositivo que você está usando para registrar uma forma de onda não pode reconhecer o formato de dados.</span><span class="sxs-lookup"><span data-stu-id="e240e-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="e240e-141">MCIERR \_ Wave \_ SETOUTPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="e240e-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="e240e-142">O dispositivo de formato de onda atual está em uso.</span><span class="sxs-lookup"><span data-stu-id="e240e-142">The current waveform device is in use.</span></span> <span data-ttu-id="e240e-143">Aguarde até que o dispositivo seja gratuito; em seguida, tente definir o dispositivo novamente para reprodução.</span><span class="sxs-lookup"><span data-stu-id="e240e-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="e240e-144">MCIERR \_ Wave \_ SETOUTPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="e240e-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="e240e-145">O dispositivo que você está usando para reproduzir uma forma de onda não pode reconhecer o formato de dados.</span><span class="sxs-lookup"><span data-stu-id="e240e-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 




