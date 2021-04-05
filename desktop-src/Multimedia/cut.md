---
title: comando Recortar
description: O comando Recortar remove dados do espaço de trabalho e os copia para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- comando Recortar multimídia do Windows
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918956"
---
# <a name="cut-command"></a><span data-ttu-id="ec6d7-105">comando Recortar</span><span class="sxs-lookup"><span data-stu-id="ec6d7-105">cut command</span></span>

<span data-ttu-id="ec6d7-106">O comando Recortar remove dados do espaço de trabalho e os copia para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="ec6d7-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ec6d7-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ec6d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec6d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec6d7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ec6d7-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ec6d7-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-111">Identifier of an MCI device.</span></span> <span data-ttu-id="ec6d7-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ec6d7-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="ec6d7-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="ec6d7-114">Um dos sinalizadores a seguir que identificam o item a ser recortado.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="ec6d7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ec6d7-115">Value</span></span>                 | <span data-ttu-id="ec6d7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ec6d7-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6d7-117">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="ec6d7-117">at *rectangle*</span></span>        | <span data-ttu-id="ec6d7-118">Especifica a parte de cada corte de quadro.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="ec6d7-119">Se for omitido, o padrão será o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="ec6d7-120">Quando esse item é especificado, os quadros não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="ec6d7-121">Em vez disso, a área dentro do retângulo se torna preta.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="ec6d7-122">*fluxo* de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="ec6d7-122">audio stream *stream*</span></span> | <span data-ttu-id="ec6d7-123">Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="ec6d7-124">Se você usar esse sinalizador e também quiser recortar o vídeo, também deverá usar o sinalizador "fluxo de vídeo".</span><span class="sxs-lookup"><span data-stu-id="ec6d7-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="ec6d7-125">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão recortados.)</span><span class="sxs-lookup"><span data-stu-id="ec6d7-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="ec6d7-126">da *posição*</span><span class="sxs-lookup"><span data-stu-id="ec6d7-126">from *position*</span></span>       | <span data-ttu-id="ec6d7-127">Especifica o início do intervalo de recorte.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="ec6d7-128">Se for omitido, o padrão será a posição atual.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="ec6d7-129">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="ec6d7-129">to *position*</span></span>         | <span data-ttu-id="ec6d7-130">Especifica o fim do intervalo de recorte.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="ec6d7-131">Os dados de áudio e vídeo recortados são exclusivos dessa posição.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="ec6d7-132">Se omitido, o padrão será o final do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="ec6d7-133">*fluxo* de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="ec6d7-133">video stream *stream*</span></span> | <span data-ttu-id="ec6d7-134">Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="ec6d7-135">Se você usar esse sinalizador e também quiser cortar o áudio, também deverá usar o sinalizador "fluxo de áudio".</span><span class="sxs-lookup"><span data-stu-id="ec6d7-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="ec6d7-136">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão recortados.)</span><span class="sxs-lookup"><span data-stu-id="ec6d7-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="ec6d7-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="ec6d7-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ec6d7-138">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="ec6d7-139">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ec6d7-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec6d7-140">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ec6d7-140">Return Value</span></span>

<span data-ttu-id="ec6d7-141">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec6d7-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec6d7-142">Remarks</span></span>

<span data-ttu-id="ec6d7-143">A alteração se torna permanente somente quando os dados são explicitamente salvos; no entanto, a reprodução funciona como se os dados tiverem sido removidos.</span><span class="sxs-lookup"><span data-stu-id="ec6d7-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec6d7-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec6d7-144">Requirements</span></span>



| <span data-ttu-id="ec6d7-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec6d7-145">Requirement</span></span> | <span data-ttu-id="ec6d7-146">Valor</span><span class="sxs-lookup"><span data-stu-id="ec6d7-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ec6d7-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec6d7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ec6d7-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec6d7-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ec6d7-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec6d7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ec6d7-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec6d7-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ec6d7-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec6d7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6d7-152">MCI</span><span class="sxs-lookup"><span data-stu-id="ec6d7-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ec6d7-153">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="ec6d7-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

