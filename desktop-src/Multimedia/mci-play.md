---
title: MCI_PLAY comando (mmsystem. h)
description: O \_ comando MCI Play sinaliza o dispositivo para começar a transmitir dados de saída. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Multimídia do Windows de comando MCI_PLAY
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824824"
---
# <a name="mci_play-command"></a><span data-ttu-id="ee975-105">\_Comando de reprodução MCI</span><span class="sxs-lookup"><span data-stu-id="ee975-105">MCI\_PLAY command</span></span>

<span data-ttu-id="ee975-106">O \_ comando MCI Play sinaliza o dispositivo para começar a transmitir dados de saída.</span><span class="sxs-lookup"><span data-stu-id="ee975-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="ee975-107">CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="ee975-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="ee975-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee975-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="ee975-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee975-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee975-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ee975-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ee975-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="ee975-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ee975-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ee975-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="ee975-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="ee975-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ee975-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee975-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span><span class="sxs-lookup"><span data-stu-id="ee975-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="ee975-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros de reprodução MCI**](mci-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ee975-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="ee975-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="ee975-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee975-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ee975-118">Return Value</span></span>

<span data-ttu-id="ee975-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ee975-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee975-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee975-120">Remarks</span></span>

<span data-ttu-id="ee975-121">Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte a \_ reprodução MCI:</span><span class="sxs-lookup"><span data-stu-id="ee975-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="ee975-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="ee975-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="ee975-123">Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="ee975-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="ee975-124">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ee975-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="ee975-125">Se \_ o MCI de não for especificado, o local inicial padrão será a posição atual.</span><span class="sxs-lookup"><span data-stu-id="ee975-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="ee975-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ee975-127">Um local final é incluído no membro **dwTo** da estrutura identificada por *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="ee975-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="ee975-128">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ee975-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="ee975-129">Se \_ o MCI para não for especificado, o local final será padronizado para o final da mídia.</span><span class="sxs-lookup"><span data-stu-id="ee975-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="ee975-130">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="ee975-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ee975-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_repetição de \_ reprodução de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee975-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="ee975-132">A reprodução deve iniciar novamente no início quando o final do conteúdo for atingido.</span><span class="sxs-lookup"><span data-stu-id="ee975-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>reversão do MCI \_ DGV \_ reproduzir \_</span><span class="sxs-lookup"><span data-stu-id="ee975-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ee975-134">A reprodução deve ocorrer em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="ee975-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>janela de reprodução do MCI \_ Mciavi \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee975-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="ee975-136">A reprodução deve ocorrer na janela associada a uma instância de dispositivo (o padrão).</span><span class="sxs-lookup"><span data-stu-id="ee975-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="ee975-137">(Esse sinalizador é específico do MCIAVI. DRV.)</span><span class="sxs-lookup"><span data-stu-id="ee975-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="ee975-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>tela de execução do MCI \_ Mciavi \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee975-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="ee975-139">A reprodução deve usar uma exibição de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="ee975-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="ee975-140">Use este sinalizador somente ao executar arquivos compactados ou de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="ee975-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="ee975-141">Para dispositivos de vídeo digital, o *lpPlay* aponta para uma estrutura de parâmetros de [**reprodução de \_ DGV \_ \_ MCI**](/previous-versions//dd743396(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ee975-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="ee975-142">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="ee975-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ee975-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_ \_ reprodução de VCR MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="ee975-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="ee975-144">O membro **dwAt** da estrutura identificada por *lpPlay* contém uma hora em que o comando inteiro começa, ou se o dispositivo for cued, quando o dispositivo atingir a posição from fornecida pelo comando de [ \_ indicação MCI](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="ee975-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>reversão de \_ reprodução de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee975-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ee975-146">A reprodução deve ocorrer em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="ee975-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_verificação de \_ reprodução de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee975-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="ee975-148">A reprodução deve ser a mais rápida possível e manter a saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ee975-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="ee975-149">Para dispositivos VCR, o *lpPlay* aponta para uma estrutura de parâmetros de [**reprodução de \_ VCR \_ \_ MCI**](mci-vcr-play-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ee975-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="ee975-150">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VIDEODISC** :</span><span class="sxs-lookup"><span data-stu-id="ee975-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="ee975-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>\_ \_ reprodução rápida de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee975-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="ee975-152">Jogue rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ee975-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>reversão de \_ reprodução de VD MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee975-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="ee975-154">Reproduzir em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="ee975-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>\_exame de \_ reprodução de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee975-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="ee975-156">Verificar rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ee975-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>\_reprodução de VD MCI \_ \_ lenta</span><span class="sxs-lookup"><span data-stu-id="ee975-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="ee975-158">Reproduzir lentamente.</span><span class="sxs-lookup"><span data-stu-id="ee975-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="ee975-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_velocidade de \_ reprodução de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="ee975-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="ee975-160">A velocidade de reprodução é incluída no membro **dwSpeed** na estrutura identificada por *lpPlay*.</span><span class="sxs-lookup"><span data-stu-id="ee975-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee975-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee975-161">Requirements</span></span>



| <span data-ttu-id="ee975-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee975-162">Requirement</span></span> | <span data-ttu-id="ee975-163">Valor</span><span class="sxs-lookup"><span data-stu-id="ee975-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee975-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee975-164">Minimum supported client</span></span><br/> | <span data-ttu-id="ee975-165">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee975-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ee975-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee975-166">Minimum supported server</span></span><br/> | <span data-ttu-id="ee975-167">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee975-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee975-168">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee975-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee975-169"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee975-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee975-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee975-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee975-171">MCI</span><span class="sxs-lookup"><span data-stu-id="ee975-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ee975-172">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="ee975-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

