---
title: MCI_PASTE comando (mmsystem. h)
description: O \_ comando Paste do MCI cola os dados da área de transferência em um arquivo. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Multimídia do Windows de comando MCI_PASTE
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644231"
---
# <a name="mci_paste-command"></a><span data-ttu-id="cdcec-105">\_Comando de colar MCI</span><span class="sxs-lookup"><span data-stu-id="cdcec-105">MCI\_PASTE command</span></span>

<span data-ttu-id="cdcec-106">O \_ comando Paste do MCI cola os dados da área de transferência em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="cdcec-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="cdcec-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="cdcec-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="cdcec-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="cdcec-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="cdcec-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdcec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdcec-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cdcec-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="cdcec-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cdcec-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="cdcec-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="cdcec-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cdcec-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span><span class="sxs-lookup"><span data-stu-id="cdcec-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-116">Ponteiro para uma estrutura de [**\_ parâmetros de \_ colagem \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .</span><span class="sxs-lookup"><span data-stu-id="cdcec-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdcec-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cdcec-117">Return Value</span></span>

<span data-ttu-id="cdcec-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="cdcec-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdcec-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdcec-119">Remarks</span></span>

<span data-ttu-id="cdcec-120">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="cdcec-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="cdcec-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_colar DGV do MCI \_ \_ em</span><span class="sxs-lookup"><span data-stu-id="cdcec-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-122">Um retângulo é incluído no membro **RC** da estrutura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="cdcec-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="cdcec-123">Os dois primeiros valores do retângulo especificam o ponto dentro do quadro para inserir as informações da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="cdcec-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="cdcec-124">Se a altura e a largura do retângulo forem diferentes de zero, o conteúdo da área de transferência será dimensionado para essas dimensões quando elas forem coladas no quadro.</span><span class="sxs-lookup"><span data-stu-id="cdcec-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="cdcec-125">Se o sinalizador for omitido, a \_ colagem do MCI padronizará para todo o retângulo do quadro.</span><span class="sxs-lookup"><span data-stu-id="cdcec-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>fluxo de áudio do MCI \_ DGV \_ colar \_ \_</span><span class="sxs-lookup"><span data-stu-id="cdcec-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-127">Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="cdcec-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="cdcec-128">Se houver apenas um fluxo de áudio na área de transferência, os dados de áudio serão colados no fluxo designado.</span><span class="sxs-lookup"><span data-stu-id="cdcec-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="cdcec-129">Se houver mais de um fluxo de áudio na área de transferência, o fluxo indicará o número inicial para as sequências de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cdcec-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="cdcec-130">Se você usar esse sinalizador e também quiser colar o vídeo, você também deverá usar o sinalizador de fluxo de vídeo MCI do \_ DGV de \_ colagem \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cdcec-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="cdcec-131">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados começando com o primeiro fluxo de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="cdcec-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="cdcec-132">Cada fluxo colado mantém seu número de fluxo original.)</span><span class="sxs-lookup"><span data-stu-id="cdcec-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_inserção de \_ colar \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="cdcec-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-134">Os dados da área de transferência devem ser inseridos no espaço de trabalho existente na posição especificada pelo \_ sinalizador MCI.</span><span class="sxs-lookup"><span data-stu-id="cdcec-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="cdcec-135">Todos os dados existentes após o ponto de inserção são movidos no espaço de trabalho para liberar espaço.</span><span class="sxs-lookup"><span data-stu-id="cdcec-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="cdcec-136">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="cdcec-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>\_substituição de \_ colar \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="cdcec-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-138">Os dados da área de transferência devem substituir os dados já presentes no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cdcec-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="cdcec-139">Os dados de espaço de trabalho substituídos seguem o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="cdcec-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_fluxo de \_ vídeo de colar DGV \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="cdcec-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-141">Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="cdcec-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="cdcec-142">Se houver apenas um fluxo de vídeo na área de transferência, os dados de vídeo serão colados no fluxo designado.</span><span class="sxs-lookup"><span data-stu-id="cdcec-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="cdcec-143">Se houver mais de um fluxo de vídeo na área de transferência, o fluxo indicará o número inicial para as sequências de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cdcec-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="cdcec-144">Se você usar esse sinalizador e também quiser colar o áudio, também deverá usar o sinalizador de \_ fluxo de áudio MCI DGV \_ colar \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cdcec-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="cdcec-145">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados começando com o primeiro fluxo de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="cdcec-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="cdcec-146">Cada fluxo colado mantém seu número de fluxo original.)</span><span class="sxs-lookup"><span data-stu-id="cdcec-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="cdcec-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="cdcec-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="cdcec-148">Um valor de posição é incluído no membro **dwTo** da estrutura identificada por *lpPaste*.</span><span class="sxs-lookup"><span data-stu-id="cdcec-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="cdcec-149">O valor de posição especifica a posição para começar a colar dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cdcec-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="cdcec-150">Se esse sinalizador for omitido, a posição padrão será a posição atual.</span><span class="sxs-lookup"><span data-stu-id="cdcec-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdcec-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdcec-151">Requirements</span></span>



| <span data-ttu-id="cdcec-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdcec-152">Requirement</span></span> | <span data-ttu-id="cdcec-153">Valor</span><span class="sxs-lookup"><span data-stu-id="cdcec-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcec-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdcec-154">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcec-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdcec-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cdcec-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdcec-156">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcec-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdcec-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cdcec-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cdcec-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdcec-159"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdcec-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcec-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdcec-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcec-161">MCI</span><span class="sxs-lookup"><span data-stu-id="cdcec-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cdcec-162">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="cdcec-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

