---
title: MCI_RECORD comando (mmsystem. h)
description: O \_ comando de registro MCI inicia a gravação a partir da posição atual ou de um local especificado para outro local especificado.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Multimídia do Windows de comando MCI_RECORD
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085666"
---
# <a name="mci_record-command"></a><span data-ttu-id="da1ca-104">\_Comando de registro MCI</span><span class="sxs-lookup"><span data-stu-id="da1ca-104">MCI\_RECORD command</span></span>

<span data-ttu-id="da1ca-105">O comando de [**\_ registro MCI**](mci-record-parms.md) inicia a gravação a partir da posição atual ou de um local especificado para outro local especificado.</span><span class="sxs-lookup"><span data-stu-id="da1ca-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="da1ca-106">Os dispositivos VCR e Wave-Audio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="da1ca-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="da1ca-107">Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.</span><span class="sxs-lookup"><span data-stu-id="da1ca-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="da1ca-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="da1ca-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="da1ca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da1ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1ca-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="da1ca-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="da1ca-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="da1ca-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="da1ca-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="da1ca-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="da1ca-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span><span class="sxs-lookup"><span data-stu-id="da1ca-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros de registro MCI**](mci-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="da1ca-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="da1ca-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="da1ca-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1ca-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="da1ca-118">Return Value</span></span>

<span data-ttu-id="da1ca-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="da1ca-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1ca-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="da1ca-120">Remarks</span></span>

<span data-ttu-id="da1ca-121">Esse comando tem suporte em dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI \_ pode \_ gravar sinalizador.</span><span class="sxs-lookup"><span data-stu-id="da1ca-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="da1ca-122">Para o driver MCIWAVE, todos os dados gravados após a abertura de um arquivo serão descartados se o arquivo for fechado sem salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="da1ca-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="da1ca-123">Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte ao \_ registro MCI:</span><span class="sxs-lookup"><span data-stu-id="da1ca-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="da1ca-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="da1ca-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-125">Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="da1ca-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="da1ca-126">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="da1ca-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="da1ca-127">Se \_ o MCI de não for especificado, o local inicial padrão será a posição atual.</span><span class="sxs-lookup"><span data-stu-id="da1ca-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_inserção de registro de MCI \_</span><span class="sxs-lookup"><span data-stu-id="da1ca-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-129">As informações registradas recentemente devem ser inseridas ou coladas nos dados existentes.</span><span class="sxs-lookup"><span data-stu-id="da1ca-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="da1ca-130">Alguns dispositivos podem não dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="da1ca-130">Some devices might not support this.</span></span> <span data-ttu-id="da1ca-131">Se houver suporte, esse será o padrão.</span><span class="sxs-lookup"><span data-stu-id="da1ca-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_substituição de registro de MCI \_</span><span class="sxs-lookup"><span data-stu-id="da1ca-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-133">Os dados devem substituir os dados existentes.</span><span class="sxs-lookup"><span data-stu-id="da1ca-133">Data should overwrite existing data.</span></span> <span data-ttu-id="da1ca-134">O MCIWAVE. O dispositivo DRV retorna MCIERR \_ função sem suporte \_ em resposta a esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="da1ca-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="da1ca-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-136">Um local final é incluído no membro **dwTo** da estrutura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="da1ca-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="da1ca-137">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="da1ca-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="da1ca-138">Se \_ o MCI para não for especificado, o local final será padronizado para o final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="da1ca-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="da1ca-139">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="da1ca-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="da1ca-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_fluxo de \_ áudio de gravação de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="da1ca-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-141">Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="da1ca-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="da1ca-142">Se você omitir esse sinalizador, os dados de áudio serão registrados no primeiro fluxo físico.</span><span class="sxs-lookup"><span data-stu-id="da1ca-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_retenção de \_ registro de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="da1ca-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-144">Quando a gravação for interrompida, a tela conterá a última imagem e não continuará mostrando o vídeo até que um comando de [ \_ Monitor MCI](mci-monitor.md) seja emitido.</span><span class="sxs-lookup"><span data-stu-id="da1ca-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_fluxo de \_ vídeo de registro DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="da1ca-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-146">Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="da1ca-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="da1ca-147">Se você omitir esse sinalizador, os dados de vídeo serão registrados no primeiro fluxo físico.</span><span class="sxs-lookup"><span data-stu-id="da1ca-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="da1ca-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-149">Um retângulo é especificado no membro **RC** da estrutura identificada por *lpRecord*.</span><span class="sxs-lookup"><span data-stu-id="da1ca-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="da1ca-150">O retângulo especifica a região da entrada externa usada como a origem dos pixels compactados e salvos.</span><span class="sxs-lookup"><span data-stu-id="da1ca-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="da1ca-151">Esse retângulo assume como padrão o retângulo especificado (ou padronizado) pelo sinalizador de \_ vídeo MCI DGV \_ Put \_ para o comando [MCI \_ Put](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="da1ca-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="da1ca-152">Quando ele é definido de forma diferente do que o retângulo do vídeo, o que é exibido não é o que é gravado</span><span class="sxs-lookup"><span data-stu-id="da1ca-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="da1ca-153">Para dispositivos de vídeo digital, o *lpRecord* aponta para uma estrutura de [**\_ \_ \_ parâmetros de registro DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .</span><span class="sxs-lookup"><span data-stu-id="da1ca-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="da1ca-154">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="da1ca-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="da1ca-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_ \_ registro de VCR MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="da1ca-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-156">O membro **dwAt** da estrutura identificada por *lpRecord* contém uma hora em que o comando inteiro começa, ou se o dispositivo for cued, quando o dispositivo atingir a posição from fornecida pelo comando cue.</span><span class="sxs-lookup"><span data-stu-id="da1ca-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="da1ca-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_inicialização de \_ registro de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="da1ca-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="da1ca-158">Busque o dispositivo até o início da mídia, comece a gravar vídeo e áudio em branco e registre o código de ponto de inicio, se possível.</span><span class="sxs-lookup"><span data-stu-id="da1ca-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="da1ca-159">Para dispositivos VCR, o *lpRecord* aponta para uma estrutura de parâmetros de [**registro de \_ VCR \_ \_ MCI**](mci-vcr-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="da1ca-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1ca-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1ca-160">Requirements</span></span>



| <span data-ttu-id="da1ca-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1ca-161">Requirement</span></span> | <span data-ttu-id="da1ca-162">Valor</span><span class="sxs-lookup"><span data-stu-id="da1ca-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1ca-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da1ca-163">Minimum supported client</span></span><br/> | <span data-ttu-id="da1ca-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da1ca-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da1ca-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da1ca-165">Minimum supported server</span></span><br/> | <span data-ttu-id="da1ca-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da1ca-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da1ca-167">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="da1ca-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="da1ca-168"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da1ca-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1ca-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="da1ca-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1ca-170">MCI</span><span class="sxs-lookup"><span data-stu-id="da1ca-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="da1ca-171">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="da1ca-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

