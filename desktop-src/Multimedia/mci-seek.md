---
title: MCI_SEEK comando (mmsystem. h)
description: O \_ comando MCI Seek altera a posição atual no conteúdo o mais rápido possível.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Multimídia do Windows de comando MCI_SEEK
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009057"
---
# <a name="mci_seek-command"></a><span data-ttu-id="7760b-104">Comando de busca do MCI \_</span><span class="sxs-lookup"><span data-stu-id="7760b-104">MCI\_SEEK command</span></span>

<span data-ttu-id="7760b-105">O \_ comando MCI Seek altera a posição atual no conteúdo o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="7760b-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="7760b-106">A saída de vídeo e áudio é desabilitada durante a busca.</span><span class="sxs-lookup"><span data-stu-id="7760b-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="7760b-107">Depois que a busca for concluída, o dispositivo será interrompido.</span><span class="sxs-lookup"><span data-stu-id="7760b-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="7760b-108">CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="7760b-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="7760b-109">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="7760b-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="7760b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7760b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7760b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7760b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7760b-112">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="7760b-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7760b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7760b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7760b-114">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="7760b-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="7760b-115">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7760b-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7760b-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span><span class="sxs-lookup"><span data-stu-id="7760b-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="7760b-117">Ponteiro para uma estrutura de [**\_ \_ parâmetros de busca MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7760b-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="7760b-118">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="7760b-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7760b-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7760b-119">Return Value</span></span>

<span data-ttu-id="7760b-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="7760b-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7760b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7760b-121">Remarks</span></span>

<span data-ttu-id="7760b-122">Se um tamanho de amostra de dados para um dispositivo for maior do que 1 byte (como com dados de wave-áudio estéreo), esse comando passará para o início do exemplo mais próximo quando uma posição especificada não coincidir com o início de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="7760b-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="7760b-123">Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte ao MCI \_ Seek:</span><span class="sxs-lookup"><span data-stu-id="7760b-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="7760b-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ buscar \_ até o \_ fim</span><span class="sxs-lookup"><span data-stu-id="7760b-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="7760b-125">Busque até o final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7760b-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="7760b-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ buscar \_ para \_ Iniciar</span><span class="sxs-lookup"><span data-stu-id="7760b-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="7760b-127">Procure o início do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7760b-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="7760b-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para</span><span class="sxs-lookup"><span data-stu-id="7760b-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="7760b-129">Uma posição é incluída no membro **dwTo** da estrutura identificada por *lpSeek*.</span><span class="sxs-lookup"><span data-stu-id="7760b-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="7760b-130">As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="7760b-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="7760b-131">Não use esse sinalizador com o MCI \_ Seek \_ para \_ final ou MCI \_ Seek \_ para \_ Iniciar.</span><span class="sxs-lookup"><span data-stu-id="7760b-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="7760b-132">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="7760b-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7760b-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>o \_ VCR do MCI \_ busca \_ em</span><span class="sxs-lookup"><span data-stu-id="7760b-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="7760b-134">O membro **dwAt** da estrutura identificada por *lpSeek* contém uma hora em que o comando inteiro começa.</span><span class="sxs-lookup"><span data-stu-id="7760b-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="7760b-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_marca de \_ busca do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="7760b-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="7760b-136">O membro **dwMark** da estrutura identificada por *lpSeek* contém a marca numerada a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="7760b-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="7760b-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>inverso de busca de videocassete de MCI \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7760b-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7760b-138">A direção de busca é inversa; Isso é usado apenas com o \_ sinalizador de marca de busca de VCR MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7760b-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="7760b-139">Para dispositivos VCR, o parâmetro *lpSeek* aponta para uma estrutura de parâmetros de busca de videocassete do [**MCI \_ \_ \_**](mci-vcr-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="7760b-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="7760b-140">O seguinte sinalizador adicional é usado com o tipo de dispositivo **VIDEODISC** :</span><span class="sxs-lookup"><span data-stu-id="7760b-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="7760b-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>\_inversa de \_ busca de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="7760b-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="7760b-142">A direção de busca é inversa.</span><span class="sxs-lookup"><span data-stu-id="7760b-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7760b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7760b-143">Requirements</span></span>



| <span data-ttu-id="7760b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7760b-144">Requirement</span></span> | <span data-ttu-id="7760b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7760b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7760b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7760b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7760b-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7760b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7760b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7760b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7760b-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7760b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7760b-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7760b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7760b-151"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7760b-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7760b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="7760b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7760b-153">MCI</span><span class="sxs-lookup"><span data-stu-id="7760b-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7760b-154">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="7760b-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

