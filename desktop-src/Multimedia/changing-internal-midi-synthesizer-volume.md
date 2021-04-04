---
title: Alterando o volume do sintetizador MIDI interno
description: Alterando o volume do sintetizador MIDI interno
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- MIDI (interface digital de instrumento musical), sintetizadores internos
- MIDI (interface digital de instrumentos musicais), sintetizadores internos
- executando arquivos MIDI, sintetizadores internos
- sintetizadores MIDI internos
- MIDI (interface digital de instrumento musical), alterando o volume
- MIDI (interface digital de instrumento musical), alterando o volume
- executando arquivos MIDI, alterando o volume
- alterando o volume MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917274"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="64da7-111">Alterando o volume do sintetizador MIDI interno</span><span class="sxs-lookup"><span data-stu-id="64da7-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="64da7-112">O Windows fornece as seguintes funções para recuperar e definir o nível de volume de dispositivos de sintetizador MIDI internos:</span><span class="sxs-lookup"><span data-stu-id="64da7-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="64da7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="64da7-113">Value</span></span>                                        | <span data-ttu-id="64da7-114">Significado</span><span class="sxs-lookup"><span data-stu-id="64da7-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="64da7-115">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="64da7-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="64da7-116">Recupera o nível de volume do dispositivo de sintetizador MIDI interno especificado.</span><span class="sxs-lookup"><span data-stu-id="64da7-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="64da7-117">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="64da7-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="64da7-118">Define o nível de volume do dispositivo de sintetizador MIDI interno especificado.</span><span class="sxs-lookup"><span data-stu-id="64da7-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="64da7-119">Nem todos os dispositivos de saída MIDI dão suporte a alterações de volume.</span><span class="sxs-lookup"><span data-stu-id="64da7-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="64da7-120">Alguns dispositivos podem dar suporte a alterações de volume individuais nos canais esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="64da7-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="64da7-121">Para obter informações sobre como determinar se um dispositivo específico dá suporte a alterações de volume, consulte [consultando dispositivos de saída de Midi](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="64da7-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="64da7-122">A menos que seu aplicativo seja projetado para ser um aplicativo mestre de controle de volume (fornece ao usuário controle de volume para todos os dispositivos de áudio em um sistema), você deve abrir um dispositivo de áudio antes de alterar seu volume.</span><span class="sxs-lookup"><span data-stu-id="64da7-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="64da7-123">Você também deve verificar o nível de volume antes de alterá-lo e restaurar o nível de volume para seu nível anterior assim que possível.</span><span class="sxs-lookup"><span data-stu-id="64da7-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="64da7-124">O volume é especificado como um valor de doubleword.</span><span class="sxs-lookup"><span data-stu-id="64da7-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="64da7-125">Os 16 bits superiores especificam o volume relativo do canal correto e os 16 bits inferiores especificam o volume relativo do canal esquerdo.</span><span class="sxs-lookup"><span data-stu-id="64da7-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="64da7-126">Para dispositivos que não dão suporte a alterações de volume individuais nos canais esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados.</span><span class="sxs-lookup"><span data-stu-id="64da7-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="64da7-127">Valores para o intervalo de nível de volume de 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logaritmicamente.</span><span class="sxs-lookup"><span data-stu-id="64da7-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="64da7-128">O aumento do volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.</span><span class="sxs-lookup"><span data-stu-id="64da7-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 