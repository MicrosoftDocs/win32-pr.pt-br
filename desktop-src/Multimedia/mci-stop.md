---
title: MCI_STOP comando (mmsystem. h)
description: O \_ comando MCI Stop interrompe todas as sequências de reprodução e registro, descarrega todos os buffers de reprodução e deixa de exibir imagens de vídeo. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- Multimídia do Windows de comando MCI_STOP
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369671"
---
# <a name="mci_stop-command"></a><span data-ttu-id="93e81-105">\_Comando Stop MCI</span><span class="sxs-lookup"><span data-stu-id="93e81-105">MCI\_STOP command</span></span>

<span data-ttu-id="93e81-106">O \_ comando MCI Stop interrompe todas as sequências de reprodução e registro, descarrega todos os buffers de reprodução e deixa de exibir imagens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93e81-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="93e81-107">CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="93e81-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="93e81-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="93e81-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="93e81-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93e81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e81-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="93e81-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="93e81-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="93e81-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="93e81-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="93e81-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="93e81-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="93e81-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="93e81-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="93e81-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="93e81-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span><span class="sxs-lookup"><span data-stu-id="93e81-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="93e81-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="93e81-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="93e81-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="93e81-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e81-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="93e81-118">Return Value</span></span>

<span data-ttu-id="93e81-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="93e81-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e81-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="93e81-120">Remarks</span></span>

<span data-ttu-id="93e81-121">A diferença entre os \_ comandos Stop MCI e [MCI \_ Pause](mci-pause.md) depende do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93e81-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="93e81-122">Se possível, \_ a pausa do MCI suspende a operação do dispositivo, mas deixa o dispositivo pronto para retomar a reprodução imediatamente.</span><span class="sxs-lookup"><span data-stu-id="93e81-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="93e81-123">Para o dispositivo de áudio de CD, \_ o MCI Stop redefine a posição da faixa atual para zero; por outro lado, a [ \_ pausa do MCI](mci-pause.md) mantém a posição atual da faixa, antecipando que o dispositivo retomará a reprodução.</span><span class="sxs-lookup"><span data-stu-id="93e81-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e81-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e81-124">Requirements</span></span>



| <span data-ttu-id="93e81-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e81-125">Requirement</span></span> | <span data-ttu-id="93e81-126">Valor</span><span class="sxs-lookup"><span data-stu-id="93e81-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e81-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e81-127">Minimum supported client</span></span><br/> | <span data-ttu-id="93e81-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93e81-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93e81-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e81-129">Minimum supported server</span></span><br/> | <span data-ttu-id="93e81-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93e81-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93e81-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="93e81-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e81-132"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e81-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e81-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="93e81-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e81-134">MCI</span><span class="sxs-lookup"><span data-stu-id="93e81-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="93e81-135">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="93e81-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

