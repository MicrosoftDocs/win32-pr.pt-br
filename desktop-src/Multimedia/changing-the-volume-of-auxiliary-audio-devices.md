---
title: Alterando o volume de Audio-Devices auxiliares
description: Alterando o volume de Audio-Devices auxiliares
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- áudio de formato de onda, alterando o volume do dispositivo de áudio auxiliar
- alterando o volume do dispositivo de áudio auxiliar
- áudio auxiliar, alterando o volume do dispositivo
- interface de áudio auxiliar
- dispositivos de áudio auxiliares, alterando o volume
- áudio auxiliar, interface
- áudio auxiliar, dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641104"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="91ebe-110">Alterando o volume de Audio-Devices auxiliares</span><span class="sxs-lookup"><span data-stu-id="91ebe-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="91ebe-111">O Windows fornece as seguintes funções para consultar e definir o volume para dispositivos de áudio auxiliares.</span><span class="sxs-lookup"><span data-stu-id="91ebe-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="91ebe-112">Função</span><span class="sxs-lookup"><span data-stu-id="91ebe-112">Function</span></span>                             | <span data-ttu-id="91ebe-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="91ebe-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="91ebe-114">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="91ebe-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="91ebe-115">Recupera a configuração de volume atual do dispositivo de saída auxiliar especificado.</span><span class="sxs-lookup"><span data-stu-id="91ebe-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="91ebe-116">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="91ebe-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="91ebe-117">Define o volume do dispositivo de saída auxiliar especificado.</span><span class="sxs-lookup"><span data-stu-id="91ebe-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="91ebe-118">Nem todos os dispositivos de áudio auxiliar dão suporte a alterações de volume.</span><span class="sxs-lookup"><span data-stu-id="91ebe-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="91ebe-119">Alguns dispositivos podem dar suporte a alterações de volume individuais nos canais esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="91ebe-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="91ebe-120">O volume é especificado em um valor doubleword, assim como as funções de controle de volume de wave-áudio e MIDI.</span><span class="sxs-lookup"><span data-stu-id="91ebe-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="91ebe-121">Quando o formato de áudio é estéreo, os 16 bits superiores especificam o volume relativo do canal correto e os 16 bits inferiores especificam o volume relativo do canal esquerdo.</span><span class="sxs-lookup"><span data-stu-id="91ebe-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="91ebe-122">Para dispositivos que não dão suporte ao controle de volume de canal esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados.</span><span class="sxs-lookup"><span data-stu-id="91ebe-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="91ebe-123">Os valores de nível de volume variam de 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logaritmicamente.</span><span class="sxs-lookup"><span data-stu-id="91ebe-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="91ebe-124">O aumento do volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.</span><span class="sxs-lookup"><span data-stu-id="91ebe-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 