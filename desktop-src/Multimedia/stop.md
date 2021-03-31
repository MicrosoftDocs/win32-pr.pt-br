---
title: comando de parada
description: O comando parar interrompe a reprodução ou a gravação. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- comando parar multimídia do Windows
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369607"
---
# <a name="stop-command"></a><span data-ttu-id="e95fc-105">comando de parada</span><span class="sxs-lookup"><span data-stu-id="e95fc-105">stop command</span></span>

<span data-ttu-id="e95fc-106">O comando parar interrompe a reprodução ou a gravação.</span><span class="sxs-lookup"><span data-stu-id="e95fc-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="e95fc-107">CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="e95fc-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="e95fc-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e95fc-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e95fc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e95fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95fc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e95fc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e95fc-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e95fc-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e95fc-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="e95fc-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e95fc-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span><span class="sxs-lookup"><span data-stu-id="e95fc-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e95fc-114">Para dispositivos de vídeo digital, ele pode ser o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="e95fc-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="e95fc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e95fc-115">Value</span></span> | <span data-ttu-id="e95fc-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e95fc-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95fc-117">bloqueio</span><span class="sxs-lookup"><span data-stu-id="e95fc-117">hold</span></span>  | <span data-ttu-id="e95fc-118">Impede a liberação de recursos necessários para redesenhar uma imagem ainda na tela.</span><span class="sxs-lookup"><span data-stu-id="e95fc-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="e95fc-119">O buffer de quadros permanece disponível para uso na atualização da exibição quando, por exemplo, a janela é movida.</span><span class="sxs-lookup"><span data-stu-id="e95fc-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e95fc-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e95fc-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e95fc-121">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="e95fc-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e95fc-122">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e95fc-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="e95fc-123">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e95fc-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95fc-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e95fc-124">Return Value</span></span>

<span data-ttu-id="e95fc-125">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e95fc-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e95fc-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e95fc-126">Remarks</span></span>

<span data-ttu-id="e95fc-127">Para dispositivos de áudio de CD, o comando parar interrompe a reprodução e redefine a posição da faixa atual para zero.</span><span class="sxs-lookup"><span data-stu-id="e95fc-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="e95fc-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e95fc-128">Examples</span></span>

<span data-ttu-id="e95fc-129">O comando a seguir interrompe a reprodução ou a gravação no dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="e95fc-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="e95fc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e95fc-130">Requirements</span></span>



| <span data-ttu-id="e95fc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e95fc-131">Requirement</span></span> | <span data-ttu-id="e95fc-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e95fc-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e95fc-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e95fc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e95fc-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e95fc-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e95fc-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e95fc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e95fc-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e95fc-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e95fc-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e95fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95fc-138">MCI</span><span class="sxs-lookup"><span data-stu-id="e95fc-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e95fc-139">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="e95fc-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

