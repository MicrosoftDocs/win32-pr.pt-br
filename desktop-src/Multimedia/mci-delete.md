---
title: MCI_DELETE comando (mmsystem. h)
description: O \_ comando MCI Delete remove dados do arquivo. Os dispositivos digital-video e Wave-Audio reconhecem este comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- Multimídia do Windows de comando MCI_DELETE
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918758"
---
# <a name="mci_delete-command"></a><span data-ttu-id="d50ca-105">Comando de exclusão do MCI \_</span><span class="sxs-lookup"><span data-stu-id="d50ca-105">MCI\_DELETE command</span></span>

<span data-ttu-id="d50ca-106">O \_ comando MCI Delete remove dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d50ca-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="d50ca-107">Os dispositivos digital-video e Wave-Audio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="d50ca-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="d50ca-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="d50ca-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="d50ca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d50ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50ca-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="d50ca-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="d50ca-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d50ca-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-113">\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d50ca-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="d50ca-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d50ca-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span><span class="sxs-lookup"><span data-stu-id="d50ca-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d50ca-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="d50ca-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="d50ca-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d50ca-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d50ca-118">Return Value</span></span>

<span data-ttu-id="d50ca-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="d50ca-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d50ca-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d50ca-120">Remarks</span></span>

<span data-ttu-id="d50ca-121">Os seguintes sinalizadores se aplicam ao tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="d50ca-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d50ca-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>\_ \_ exclusão de DGV MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="d50ca-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-123">Um retângulo é incluído no membro **RC** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-124">O retângulo especifica a parte de cada quadro a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="d50ca-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="d50ca-125">Quando esse sinalizador é usado, o quadro é retido no espaço de trabalho e a área especificada pelo retângulo se torna preta.</span><span class="sxs-lookup"><span data-stu-id="d50ca-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="d50ca-126">Se o sinalizador for omitido, o MCI \_ excluirá o padrão para o quadro inteiro e removerá o quadro do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d50ca-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>\_fluxo de \_ áudio de exclusão de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="d50ca-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-128">Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-129">Se você usar esse sinalizador e também quiser excluir o vídeo, também deverá usar o sinalizador MCI \_ DGV \_ excluir \_ fluxo de vídeo \_ .</span><span class="sxs-lookup"><span data-stu-id="d50ca-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="d50ca-130">(Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão excluídos.)</span><span class="sxs-lookup"><span data-stu-id="d50ca-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_fluxo de \_ vídeo de exclusão de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="d50ca-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-132">Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-133">Se você usar esse sinalizador e também quiser excluir áudio, você também deverá usar o sinalizador de \_ fluxo de áudio MCI DGV \_ excluir \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d50ca-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="d50ca-134">(Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão excluídos.)</span><span class="sxs-lookup"><span data-stu-id="d50ca-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="d50ca-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-136">Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-137">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="d50ca-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="d50ca-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-139">Um local final é incluído no membro **dwTo** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-140">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d50ca-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="d50ca-141">Para dispositivos de vídeo digital, o parâmetro *lpDelete* aponta para uma estrutura de [**exclusão de \_ \_ \_ parâmetros DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .</span><span class="sxs-lookup"><span data-stu-id="d50ca-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="d50ca-142">Os seguintes sinalizadores se aplicam ao tipo de dispositivo **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="d50ca-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="d50ca-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="d50ca-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-144">Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-145">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do [ \_ conjunto de MCI](mci-set.md).</span><span class="sxs-lookup"><span data-stu-id="d50ca-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="d50ca-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-147">Um local final é incluído no membro **dwTo** da estrutura identificada por *lpDelete*.</span><span class="sxs-lookup"><span data-stu-id="d50ca-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="d50ca-148">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d50ca-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="d50ca-149">Para dispositivos de formato de onda-áudio, o parâmetro *lpDelete* aponta para uma estrutura de [**parâmetros de \_ \_ exclusão \_ de Wave MCI**](mci-wave-delete-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d50ca-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d50ca-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d50ca-150">Requirements</span></span>



| <span data-ttu-id="d50ca-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50ca-151">Requirement</span></span> | <span data-ttu-id="d50ca-152">Valor</span><span class="sxs-lookup"><span data-stu-id="d50ca-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50ca-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d50ca-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d50ca-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d50ca-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d50ca-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d50ca-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d50ca-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d50ca-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d50ca-158"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d50ca-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d50ca-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="d50ca-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50ca-160">MCI</span><span class="sxs-lookup"><span data-stu-id="d50ca-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d50ca-161">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d50ca-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

