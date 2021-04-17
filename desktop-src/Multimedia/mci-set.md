---
title: MCI_SET comando (mmsystem. h)
description: O \_ comando set do MCI define as informações do dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Multimídia do Windows de comando MCI_SET
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105766374"
---
# <a name="mci_set-command"></a><span data-ttu-id="f3eb3-105">Comando de definição do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="f3eb3-106">Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="f3eb3-107">Neste documento, há referências à palavra ' escravo '.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="f3eb3-108">O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="f3eb3-109">Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="f3eb3-110">Para fins de consistência, este documento contém esta palavra.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="f3eb3-111">Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="f3eb3-112">O \_ comando set do MCI define as informações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="f3eb3-113">CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="f3eb3-114">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="f3eb3-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3eb3-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f3eb3-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-117">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f3eb3-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-119">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="f3eb3-120">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f3eb3-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span><span class="sxs-lookup"><span data-stu-id="f3eb3-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-122">Ponteiro para uma estrutura de [**\_ \_ parâmetros do MCI Set**](mci-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="f3eb3-123">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="f3eb3-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3eb3-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f3eb3-124">Return Value</span></span>

<span data-ttu-id="f3eb3-125">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3eb3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3eb3-126">Remarks</span></span>

<span data-ttu-id="f3eb3-127">Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte ao conjunto de MCI \_ :</span><span class="sxs-lookup"><span data-stu-id="f3eb3-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>\_áudio definido por MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-129">Um número de canal de áudio é incluído no membro dwAudio da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-130">Esse sinalizador deve ser usado com o MCI \_ definido \_ como ativado ou MCI \_ definido como \_ off.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="f3eb3-131">Use uma das seguintes constantes para indicar o número do canal:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>o MCI \_ definir \_ áudio \_ tudo</span><span class="sxs-lookup"><span data-stu-id="f3eb3-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-133">Todos os canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ definir \_ áudio \_ restante</span><span class="sxs-lookup"><span data-stu-id="f3eb3-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-135">Canal esquerdo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ definir \_ áudio \_ à direita</span><span class="sxs-lookup"><span data-stu-id="f3eb3-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-137">Canal direito.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>porta do conjunto do MCI \_ \_ \_ fechada</span><span class="sxs-lookup"><span data-stu-id="f3eb3-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-139">Fecha a cobertura de mídia (se houver).</span><span class="sxs-lookup"><span data-stu-id="f3eb3-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>porta do conjunto do MCI \_ \_ \_ aberta</span><span class="sxs-lookup"><span data-stu-id="f3eb3-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-141">Abre a tampa de mídia (se houver).</span><span class="sxs-lookup"><span data-stu-id="f3eb3-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="f3eb3-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-143">Desabilita o vídeo ou o canal de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="f3eb3-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-145">Habilita o vídeo ou o canal de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_formato de \_ hora \_ definido do MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-147">Um parâmetro de formato de hora é incluído no membro **dwTimeFormat** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-148">Os sinalizadores a seguir são usados com este sinalizador:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_bytes de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-150">Em um formato de dados PCM (modulação de código de pulso), o altera a descrição do membro de tempo para bytes para entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="f3eb3-151">Reconhecido pelo tipo de dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_quadros de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-153">Os comandos subsequentes usarão quadros.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="f3eb3-154">Reconhecido pelos tipos de dispositivo **DigitalVideo**, **VCR** e **VIDEODISC** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_formato MCI \_ HMS</span><span class="sxs-lookup"><span data-stu-id="f3eb3-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-156">Altera o formato de hora para horas, minutos e segundos.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="f3eb3-157">Reconhecido pelos tipos de dispositivo **VCR** e **VIDEODISC** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>\_milissegundos do formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-159">Altera o formato de hora para milissegundos.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="f3eb3-160">Reconhecido por todos os tipos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="f3eb3-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-162">Altera o formato de hora para minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="f3eb3-163">Reconhecido pelos tipos de dispositivo **cdaudio** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_exemplos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-165">Altera o formato de hora para exemplos de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="f3eb3-166">Reconhecido pelo tipo de dispositivo **WaveAudio** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Formato MCI \_ SMPTE \_ 24, \_ formato MCI \_ SMPTE \_ 25 e formato MCI \_ \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="f3eb3-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-168">Define o formato de hora como 24, 25 e 30 quadros SMPTE (sociedade de imagem de movimento e engenheiros de televisão), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="f3eb3-169">Reconhecido pelos tipos de dispositivo **Sequencer** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Formato MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="f3eb3-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-171">Define o formato de hora para 30 quadros de distribuição SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="f3eb3-172">Reconhecido pelos tipos de dispositivo **Sequencer** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="f3eb3-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-174">Altera o formato de hora para faixas, minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="f3eb3-175">(O MCI usa números de faixa contínuos.) Reconhecido pelos tipos de dispositivo **cdaudio** e **VCR** .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_vídeo de conjunto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-177">Define ou desativa o sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-177">Sets the video signal on or off.</span></span> <span data-ttu-id="f3eb3-178">Esse sinalizador deve ser usado com o MCI \_ definido \_ como ativado ou MCI \_ definido como \_ off.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="f3eb3-179">Dispositivos que não têm vídeo de retorno MCIERR \_ função sem suporte \_ .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="f3eb3-180">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="f3eb3-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>DGV do MCI \_ \_ definir \_ FileFormat</span><span class="sxs-lookup"><span data-stu-id="f3eb3-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-182">Um parâmetro de formato de arquivo é incluído no membro **dwFileFormat** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-183">Para dispositivos de vídeo digital, o formato de arquivo é usado para salvar ou capturar comandos.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="f3eb3-184">Se omitido, isso pode padronizar para um formato definido por driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="f3eb3-185">Se o formato de arquivo especificado estiver em conflito com o algoritmo e a qualidade selecionados no momento, eles serão alterados para os padrões para o formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="f3eb3-186">As seguintes constantes de formato de arquivo são definidas:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ avi</span><span class="sxs-lookup"><span data-stu-id="f3eb3-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-188">Formato AVI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS</span><span class="sxs-lookup"><span data-stu-id="f3eb3-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-190">Formato AVSS.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB</span><span class="sxs-lookup"><span data-stu-id="f3eb3-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-192">Formato DIB.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF</span><span class="sxs-lookup"><span data-stu-id="f3eb3-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-194">Formato JFIF.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="f3eb3-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-196">Formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="f3eb3-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-198">Formato MPEG.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB</span><span class="sxs-lookup"><span data-stu-id="f3eb3-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-200">Formato de DIB RLE.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG</span><span class="sxs-lookup"><span data-stu-id="f3eb3-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-202">Formato RJPEG.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI \_ DGV \_ definir \_ busca \_ exata</span><span class="sxs-lookup"><span data-stu-id="f3eb3-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-204">Define o formato usado para posicionamento.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-204">Sets the format used for positioning.</span></span> <span data-ttu-id="f3eb3-205">Esse sinalizador deve ser usado com o MCI \_ definido \_ como ativado ou MCI \_ definido como \_ off.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="f3eb3-206">Se \_ o MCI definido \_ em for especificado, executar ou gravar precisamente acessará o quadro especificado com o \_ sinalizador MCI de.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="f3eb3-207">Isso pode adicionar um atraso extra se o quadro solicitado não for um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="f3eb3-208">Se \_ o MCI definido \_ como OFF for especificado, o dispositivo buscará uma imagem de quadro-chave que precede o quadro solicitado.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="f3eb3-209">Para alguns arquivos e dispositivos, esse pode ser o primeiro quadro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="f3eb3-210">O padrão para esse sinalizador depende do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_velocidade do \_ conjunto de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-212">Um parâmetro Speed é incluído no membro **dwSpeed** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-213">A velocidade é especificada como uma proporção entre a taxa de quadros nominal e a taxa de quadros desejada, em que a taxa de quadros nominal é designada como 1000.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="f3eb3-214">Meia velocidade é 500 e a velocidade dupla é 2000.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="f3eb3-215">O intervalo de velocidade permitido depende do dispositivo e possivelmente do arquivo também.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_DGV MCI \_ set \_ ainda</span><span class="sxs-lookup"><span data-stu-id="f3eb3-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-217">Quando usado com o MCI \_ DGV \_ set \_ FileFormat, \_ o MCI set define o formato de arquivo usado para comandos de captura.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="f3eb3-218">Para dispositivos de vídeo digital, o parâmetro *lpSet* aponta para uma [**estrutura \_ DGV MCI \_ set \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="f3eb3-219">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **Sequencer** :</span><span class="sxs-lookup"><span data-stu-id="f3eb3-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>\_formato de Seq MCI \_ \_ SONGPTR</span><span class="sxs-lookup"><span data-stu-id="f3eb3-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-221">Define o formato de hora para as unidades de ponteiro de música.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_mestre de \_ conjunto de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-223">Define o Sequencer como uma fonte de dados de sincronização e indica que o tipo de sincronização é especificado no membro **dwMaster** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-224">MCISEQ retorna MCIERR \_ função sem suporte \_ .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="f3eb3-225">As constantes a seguir são definidas para o tipo de sincronização:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ Midi</span><span class="sxs-lookup"><span data-stu-id="f3eb3-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-227">O Sequencer enviará dados de sincronização de formato MIDI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="f3eb3-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-229">O Sequencer enviará dados de sincronização de formato SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_Seq MCI \_ None</span><span class="sxs-lookup"><span data-stu-id="f3eb3-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-231">O sequenciador não enviará dados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>\_deslocamento do \_ conjunto de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-233">Altera o deslocamento SMPTE de uma sequência para aquela especificada pelo membro **dwOffset** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-234">Isso afeta apenas as sequências com um tipo de divisão SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_porta do \_ conjunto de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-236">Define a porta MIDI de saída de uma sequência para aquela especificada pelo identificador de dispositivo MIDI no membro **dwPort** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-237">O dispositivo fecha a porta anterior (se houver) e tenta abrir e usar a nova porta.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="f3eb3-238">Se falhar, ele retornará um erro e reabrirá a porta usada anteriormente (se houver).</span><span class="sxs-lookup"><span data-stu-id="f3eb3-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="f3eb3-239">As constantes a seguir são definidas para as portas:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_Seq MCI \_ None</span><span class="sxs-lookup"><span data-stu-id="f3eb3-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-241">Fecha a porta usada anteriormente (se houver).</span><span class="sxs-lookup"><span data-stu-id="f3eb3-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="f3eb3-242">O Sequencer se comporta exatamente como se uma porta estivesse aberta, exceto que nenhuma mensagem MIDI é enviada.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_mapeador de Midi</span><span class="sxs-lookup"><span data-stu-id="f3eb3-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-244">Define a porta aberta para o mapeador de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>\_slave do \_ conjunto de Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-246">Define o Sequencer para receber dados de sincronização e indica que o tipo de sincronização é especificado no membro **dwSlave** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-247">MCISEQ retorna MCIERR \_ função sem suporte \_ .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="f3eb3-248">As constantes a seguir são definidas para o tipo de sincronização:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_arquivo Seq \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-250">Define o Sequencer para receber dados de sincronização contidos no arquivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ Midi</span><span class="sxs-lookup"><span data-stu-id="f3eb3-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-252">Define o Sequencer para receber dados de sincronização de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_Seq MCI \_ None</span><span class="sxs-lookup"><span data-stu-id="f3eb3-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-254">Define o Sequencer para ignorar os dados de sincronização em um fluxo de MIDI.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="f3eb3-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-256">Define o Sequencer para receber dados de sincronização do SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_tempo de \_ definição do Seq MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-258">Altera o tempo da sequência de MIDI para o especificado pelo membro **dwTempo** da estrutura apontada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="f3eb3-259">Para sequências com o tipo de divisão PPQN, o tempo é especificado em batidas por minuto; para sequências com o tipo de divisão SMPTE, o tempo é especificado em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="f3eb3-260">Para dispositivos do Sequencer, o parâmetro *lpSet* aponta para uma estrutura de [**parâmetros de \_ \_ conjunto \_ de Seq MCI**](mci-seq-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="f3eb3-261">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="f3eb3-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_registro de \_ montagem de conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-263">Define o dispositivo a ser gravado nos modos de montagem ou inserção (quando assemble está desativado, INSERT é on e vice-versa).</span><span class="sxs-lookup"><span data-stu-id="f3eb3-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="f3eb3-264">Use com um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="f3eb3-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-266">Define o registro de montagem ativado e ativa o registro de inserção.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="f3eb3-267">Registra todas as faixas de vídeo, áudio e código de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="f3eb3-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-269">Define o registro de montagem como off e ativa o registro de inserção.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="f3eb3-270">Quando o registro de montagem está desativado, faixas individuais de vídeo, áudio e código de pafica podem ser selecionadas para gravação.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_relógio de \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-272">O membro **dwClock** da estrutura identificada por *lpSet* contém o novo horário do relógio.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>\_contador de \_ conjunto de VCR \_ MCI forma \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-274">O membro **dwCounterFormat** da estrutura identificada por *lpSet* contém uma constante especificando o novo formato de hora do contador a ser usado pelo contador de status.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="f3eb3-275">Para obter uma lista de constantes válidas, \_ consulte \_ formato de hora Set MCI \_ na lista de sinalizadores adicionais para este comando.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_valor do \_ contador do conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-277">O membro **dwCounterValue** da estrutura identificada por *lpSet* contém o novo valor do contador.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_índice de \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-279">O membro **dwIndex** da estrutura identificada por *lpSet* contém uma constante que indica o conteúdo da exibição na tela e deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_contador de \_ índice de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-281">Exibe o contador.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_data do \_ índice de VCR do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-283">Exibe a data.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_tempo de \_ índice de VCR do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-285">Exibe a hora.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>código de meio do \_ índice de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-287">Exibe o código de code.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-287">Displays timecode.</span></span>

<span data-ttu-id="f3eb3-288">Para obter mais informações, consulte o comando de [ \_ índice MCI](mci-index.md) .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_ \_ \_ tempo limite de pausa de set de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-290">O membro **dwPauseTimeout** da estrutura identificada por *lpSet* contém a duração máxima, em milissegundos, de um comando PAUSE.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>duração do registro do VCR do MCI \_ \_ definido \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-292">O membro **dwPostrollDuration** da estrutura identificada por *lpSet* contém o comprimento da fita de vídeo, no formato de hora atual, necessário para finalizar o transporte de videocassete quando um comando Stop ou PAUSE é emitido.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_potência do \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-294">Define ou desativa a ativação.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-294">Sets the power on or off.</span></span> <span data-ttu-id="f3eb3-295">Deve ser usado com um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="f3eb3-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-297">Desliga o desligamento.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="f3eb3-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-299">Ativa a ativação.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_duração da \_ preversão do conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-301">O membro **dwPrerollDuration** da estrutura identificada por *lpSet* contém o comprimento da fita de vídeo, no formato de hora atual, necessário para estabilizar a saída do VCR.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_formato de \_ registro do conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-303">O membro **dwRecordFormat** da estrutura identificada por *lpSet* contém uma constante que descreve a velocidade do registro, que deve ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_EP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-305">Registros em velocidade lenta.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_formato de videocassete MCI \_ \_ LP</span><span class="sxs-lookup"><span data-stu-id="f3eb3-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-307">Registros em velocidade média-lenta.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_SP de \_ formato \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-309">Registros na velocidade padrão.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_velocidade do \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-311">O membro **dwSpeed** da estrutura identificada por *lpSet* contém a nova configuração de velocidade, em que 1000 é velocidade normal, 2000 é de velocidade dupla e 500 é meia velocidade e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_tamanho da \_ fita do conjunto de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-313">O membro **dwTapeLength** da estrutura identificada por *lpSet* contém o novo comprimento da fita, desde que o comprimento da fita não seja detectável.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>\_modo de \_ \_ tempo definido de VCR \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-315">O membro **dwTimeMode** da estrutura identificada por *lpSet* contém uma constante que indica o novo modo de tempo posicional.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="f3eb3-316">As seguintes constantes são válidas:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-318">Força o dispositivo a usar o contador exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_detecção de \_ tempo de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-320">Cada vez que uma nova fita de vídeo é inserida no dispositivo ou o modo é alterado de não pronto para pronto, o dispositivo deve tentar determinar se há um código de tempo disponível na fita de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="f3eb3-321">Se o código de indisponibilidade estiver disponível, use o código de sob todos os comandos subsequentes que especificam posições.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="f3eb3-322">Caso contrário, use o contador.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>tempo de vida de \_ hora do VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-324">Força o dispositivo a usar o código de Code exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_controle de \_ conjunto de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-326">Ajusta a velocidade do transporte de fita do VCR com um ajuste fino e deve ser usado com um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_VCR MCI \_ Plus</span><span class="sxs-lookup"><span data-stu-id="f3eb3-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-328">Aumenta a velocidade de transporte de fita.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>subtração de \_ VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-330">Diminui a velocidade de transporte de fita.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>redefinição de \_ VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-332">Retorna o ajuste de controle para zero.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="f3eb3-333">Para dispositivos VCR, o parâmetro *lpSet* aponta para uma estrutura de [**conjunto de \_ \_ \_ parâmetros do VCR MCI**](mci-vcr-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="f3eb3-334">O seguinte sinalizador adicional é usado com o tipo de dispositivo **VIDEODISC** :</span><span class="sxs-lookup"><span data-stu-id="f3eb3-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_faixa de \_ formato de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-336">Altera o formato de hora para faixas.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-336">Changes the time format to tracks.</span></span> <span data-ttu-id="f3eb3-337">O MCI usa números de faixa contínuos.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="f3eb3-338">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="f3eb3-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="f3eb3-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-340">Define a entrada usada para gravar no membro **wInput** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-342">Define a saída usada para reproduzir o membro **wOutput** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>ANYINPUT de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-344">Qualquer entrada de onda compatível com o formato atual pode ser usada para gravação.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>ANYOUTPUT de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-346">Qualquer saída de Wave compatível com o formato atual pode ser usada para reprodução.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>AVGBYTESPERSEC de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-348">Define os bytes por segundo usados para reproduzir, gravar e salvar no membro **nAvgBytesPerSec** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>BITSPERSAMPLE de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-350">Define os bits por exemplo usado para reproduzir, gravar e salvar no membro **nBitsPerSample** do formato de dados PCM identificado por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>BLOCKALIGN de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-352">Define o alinhamento de bloco usado para reproduzir, gravar e salvar no membro **nBlockAlign** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_canais de \_ conjunto de ondas MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-354">O número de canais é indicado no membro **nChannels** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>FORMATTAG de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-356">Define o tipo de formato usado para reproduzir, gravar e salvar no membro **wFormatTag** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="f3eb3-357">Especificar \_ o formato Wave \_ PCM altera o formato para PCM.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb3-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>SAMPLESPERSEC de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="f3eb3-359">Define os exemplos por segundo usados para reproduzir, gravar e salvar no membro **nSamplesPerSec** da estrutura identificada por *lpSet*.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="f3eb3-360">Para dispositivos de formato de onda-áudio, o parâmetro *lpSet* aponta para uma estrutura [**MCI do \_ tipo Wave \_ set \_ parms**](mci-wave-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f3eb3-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="f3eb3-361">Várias propriedades dos dados de formato de onda-áudio são definidas quando o arquivo para armazenar os dados é criado.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="f3eb3-362">Essas propriedades descrevem como os dados são estruturados dentro do arquivo e não podem ser alterados após o início da gravação.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="f3eb3-363">A lista de sinalizadores a seguir identifica essas propriedades:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="f3eb3-364">AVGBYTESPERSEC de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="f3eb3-365">BITSPERSAMPLE de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="f3eb3-366">BLOCKALIGN de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="f3eb3-367">\_canais de \_ conjunto de ondas MCI \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="f3eb3-368">FORMATTAG de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="f3eb3-369">SAMPLESPERSEC de onda do MCI \_ \_ set \_</span><span class="sxs-lookup"><span data-stu-id="f3eb3-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eb3-370">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3eb3-370">Requirements</span></span>



| <span data-ttu-id="f3eb3-371">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eb3-371">Requirement</span></span> | <span data-ttu-id="f3eb3-372">Valor</span><span class="sxs-lookup"><span data-stu-id="f3eb3-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eb3-373">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3eb3-373">Minimum supported client</span></span><br/> | <span data-ttu-id="f3eb3-374">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3eb3-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f3eb3-375">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3eb3-375">Minimum supported server</span></span><br/> | <span data-ttu-id="f3eb3-376">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3eb3-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3eb3-377">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f3eb3-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3eb3-378"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3eb3-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3eb3-379">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3eb3-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eb3-380">MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f3eb3-381">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f3eb3-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

