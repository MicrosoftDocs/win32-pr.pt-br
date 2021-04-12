---
title: comando Step
description: As etapas do comando Step executam um ou mais quadros para frente ou verso. A ação padrão é avançar um quadro. Dispositivos Digital-Video, VCR e CAV-Format VIDEODISC reconhecem este comando.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- comando da etapa multimídia do Windows
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455102"
---
# <a name="step-command"></a><span data-ttu-id="e75c6-106">comando Step</span><span class="sxs-lookup"><span data-stu-id="e75c6-106">step command</span></span>

<span data-ttu-id="e75c6-107">As etapas do comando Step executam um ou mais quadros para frente ou verso.</span><span class="sxs-lookup"><span data-stu-id="e75c6-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="e75c6-108">A ação padrão é avançar um quadro.</span><span class="sxs-lookup"><span data-stu-id="e75c6-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="e75c6-109">Dispositivos Digital-Video, VCR e CAV-Format VIDEODISC reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="e75c6-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="e75c6-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e75c6-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e75c6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e75c6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e75c6-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="e75c6-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e75c6-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e75c6-113">Identifier of an MCI device.</span></span> <span data-ttu-id="e75c6-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="e75c6-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e75c6-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span><span class="sxs-lookup"><span data-stu-id="e75c6-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e75c6-116">Um ou ambos os sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e75c6-116">One or both of the following flags.</span></span>



| <span data-ttu-id="e75c6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e75c6-117">Value</span></span>       | <span data-ttu-id="e75c6-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e75c6-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75c6-119">por *quadros*</span><span class="sxs-lookup"><span data-stu-id="e75c6-119">by *frames*</span></span> | <span data-ttu-id="e75c6-120">Indica o número de quadros a serem conetapas.</span><span class="sxs-lookup"><span data-stu-id="e75c6-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="e75c6-121">Se você especificar um valor de *quadros* negativos, não poderá especificar o sinalizador "Reverse".</span><span class="sxs-lookup"><span data-stu-id="e75c6-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="e75c6-122">reverse</span><span class="sxs-lookup"><span data-stu-id="e75c6-122">reverse</span></span>     | <span data-ttu-id="e75c6-123">Passe os quadros em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="e75c6-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="e75c6-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="e75c6-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e75c6-125">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="e75c6-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="e75c6-126">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e75c6-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="e75c6-127">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e75c6-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e75c6-128">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e75c6-128">Return Value</span></span>

<span data-ttu-id="e75c6-129">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e75c6-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75c6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e75c6-130">Requirements</span></span>



| <span data-ttu-id="e75c6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e75c6-131">Requirement</span></span> | <span data-ttu-id="e75c6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e75c6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e75c6-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e75c6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e75c6-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e75c6-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e75c6-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e75c6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e75c6-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e75c6-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e75c6-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e75c6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75c6-138">MCI</span><span class="sxs-lookup"><span data-stu-id="e75c6-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e75c6-139">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="e75c6-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

