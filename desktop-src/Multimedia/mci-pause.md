---
title: MCI_PAUSE comando (mmsystem. h)
description: O \_ comando MCI PAUSE Pausa a ação atual. CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- Multimídia do Windows de comando MCI_PAUSE
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644230"
---
# <a name="mci_pause-command"></a><span data-ttu-id="28c64-105">\_Comando MCI Pause</span><span class="sxs-lookup"><span data-stu-id="28c64-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="28c64-106">O \_ comando MCI PAUSE Pausa a ação atual.</span><span class="sxs-lookup"><span data-stu-id="28c64-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="28c64-107">CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="28c64-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="28c64-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="28c64-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="28c64-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28c64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c64-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="28c64-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="28c64-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="28c64-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="28c64-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="28c64-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="28c64-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="28c64-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="28c64-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="28c64-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="28c64-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span><span class="sxs-lookup"><span data-stu-id="28c64-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="28c64-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="28c64-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="28c64-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="28c64-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c64-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="28c64-118">Return Value</span></span>

<span data-ttu-id="28c64-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="28c64-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="28c64-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="28c64-120">Remarks</span></span>

<span data-ttu-id="28c64-121">A diferença entre os [comandos \_ Stop MCI](mci-stop.md) e MCI \_ Pause depende do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28c64-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="28c64-122">Se possível, \_ a pausa do MCI suspende a operação do dispositivo, mas deixa o dispositivo pronto para retomar a reprodução imediatamente.</span><span class="sxs-lookup"><span data-stu-id="28c64-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="28c64-123">Com os drivers MCICDA, MCISEQ e MCIPIONR, o comando MCI \_ Pause funciona da mesma forma que o \_ comando MCI stop.</span><span class="sxs-lookup"><span data-stu-id="28c64-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="28c64-124">Para dispositivos de vídeo digital, o parâmetro *lpPause* aponta para uma estrutura [**DGV de \_ \_ Pausar \_ parâmetros do MCI**](/previous-versions//dd743395(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="28c64-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c64-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c64-125">Requirements</span></span>



| <span data-ttu-id="28c64-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c64-126">Requirement</span></span> | <span data-ttu-id="28c64-127">Valor</span><span class="sxs-lookup"><span data-stu-id="28c64-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c64-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c64-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28c64-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28c64-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="28c64-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c64-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28c64-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28c64-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28c64-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28c64-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c64-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28c64-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c64-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="28c64-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c64-135">MCI</span><span class="sxs-lookup"><span data-stu-id="28c64-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="28c64-136">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="28c64-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

