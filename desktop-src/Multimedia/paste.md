---
title: comando colar
description: O comando Paste copia o conteúdo da área de transferência no espaço de trabalho. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- comando colar multimídia do Windows
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009054"
---
# <a name="paste-command"></a><span data-ttu-id="f6cc4-105">comando colar</span><span class="sxs-lookup"><span data-stu-id="f6cc4-105">paste command</span></span>

<span data-ttu-id="f6cc4-106">O comando Paste copia o conteúdo da área de transferência no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="f6cc4-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="f6cc4-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f6cc4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6cc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6cc4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f6cc4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f6cc4-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f6cc4-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f6cc4-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span><span class="sxs-lookup"><span data-stu-id="f6cc4-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="f6cc4-114">Um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-114">One or more of the following flags.</span></span>



| <span data-ttu-id="f6cc4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f6cc4-115">Value</span></span>                 | <span data-ttu-id="f6cc4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f6cc4-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6cc4-117">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="f6cc4-117">at *rectangle*</span></span>        | <span data-ttu-id="f6cc4-118">Especifica o local dentro do quadro onde os dados são colados.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="f6cc4-119">O canto superior esquerdo do *retângulo* corresponde ao canto superior esquerdo dos dados adicionados.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="f6cc4-120">Se o retângulo tiver um tamanho diferente de zero em X ou Y, o conteúdo da área de transferência será dimensionado nessas dimensões quando eles forem colados no quadro.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="f6cc4-121">Se omitido, o *retângulo* assume como padrão o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="f6cc4-122">Se esse sinalizador for especificado no modo de "inserção" (o padrão), qualquer região fora do retângulo será pintada como uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="f6cc4-123">*fluxo* de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="f6cc4-123">audio stream *stream*</span></span> | <span data-ttu-id="f6cc4-124">Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="f6cc4-125">Se houver apenas um fluxo de áudio na área de transferência, os dados de áudio serão colados no *fluxo* designado.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="f6cc4-126">Se houver mais de um fluxo de áudio na área de transferência, o *fluxo* indicará o número inicial para as sequências de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="f6cc4-127">Se você usar esse sinalizador e também quiser colar o vídeo, também deverá usar o sinalizador "fluxo de vídeo".</span><span class="sxs-lookup"><span data-stu-id="f6cc4-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="f6cc4-128">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados e manterão seus números de fluxo originais.)</span><span class="sxs-lookup"><span data-stu-id="f6cc4-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="f6cc4-129">insert</span><span class="sxs-lookup"><span data-stu-id="f6cc4-129">insert</span></span>                | <span data-ttu-id="f6cc4-130">Especifica que os dados são inseridos no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="f6cc4-131">Todos os dados após o ponto de inserção são movidos para frente no espaço de trabalho para liberar espaço.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="f6cc4-132">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f6cc4-133">overwrite</span><span class="sxs-lookup"><span data-stu-id="f6cc4-133">overwrite</span></span>             | <span data-ttu-id="f6cc4-134">Especifica que os dados são copiados no espaço de trabalho por meio da gravação de todos os dados existentes após o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="f6cc4-135">Os sinalizadores "Inserir" e "substituir" afetam se os quadros são destruídos ou movidos durante a operação de colagem, e não como os dados são colados dentro de cada quadro.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="f6cc4-136">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="f6cc4-136">to *position*</span></span>         | <span data-ttu-id="f6cc4-137">Especifica a posição no espaço de trabalho em que os dados são colados.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="f6cc4-138">Se for omitido, o padrão será a posição atual.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f6cc4-139">*fluxo* de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="f6cc4-139">video stream *stream*</span></span> | <span data-ttu-id="f6cc4-140">Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="f6cc4-141">Se houver apenas um fluxo de vídeo na área de transferência, os dados de vídeo serão colados no *fluxo* designado.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="f6cc4-142">Se houver mais de um fluxo de vídeo na área de transferência, o *fluxo* indicará o número inicial para as sequências de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="f6cc4-143">Se você usar esse sinalizador e também quiser colar o áudio, também deverá usar o sinalizador "fluxo de áudio".</span><span class="sxs-lookup"><span data-stu-id="f6cc4-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="f6cc4-144">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados e manterão seus números de fluxo originais.)</span><span class="sxs-lookup"><span data-stu-id="f6cc4-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="f6cc4-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f6cc4-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f6cc4-146">Pode ser "Wait", "Notify", "Test" ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="f6cc4-147">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f6cc4-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6cc4-148">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f6cc4-148">Return Value</span></span>

<span data-ttu-id="f6cc4-149">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6cc4-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6cc4-150">Remarks</span></span>

<span data-ttu-id="f6cc4-151">Não há sinais presentes nos dados copiados da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="f6cc4-152">A alteração se torna permanente somente quando os dados são explicitamente salvos; no entanto, a reprodução age como se os dados tiverem sido adicionados.</span><span class="sxs-lookup"><span data-stu-id="f6cc4-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6cc4-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6cc4-153">Requirements</span></span>



| <span data-ttu-id="f6cc4-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6cc4-154">Requirement</span></span> | <span data-ttu-id="f6cc4-155">Valor</span><span class="sxs-lookup"><span data-stu-id="f6cc4-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f6cc4-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6cc4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f6cc4-157">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6cc4-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f6cc4-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6cc4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f6cc4-159">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6cc4-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f6cc4-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6cc4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6cc4-161">MCI</span><span class="sxs-lookup"><span data-stu-id="f6cc4-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f6cc4-162">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="f6cc4-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

