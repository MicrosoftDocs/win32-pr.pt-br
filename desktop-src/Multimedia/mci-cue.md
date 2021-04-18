---
title: MCI_CUE comando (mmsystem. h)
description: O \_ comando de indicação MCI indicações de um dispositivo para que a reprodução ou a gravação comece com o atraso mínimo. Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- Multimídia do Windows de comando MCI_CUE
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766375"
---
# <a name="mci_cue-command"></a><span data-ttu-id="7174d-105">\_Comando de indicação MCI</span><span class="sxs-lookup"><span data-stu-id="7174d-105">MCI\_CUE command</span></span>

<span data-ttu-id="7174d-106">O \_ comando de indicação MCI indicações de um dispositivo para que a reprodução ou a gravação comece com o atraso mínimo.</span><span class="sxs-lookup"><span data-stu-id="7174d-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="7174d-107">Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="7174d-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="7174d-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="7174d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="7174d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7174d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7174d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7174d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7174d-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="7174d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7174d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7174d-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="7174d-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="7174d-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7174d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7174d-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span><span class="sxs-lookup"><span data-stu-id="7174d-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="7174d-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7174d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="7174d-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="7174d-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7174d-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7174d-118">Return Value</span></span>

<span data-ttu-id="7174d-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="7174d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7174d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7174d-120">Remarks</span></span>

<span data-ttu-id="7174d-121">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="7174d-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7174d-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_entrada de \_ indicação MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="7174d-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="7174d-123">Uma instância de vídeo digital deve se preparar para a gravação.</span><span class="sxs-lookup"><span data-stu-id="7174d-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="7174d-124">Se o aplicativo não tiver espaço em disco reservado, o dispositivo reservará o espaço em disco usando seus parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="7174d-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="7174d-125">O aplicativo pode omitir esse sinalizador se a fonte da apresentação atual já for a entrada externa.</span><span class="sxs-lookup"><span data-stu-id="7174d-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="7174d-126">(Esse sinalizador não tem efeito na seleção da origem da apresentação.)</span><span class="sxs-lookup"><span data-stu-id="7174d-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="7174d-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>\_DGV da \_ pista do MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="7174d-128">Uma instância de vídeo digital deve se preparar para reproduzir o quadro especificado com o comando sem exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="7174d-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="7174d-129">Quando esse sinalizador é especificado, a exibição continua a mostrar a imagem no buffer de quadro, embora seu quadro correspondente não seja a posição atual.</span><span class="sxs-lookup"><span data-stu-id="7174d-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="7174d-130">Por exemplo, se o buffer de quadros contiver a imagem do quadro 7, o dispositivo continuará a mostrar o quadro 7 quando esse sinalizador for usado para marcar o dispositivo para qualquer outra posição.</span><span class="sxs-lookup"><span data-stu-id="7174d-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="7174d-131">Um comando de indicação subsequente sem esse sinalizador e sem o MCI \_ para sinalizar exibe o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="7174d-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>\_saída de \_ indicação MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="7174d-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="7174d-133">Uma instância de vídeo digital deve se preparar para a execução.</span><span class="sxs-lookup"><span data-stu-id="7174d-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="7174d-134">Se o espaço de trabalho estiver em pausa, nenhum posicionamento ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="7174d-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="7174d-135">Se o espaço de trabalho for interrompido, a posição poderá mudar para uma imagem de quadro chave anterior.</span><span class="sxs-lookup"><span data-stu-id="7174d-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="7174d-136">O aplicativo pode omitir esse sinalizador se a fonte da apresentação atual já for o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7174d-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="7174d-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="7174d-138">Uma posição de espaço de trabalho é incluída no membro **dwTo** da estrutura identificada por *lpCue*.</span><span class="sxs-lookup"><span data-stu-id="7174d-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="7174d-139">As unidades atribuídas aos valores de posição são especificadas usando \_ o \_ \_ sinalizador de formato de tempo MCI set do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="7174d-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="7174d-140">Isso é equivalente a procurar uma posição, exceto que o dispositivo é pausado após o comando.</span><span class="sxs-lookup"><span data-stu-id="7174d-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="7174d-141">Para dispositivos **DigitalVideo** , o parâmetro *lpCue* aponta para uma estrutura de [**parâmetros MCI do \_ DGV \_ Cue \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .</span><span class="sxs-lookup"><span data-stu-id="7174d-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="7174d-142">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="7174d-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7174d-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="7174d-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="7174d-144">O membro **dwFrom** da estrutura apontada por *lpCue* contém o local inicial especificado no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="7174d-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="7174d-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="7174d-146">O membro **dwTo** da estrutura apontada por *lpCue* contém o local final (pausando) especificado no formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="7174d-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_entrada de \_ indicação de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="7174d-148">Prepare-se para a gravação.</span><span class="sxs-lookup"><span data-stu-id="7174d-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_saída de \_ pista de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="7174d-150">Prepare-se para jogar.</span><span class="sxs-lookup"><span data-stu-id="7174d-150">Prepare for playing.</span></span> <span data-ttu-id="7174d-151">Se nenhuma \_ \_ entrada de sinalização de VCR MCI \_ ou \_ \_ saída de sinal de VCR MCI \_ for especificada, a \_ saída de sinalização de VCR MCI \_ \_ será assumida.</span><span class="sxs-lookup"><span data-stu-id="7174d-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>preversão de \_ \_ sinalização de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="7174d-153">Marque o dispositivo para a posição atual ou a posição **dwFrom** , menos a duração de preversão.</span><span class="sxs-lookup"><span data-stu-id="7174d-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="7174d-154">Isso permitirá que o dispositivo se prepare antes de inserir o modo de gravação ou de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7174d-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>inversão de \_ \_ sinalização de videocassete MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7174d-156">A direção do comando de próxima reprodução ou de registro é inversa.</span><span class="sxs-lookup"><span data-stu-id="7174d-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="7174d-157">Quando advertência para reprodução usando o comando de \_ indicação MCI com o \_ sinalizador de \_ saída MCI de sinalização de videocassete \_ , você pode cancelar \_ a indicação de MCI emitindo o comando de [ \_ reprodução MCI](mci-play.md) com MCI \_ de, MCI \_ para ou MCI de \_ reprodução de VCR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7174d-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="7174d-158">Quando advertência para gravação usando \_ a indicação MCI com o \_ sinalizador de entrada de sinalização de videocassete MCI \_ \_ , você pode cancelar \_ a indicação de MCI emitindo o comando de [ \_ registro MCI](mci-record.md) com a \_ inicialização do registro MCI de, MCI \_ para ou MCI \_ VCR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7174d-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="7174d-159">Para dispositivos **VCR** , o parâmetro *lpCue* aponta para uma estrutura de [**\_ \_ \_ parâmetros de sinalização VCR MCI**](mci-vcr-cue-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7174d-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="7174d-160">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="7174d-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7174d-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="7174d-162">Um dispositivo de entrada de wave-áudio deve ser cued.</span><span class="sxs-lookup"><span data-stu-id="7174d-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="7174d-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_</span><span class="sxs-lookup"><span data-stu-id="7174d-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="7174d-164">Um dispositivo de saída de wave-áudio deve ser cued.</span><span class="sxs-lookup"><span data-stu-id="7174d-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="7174d-165">Esse será o sinalizador padrão se um sinalizador não for especificado.</span><span class="sxs-lookup"><span data-stu-id="7174d-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7174d-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7174d-166">Requirements</span></span>



| <span data-ttu-id="7174d-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="7174d-167">Requirement</span></span> | <span data-ttu-id="7174d-168">Valor</span><span class="sxs-lookup"><span data-stu-id="7174d-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7174d-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7174d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="7174d-170">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7174d-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7174d-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7174d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="7174d-172">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7174d-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7174d-173">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7174d-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="7174d-174"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7174d-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7174d-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="7174d-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7174d-176">MCI</span><span class="sxs-lookup"><span data-stu-id="7174d-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7174d-177">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="7174d-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

