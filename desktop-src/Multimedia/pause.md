---
title: comando Pause
description: O comando PAUSE Pausa a reprodução ou a gravação.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- pausar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824819"
---
# <a name="pause-command"></a><span data-ttu-id="48183-104">comando Pause</span><span class="sxs-lookup"><span data-stu-id="48183-104">pause command</span></span>

<span data-ttu-id="48183-105">O comando PAUSE Pausa a reprodução ou a gravação.</span><span class="sxs-lookup"><span data-stu-id="48183-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="48183-106">A maioria dos drivers mantém a posição atual e, eventualmente, reinicia a reprodução ou a gravação nessa posição.</span><span class="sxs-lookup"><span data-stu-id="48183-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="48183-107">CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="48183-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="48183-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="48183-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="48183-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48183-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48183-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="48183-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="48183-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="48183-111">Identifier of an MCI device.</span></span> <span data-ttu-id="48183-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="48183-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="48183-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="48183-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="48183-114">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="48183-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="48183-115">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="48183-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="48183-116">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="48183-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48183-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="48183-117">Return Value</span></span>

<span data-ttu-id="48183-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="48183-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="48183-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="48183-119">Remarks</span></span>

<span data-ttu-id="48183-120">Com os drivers MCICDA, MCISEQ e MCIPIONR, o comando Pause funciona da mesma forma que o comando [Stop](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="48183-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="48183-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48183-121">Examples</span></span>

<span data-ttu-id="48183-122">O comando a seguir pausa o dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="48183-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="48183-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48183-123">Requirements</span></span>



| <span data-ttu-id="48183-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="48183-124">Requirement</span></span> | <span data-ttu-id="48183-125">Valor</span><span class="sxs-lookup"><span data-stu-id="48183-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="48183-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48183-126">Minimum supported client</span></span><br/> | <span data-ttu-id="48183-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48183-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48183-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48183-128">Minimum supported server</span></span><br/> | <span data-ttu-id="48183-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48183-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="48183-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="48183-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48183-131">MCI</span><span class="sxs-lookup"><span data-stu-id="48183-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="48183-132">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="48183-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="48183-133">stop</span><span class="sxs-lookup"><span data-stu-id="48183-133">stop</span></span>](stop.md)
</dt> </dl>

 

