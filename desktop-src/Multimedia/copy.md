---
title: comando de cópia
description: O comando de cópia copia dados para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- comando de cópia multimídia do Windows
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644399"
---
# <a name="copy-command"></a><span data-ttu-id="bc06a-105">comando de cópia</span><span class="sxs-lookup"><span data-stu-id="bc06a-105">copy command</span></span>

<span data-ttu-id="bc06a-106">O comando de cópia copia dados para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="bc06a-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="bc06a-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="bc06a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="bc06a-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="bc06a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="bc06a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc06a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc06a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bc06a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bc06a-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="bc06a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="bc06a-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="bc06a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="bc06a-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="bc06a-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="bc06a-114">Um dos sinalizadores a seguir que identificam o item a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="bc06a-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="bc06a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bc06a-115">Value</span></span>                 | <span data-ttu-id="bc06a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="bc06a-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc06a-117">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="bc06a-117">at *rectangle*</span></span>        | <span data-ttu-id="bc06a-118">Especifica a parte de cada quadro que será copiada.</span><span class="sxs-lookup"><span data-stu-id="bc06a-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="bc06a-119">Se omitido, a configuração padrão será o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="bc06a-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="bc06a-120">*fluxo* de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="bc06a-120">audio stream *stream*</span></span> | <span data-ttu-id="bc06a-121">Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="bc06a-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="bc06a-122">Se você usar esse sinalizador e também quiser copiar o vídeo, também deverá usar o sinalizador "fluxo de vídeo".</span><span class="sxs-lookup"><span data-stu-id="bc06a-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="bc06a-123">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão copiados.)</span><span class="sxs-lookup"><span data-stu-id="bc06a-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="bc06a-124">da *posição*</span><span class="sxs-lookup"><span data-stu-id="bc06a-124">from *position*</span></span>       | <span data-ttu-id="bc06a-125">Especifica o início do intervalo copiado.</span><span class="sxs-lookup"><span data-stu-id="bc06a-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="bc06a-126">Se omitido, a configuração padrão será a posição atual.</span><span class="sxs-lookup"><span data-stu-id="bc06a-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="bc06a-127">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="bc06a-127">to *position*</span></span>         | <span data-ttu-id="bc06a-128">Especifica o fim do intervalo copiado.</span><span class="sxs-lookup"><span data-stu-id="bc06a-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="bc06a-129">Os dados de áudio e vídeo copiados são exclusivos dessa posição.</span><span class="sxs-lookup"><span data-stu-id="bc06a-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="bc06a-130">Se omitido, a configuração padrão será o final do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc06a-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="bc06a-131">*fluxo* de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="bc06a-131">video stream *stream*</span></span> | <span data-ttu-id="bc06a-132">Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="bc06a-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="bc06a-133">Se você usar esse sinalizador e também quiser copiar áudio, também deverá usar o sinalizador "fluxo de áudio".</span><span class="sxs-lookup"><span data-stu-id="bc06a-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="bc06a-134">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão copiados.)</span><span class="sxs-lookup"><span data-stu-id="bc06a-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="bc06a-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="bc06a-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bc06a-136">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="bc06a-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="bc06a-137">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bc06a-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc06a-138">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bc06a-138">Return Value</span></span>

<span data-ttu-id="bc06a-139">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="bc06a-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc06a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc06a-140">Requirements</span></span>



| <span data-ttu-id="bc06a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc06a-141">Requirement</span></span> | <span data-ttu-id="bc06a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="bc06a-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bc06a-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc06a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bc06a-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc06a-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc06a-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc06a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bc06a-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc06a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bc06a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc06a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc06a-148">MCI</span><span class="sxs-lookup"><span data-stu-id="bc06a-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc06a-149">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="bc06a-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

