---
title: MCI_RESUME comando (mmsystem. h)
description: O \_ comando de retomada do MCI faz com que um dispositivo em pausa retome a operação pausada.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- Multimídia do Windows de comando MCI_RESUME
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918107"
---
# <a name="mci_resume-command"></a><span data-ttu-id="f9508-104">\_Comando de retomada do MCI</span><span class="sxs-lookup"><span data-stu-id="f9508-104">MCI\_RESUME command</span></span>

<span data-ttu-id="f9508-105">O \_ comando de retomada do MCI faz com que um dispositivo em pausa retome a operação pausada.</span><span class="sxs-lookup"><span data-stu-id="f9508-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="f9508-106">Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f9508-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="f9508-107">Embora os dispositivos de áudio CD, MIDI Sequencer e VIDEODISC também reconheçam esse comando, os drivers de dispositivo MCICDA, MCISEQ e MCIPIONR não dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="f9508-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="f9508-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9508-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="f9508-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9508-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9508-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f9508-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f9508-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="f9508-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f9508-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f9508-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f9508-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="f9508-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="f9508-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f9508-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9508-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span><span class="sxs-lookup"><span data-stu-id="f9508-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="f9508-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f9508-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f9508-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="f9508-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9508-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f9508-118">Return Value</span></span>

<span data-ttu-id="f9508-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f9508-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9508-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9508-120">Remarks</span></span>

<span data-ttu-id="f9508-121">Esse comando retoma a reprodução e a gravação sem alterar o conjunto de posições de faixa atual com [o \_ registro](mci-record.md)MCI de [ \_ reprodução](mci-play.md) ou MCI.</span><span class="sxs-lookup"><span data-stu-id="f9508-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9508-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9508-122">Requirements</span></span>



| <span data-ttu-id="f9508-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9508-123">Requirement</span></span> | <span data-ttu-id="f9508-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f9508-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9508-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9508-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f9508-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9508-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9508-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9508-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f9508-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9508-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f9508-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9508-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9508-130"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9508-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9508-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9508-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9508-132">MCI</span><span class="sxs-lookup"><span data-stu-id="f9508-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f9508-133">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f9508-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

