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
# <a name="stop-command"></a><span data-ttu-id="cfabd-105">comando de parada</span><span class="sxs-lookup"><span data-stu-id="cfabd-105">stop command</span></span>

<span data-ttu-id="cfabd-106">O comando parar interrompe a reprodução ou a gravação.</span><span class="sxs-lookup"><span data-stu-id="cfabd-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="cfabd-107">CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="cfabd-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="cfabd-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="cfabd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="cfabd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfabd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfabd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="cfabd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cfabd-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="cfabd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="cfabd-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="cfabd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="cfabd-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span><span class="sxs-lookup"><span data-stu-id="cfabd-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cfabd-114">Para dispositivos de vídeo digital, ele pode ser o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="cfabd-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="cfabd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cfabd-115">Value</span></span> | <span data-ttu-id="cfabd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="cfabd-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfabd-117">bloqueio</span><span class="sxs-lookup"><span data-stu-id="cfabd-117">hold</span></span>  | <span data-ttu-id="cfabd-118">Impede a liberação de recursos necessários para redesenhar uma imagem ainda na tela.</span><span class="sxs-lookup"><span data-stu-id="cfabd-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="cfabd-119">O buffer de quadros permanece disponível para uso na atualização da exibição quando, por exemplo, a janela é movida.</span><span class="sxs-lookup"><span data-stu-id="cfabd-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="cfabd-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="cfabd-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cfabd-121">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="cfabd-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="cfabd-122">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="cfabd-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="cfabd-123">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cfabd-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfabd-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cfabd-124">Return Value</span></span>

<span data-ttu-id="cfabd-125">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="cfabd-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfabd-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfabd-126">Remarks</span></span>

<span data-ttu-id="cfabd-127">Para dispositivos de áudio de CD, o comando parar interrompe a reprodução e redefine a posição da faixa atual para zero.</span><span class="sxs-lookup"><span data-stu-id="cfabd-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="cfabd-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cfabd-128">Examples</span></span>

<span data-ttu-id="cfabd-129">O comando a seguir interrompe a reprodução ou a gravação no dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="cfabd-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="cfabd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfabd-130">Requirements</span></span>



| <span data-ttu-id="cfabd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfabd-131">Requirement</span></span> | <span data-ttu-id="cfabd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="cfabd-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cfabd-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfabd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cfabd-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cfabd-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cfabd-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfabd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cfabd-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cfabd-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cfabd-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfabd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfabd-138">MCI</span><span class="sxs-lookup"><span data-stu-id="cfabd-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cfabd-139">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="cfabd-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

