---
title: Excluir comando
description: O comando Excluir exclui um segmento de dados de um arquivo. Os dispositivos digital-video e Wave-Audio reconhecem este comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- excluir o comando multimídia do Windows
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824737"
---
# <a name="delete-command"></a><span data-ttu-id="a553e-105">Excluir comando</span><span class="sxs-lookup"><span data-stu-id="a553e-105">delete command</span></span>

<span data-ttu-id="a553e-106">O comando Excluir exclui um segmento de dados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a553e-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="a553e-107">Os dispositivos digital-video e Wave-Audio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="a553e-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="a553e-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a553e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a553e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a553e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a553e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a553e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a553e-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a553e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a553e-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="a553e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a553e-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span><span class="sxs-lookup"><span data-stu-id="a553e-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="a553e-114">Sinalizador que identifica um segmento de dados a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="a553e-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="a553e-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **exclusão** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="a553e-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a553e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a553e-116">Value</span></span></th>
<th><span data-ttu-id="a553e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a553e-117">Meaning</span></span></th>
<th><span data-ttu-id="a553e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a553e-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a553e-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="a553e-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="a553e-120">no <em>retângulo</em></span><span class="sxs-lookup"><span data-stu-id="a553e-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="a553e-121"><em>fluxo</em> de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="a553e-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="a553e-122">da <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="a553e-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a553e-123">para a <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="a553e-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="a553e-124"><em>fluxo</em> de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="a553e-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a553e-125">waveaudio</span><span class="sxs-lookup"><span data-stu-id="a553e-125">waveaudio</span></span></td>
<td><span data-ttu-id="a553e-126">da <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="a553e-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="a553e-127">para a <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="a553e-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a553e-128">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszPosition* e seus significados.</span><span class="sxs-lookup"><span data-stu-id="a553e-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="a553e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a553e-129">Value</span></span>                 | <span data-ttu-id="a553e-130">Significado</span><span class="sxs-lookup"><span data-stu-id="a553e-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a553e-131">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="a553e-131">at *rectangle*</span></span>        | <span data-ttu-id="a553e-132">Especifica a parte de cada quadro excluída.</span><span class="sxs-lookup"><span data-stu-id="a553e-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="a553e-133">Se for omitido, o padrão será o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="a553e-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="a553e-134">Quando esse item é especificado, os quadros não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="a553e-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="a553e-135">Em vez disso, a área dentro do retângulo se torna preta.</span><span class="sxs-lookup"><span data-stu-id="a553e-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="a553e-136">*fluxo* de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="a553e-136">audio stream *stream*</span></span> | <span data-ttu-id="a553e-137">Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="a553e-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="a553e-138">Se você usar esse sinalizador e também quiser excluir o vídeo, também deverá usar o sinalizador "fluxo de vídeo".</span><span class="sxs-lookup"><span data-stu-id="a553e-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="a553e-139">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão excluídos.)</span><span class="sxs-lookup"><span data-stu-id="a553e-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="a553e-140">da *posição*</span><span class="sxs-lookup"><span data-stu-id="a553e-140">from *position*</span></span>       | <span data-ttu-id="a553e-141">Especifica a posição na qual começa a exclusão.</span><span class="sxs-lookup"><span data-stu-id="a553e-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="a553e-142">Se esse sinalizador for omitido, a exclusão começará na posição atual.</span><span class="sxs-lookup"><span data-stu-id="a553e-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="a553e-143">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="a553e-143">to *position*</span></span>         | <span data-ttu-id="a553e-144">Especifica a posição na qual termina a exclusão.</span><span class="sxs-lookup"><span data-stu-id="a553e-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="a553e-145">Se esse sinalizador for omitido, a exclusão continuará no final do conteúdo ou espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a553e-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="a553e-146">*fluxo* de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="a553e-146">video stream *stream*</span></span> | <span data-ttu-id="a553e-147">Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando.</span><span class="sxs-lookup"><span data-stu-id="a553e-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="a553e-148">Se você usar esse sinalizador e também quiser excluir áudio, também deverá usar o sinalizador "fluxo de áudio".</span><span class="sxs-lookup"><span data-stu-id="a553e-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="a553e-149">(Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão excluídos.)</span><span class="sxs-lookup"><span data-stu-id="a553e-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a553e-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a553e-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a553e-151">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="a553e-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a553e-152">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a553e-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="a553e-153">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a553e-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a553e-154">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a553e-154">Return Value</span></span>

<span data-ttu-id="a553e-155">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a553e-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a553e-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="a553e-156">Remarks</span></span>

<span data-ttu-id="a553e-157">Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="a553e-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="a553e-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a553e-158">Examples</span></span>

<span data-ttu-id="a553e-159">O comando a seguir exclui os dados de forma de onda-áudio de 1 milissegundo a 900 milissegundos (supondo que o formato de hora seja definido como milissegundos).</span><span class="sxs-lookup"><span data-stu-id="a553e-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="a553e-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a553e-160">Requirements</span></span>



| <span data-ttu-id="a553e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a553e-161">Requirement</span></span> | <span data-ttu-id="a553e-162">Valor</span><span class="sxs-lookup"><span data-stu-id="a553e-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a553e-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a553e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a553e-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a553e-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a553e-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a553e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a553e-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a553e-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a553e-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="a553e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a553e-168">MCI</span><span class="sxs-lookup"><span data-stu-id="a553e-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a553e-169">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="a553e-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a553e-170">set</span><span class="sxs-lookup"><span data-stu-id="a553e-170">set</span></span>](set.md)
</dt> </dl>

 

