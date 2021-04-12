---
title: Alterando a taxa de densidade e reprodução
description: Alterando a taxa de densidade e reprodução
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- áudio de onda, densidade
- Wave-interface de áudio, pitch
- áudio de forma de onda, taxa de reprodução
- forma de onda-interface de áudio, taxa de reprodução
- áudio de onda, mudança de Tom
- Wave-interface de áudio, alterando a densidade
- áudio de forma de onda, alterando a taxa de reprodução
- forma de onda-interface de áudio, alterando taxa de reprodução
- alterando a forma de onda-taxa de reprodução de áudio
- alterando a onda-densidade de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454066"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="9b8d3-113">Alterando a taxa de densidade e reprodução</span><span class="sxs-lookup"><span data-stu-id="9b8d3-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="9b8d3-114">Alguns dispositivos de saída de wave-áudio podem variar a densidade e a taxa de reprodução dos dados de áudio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="9b8d3-115">Nem todos os dispositivos de wave-áudio dão suporte a alterações de taxa de reprodução e de densidade.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="9b8d3-116">Para obter informações sobre como determinar se um dispositivo de wave-áudio específico dá suporte a alterações de taxa de reprodução e de densidade, consulte [dispositivos e tipos de dados](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="9b8d3-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="9b8d3-117">As diferenças entre a alteração da taxa de densidade e de reprodução são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="9b8d3-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="9b8d3-118">A alteração da taxa de reprodução é executada pelo driver de dispositivo e não requer hardware especializado.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="9b8d3-119">A taxa de amostra não é alterada, mas o driver interpola-se ignorando ou sintetizando amostras.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="9b8d3-120">Por exemplo, se a taxa de reprodução for alterada por um fator de dois, o driver ignorará todas as outras amostras.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="9b8d3-121">A alteração da densidade exige hardware especializado.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="9b8d3-122">A taxa de reprodução e a taxa de amostragem não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="9b8d3-123">O Windows fornece as seguintes funções para consultar e definir o tom de onda-áudio e as taxas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="9b8d3-124">Função</span><span class="sxs-lookup"><span data-stu-id="9b8d3-124">Function</span></span>                                                 | <span data-ttu-id="9b8d3-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b8d3-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="9b8d3-126">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="9b8d3-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="9b8d3-127">Recupera a densidade do dispositivo de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="9b8d3-128">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="9b8d3-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="9b8d3-129">Recupera a taxa de reprodução para o dispositivo de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="9b8d3-130">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="9b8d3-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="9b8d3-131">Define a densidade para o dispositivo de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="9b8d3-132">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="9b8d3-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="9b8d3-133">Define a taxa de reprodução para o dispositivo de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="9b8d3-134">As taxas de densidade e reprodução são alteradas por um fator especificado com um número de ponto fixo empacotado em um valor de doubleword.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="9b8d3-135">Os 16 bits superiores especificam a parte inteira do número; os 16 bits inferiores especificam a parte fracionária.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="9b8d3-136">Por exemplo, o valor 1,5 é representado como 0x00018000L.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="9b8d3-137">O valor 0,75 é representado como 0x0000C000L.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="9b8d3-138">Um valor de 1,0 (0x00010000) significa que a taxa de densidade ou reprodução não foi alterada.</span><span class="sxs-lookup"><span data-stu-id="9b8d3-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 