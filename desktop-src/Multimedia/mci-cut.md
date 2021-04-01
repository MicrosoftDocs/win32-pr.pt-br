---
title: MCI_CUT comando (mmsystem. h)
description: O \_ comando Recortar do MCI remove os dados do arquivo e os copia para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Multimídia do Windows de comando MCI_CUT
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918759"
---
# <a name="mci_cut-command"></a><span data-ttu-id="10127-105">\_Comando de recorte do MCI</span><span class="sxs-lookup"><span data-stu-id="10127-105">MCI\_CUT command</span></span>

<span data-ttu-id="10127-106">O \_ comando Recortar do MCI remove os dados do arquivo e os copia para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="10127-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="10127-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="10127-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="10127-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="10127-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="10127-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10127-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10127-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="10127-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="10127-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="10127-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="10127-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="10127-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="10127-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="10127-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="10127-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="10127-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="10127-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span><span class="sxs-lookup"><span data-stu-id="10127-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="10127-116">Ponteiro para uma estrutura [**MCI \_ DGV \_ recortar \_ parâmetros**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .</span><span class="sxs-lookup"><span data-stu-id="10127-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10127-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="10127-117">Return Value</span></span>

<span data-ttu-id="10127-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="10127-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="10127-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="10127-119">Remarks</span></span>

<span data-ttu-id="10127-120">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="10127-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="10127-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>DGV do MCI \_ \_ recortar \_ em</span><span class="sxs-lookup"><span data-stu-id="10127-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="10127-122">Um retângulo é incluído no membro **RC** da estrutura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="10127-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="10127-123">O retângulo especifica a parte de cada quadro a ser recortada.</span><span class="sxs-lookup"><span data-stu-id="10127-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="10127-124">Se o sinalizador for omitido, o MCI \_ recortará o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="10127-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="10127-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_fluxo de \_ áudio de recorte MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="10127-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="10127-126">Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="10127-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="10127-127">Se você usar esse sinalizador e também quiser recortar o vídeo, também deverá usar o \_ sinalizador de \_ fluxo de vídeo de recorte do DGV MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="10127-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="10127-128">(Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão recortados.)</span><span class="sxs-lookup"><span data-stu-id="10127-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="10127-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_fluxo de \_ vídeo de recorte de DGV MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="10127-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="10127-130">Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="10127-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="10127-131">Se você usar esse sinalizador e também quiser cortar o áudio, também deverá usar o sinalizador de \_ \_ fluxo de áudio de recorte MCI DGV \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="10127-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="10127-132">(Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão recortados.)</span><span class="sxs-lookup"><span data-stu-id="10127-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="10127-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de</span><span class="sxs-lookup"><span data-stu-id="10127-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="10127-134">Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="10127-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="10127-135">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="10127-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="10127-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="10127-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="10127-137">Um local final é incluído no membro **dwTo** da estrutura identificada por *lpCut*.</span><span class="sxs-lookup"><span data-stu-id="10127-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="10127-138">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="10127-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10127-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10127-139">Requirements</span></span>



| <span data-ttu-id="10127-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="10127-140">Requirement</span></span> | <span data-ttu-id="10127-141">Valor</span><span class="sxs-lookup"><span data-stu-id="10127-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10127-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10127-142">Minimum supported client</span></span><br/> | <span data-ttu-id="10127-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10127-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10127-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10127-144">Minimum supported server</span></span><br/> | <span data-ttu-id="10127-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10127-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="10127-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10127-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="10127-147"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10127-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10127-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="10127-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10127-149">MCI</span><span class="sxs-lookup"><span data-stu-id="10127-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="10127-150">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="10127-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

