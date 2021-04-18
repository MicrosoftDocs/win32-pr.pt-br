---
title: comando retomar
description: O comando retomar continua a reproduzir ou gravar em um dispositivo que foi pausado usando o comando PAUSE.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- retomar a multimídia do Windows do comando
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810304"
---
# <a name="resume-command"></a><span data-ttu-id="0e3d4-104">comando retomar</span><span class="sxs-lookup"><span data-stu-id="0e3d4-104">resume command</span></span>

<span data-ttu-id="0e3d4-105">O comando retomar continua a reproduzir ou gravar em um dispositivo que foi pausado usando o comando [Pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="0e3d4-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="0e3d4-106">Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="0e3d4-107">Embora os dispositivos de áudio CD, MIDI Sequencer e VIDEODISC também reconheçam esse comando, os drivers de dispositivo MCICDA, MCISEQ e MCIPIONR não dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="0e3d4-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0e3d4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e3d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e3d4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="0e3d4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0e3d4-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0e3d4-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0e3d4-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="0e3d4-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0e3d4-114">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0e3d4-115">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="0e3d4-116">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0e3d4-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e3d4-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0e3d4-117">Return Value</span></span>

<span data-ttu-id="0e3d4-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="0e3d4-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="0e3d4-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e3d4-119">Examples</span></span>

<span data-ttu-id="0e3d4-120">O comando a seguir continua a reproduzir ou gravar o dispositivo "newsound".</span><span class="sxs-lookup"><span data-stu-id="0e3d4-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="0e3d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e3d4-121">Requirements</span></span>



| <span data-ttu-id="0e3d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e3d4-122">Requirement</span></span> | <span data-ttu-id="0e3d4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0e3d4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e3d4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e3d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3d4-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e3d4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e3d4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e3d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3d4-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e3d4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0e3d4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e3d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3d4-129">MCI</span><span class="sxs-lookup"><span data-stu-id="0e3d4-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0e3d4-130">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="0e3d4-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="0e3d4-131">pause</span><span class="sxs-lookup"><span data-stu-id="0e3d4-131">pause</span></span>](pause.md)
</dt> </dl>

 

