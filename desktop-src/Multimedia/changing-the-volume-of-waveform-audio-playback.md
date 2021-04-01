---
title: Alterando o volume de Waveform-Audio reprodução
description: Alterando o volume de Waveform-Audio reprodução
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- áudio de onda, alterando volume de reprodução
- Wave-interface de áudio, alterando volume de reprodução
- áudio de onda, volume de reprodução
- Wave-interface de áudio, volume de reprodução
- alterando a onda-volume de reprodução de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641103"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="d813e-108">Alterando o volume de Waveform-Audio reprodução</span><span class="sxs-lookup"><span data-stu-id="d813e-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="d813e-109">O Windows fornece as seguintes funções para consultar e definir o nível de volume de dispositivos de saída de wave-áudio.</span><span class="sxs-lookup"><span data-stu-id="d813e-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="d813e-110">Função</span><span class="sxs-lookup"><span data-stu-id="d813e-110">Function</span></span>                                     | <span data-ttu-id="d813e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d813e-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d813e-112">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="d813e-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="d813e-113">Recupera o nível de volume atual do dispositivo de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="d813e-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="d813e-114">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="d813e-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="d813e-115">Define o nível de volume do dispositivo de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="d813e-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="d813e-116">Nem todos os dispositivos de wave-áudio dão suporte a alterações de volume.</span><span class="sxs-lookup"><span data-stu-id="d813e-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="d813e-117">Alguns dispositivos dão suporte ao controle de volume individual nos canais esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="d813e-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="d813e-118">Para obter informações sobre como determinar os recursos de controle de volume dos dispositivos de formato de onda-áudio, consulte [dispositivos e tipos de dados](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="d813e-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="d813e-119">Alguns aplicativos permitem que o usuário controle o volume de todos os dispositivos de áudio em um sistema.</span><span class="sxs-lookup"><span data-stu-id="d813e-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="d813e-120">(Muitos aplicativos desse tipo usam os serviços de mixer de áudio; para obter mais informações, consulte [mixers de áudio](audio-mixers.md).) A menos que seu aplicativo seja capaz desse tipo de controle de volume mestre, você deve abrir um dispositivo de áudio antes de alterar seu volume.</span><span class="sxs-lookup"><span data-stu-id="d813e-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="d813e-121">Você também deve consultar o nível de volume antes de alterá-lo e restaurar o nível de volume para seu nível anterior assim que possível.</span><span class="sxs-lookup"><span data-stu-id="d813e-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="d813e-122">O volume é especificado em um valor doubleword.</span><span class="sxs-lookup"><span data-stu-id="d813e-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="d813e-123">Quando o formato de áudio é estéreo, os 16 bits superiores especificam o volume relativo do canal correto e os 16 bits inferiores especificam o volume relativo do canal esquerdo.</span><span class="sxs-lookup"><span data-stu-id="d813e-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="d813e-124">Para dispositivos que não dão suporte ao controle de volume de canal esquerdo e direito, os 16 bits inferiores especificam o nível de volume e os 16 bits superiores são ignorados.</span><span class="sxs-lookup"><span data-stu-id="d813e-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="d813e-125">Os valores de nível de volume variam de 0x0 (silêncio) a 0xFFFF (volume máximo) e são interpretados logaritmicamente.</span><span class="sxs-lookup"><span data-stu-id="d813e-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="d813e-126">O aumento do volume percebido é o mesmo ao aumentar o nível de volume de 0x5000 para 0x6000, pois ele é de 0x4000 para 0x5000.</span><span class="sxs-lookup"><span data-stu-id="d813e-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 