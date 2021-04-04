---
title: MCI_COPY comando (mmsystem. h)
description: O \_ comando de cópia MCI copia dados para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- Multimídia do Windows de comando MCI_COPY
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918509"
---
# <a name="mci_copy-command"></a><span data-ttu-id="2627a-105">\_Comando de cópia MCI</span><span class="sxs-lookup"><span data-stu-id="2627a-105">MCI\_COPY command</span></span>

<span data-ttu-id="2627a-106">O \_ comando de cópia MCI copia dados para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="2627a-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="2627a-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="2627a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="2627a-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="2627a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="2627a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2627a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2627a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2627a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2627a-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="2627a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2627a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2627a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2627a-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2627a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2627a-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2627a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2627a-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span><span class="sxs-lookup"><span data-stu-id="2627a-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="2627a-116">Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de cópia DGV do MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .</span><span class="sxs-lookup"><span data-stu-id="2627a-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2627a-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2627a-117">Return Value</span></span>

<span data-ttu-id="2627a-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="2627a-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2627a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2627a-119">Remarks</span></span>

<span data-ttu-id="2627a-120">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="2627a-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="2627a-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_cópia DGV do MCI \_ \_ em</span><span class="sxs-lookup"><span data-stu-id="2627a-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="2627a-122">Um retângulo é incluído no membro **RC** da estrutura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="2627a-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="2627a-123">O retângulo especifica a parte de cada quadro a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="2627a-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="2627a-124">Se o sinalizador for omitido, a \_ cópia do MCI copiará o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="2627a-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="2627a-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_fluxo de \_ áudio de cópia DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="2627a-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="2627a-126">Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="2627a-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="2627a-127">Se você usar esse sinalizador e também quiser copiar o vídeo, também deverá usar o sinalizador de \_ fluxo de vídeo MCI DGV \_ Copy \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2627a-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="2627a-128">(Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão copiados.)</span><span class="sxs-lookup"><span data-stu-id="2627a-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="2627a-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_fluxo de \_ vídeo de cópia DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="2627a-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="2627a-130">Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="2627a-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="2627a-131">Se você usar esse sinalizador e também quiser copiar áudio, você também deverá usar o sinalizador de \_ fluxo de áudio MCI DGV \_ copiar \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2627a-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="2627a-132">(Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão copiados.)</span><span class="sxs-lookup"><span data-stu-id="2627a-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="2627a-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="2627a-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="2627a-134">Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="2627a-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="2627a-135">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="2627a-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="2627a-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="2627a-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="2627a-137">Um local final é incluído no membro **dwTo** da estrutura identificada por *lpCopy*.</span><span class="sxs-lookup"><span data-stu-id="2627a-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="2627a-138">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do \_ comando MCI set.</span><span class="sxs-lookup"><span data-stu-id="2627a-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2627a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2627a-139">Requirements</span></span>



| <span data-ttu-id="2627a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2627a-140">Requirement</span></span> | <span data-ttu-id="2627a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="2627a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2627a-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2627a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2627a-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2627a-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2627a-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2627a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2627a-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2627a-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2627a-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2627a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2627a-147"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2627a-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2627a-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="2627a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2627a-149">MCI</span><span class="sxs-lookup"><span data-stu-id="2627a-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2627a-150">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="2627a-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

