---
title: comando gravar
description: O comando gravar começa a gravar dados. Os dispositivos VCR e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- gravar comando multimídia do Windows
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824182"
---
# <a name="record-command"></a><span data-ttu-id="38fdd-106">comando gravar</span><span class="sxs-lookup"><span data-stu-id="38fdd-106">record command</span></span>

<span data-ttu-id="38fdd-107">O comando gravar começa a gravar dados.</span><span class="sxs-lookup"><span data-stu-id="38fdd-107">The record command starts recording data.</span></span> <span data-ttu-id="38fdd-108">Os dispositivos VCR e Wave-Audio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="38fdd-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="38fdd-109">Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.</span><span class="sxs-lookup"><span data-stu-id="38fdd-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="38fdd-110">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="38fdd-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="38fdd-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38fdd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38fdd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="38fdd-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="38fdd-113">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="38fdd-113">Identifier of an MCI device.</span></span> <span data-ttu-id="38fdd-114">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="38fdd-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="38fdd-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span><span class="sxs-lookup"><span data-stu-id="38fdd-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="38fdd-116">Sinalizador para gravar dados.</span><span class="sxs-lookup"><span data-stu-id="38fdd-116">Flag for recording data.</span></span> <span data-ttu-id="38fdd-117">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **registro** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="38fdd-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="38fdd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="38fdd-118">Value</span></span>        | <span data-ttu-id="38fdd-119">Significado</span><span class="sxs-lookup"><span data-stu-id="38fdd-119">Meaning</span></span>                                                | <span data-ttu-id="38fdd-120">Significado</span><span class="sxs-lookup"><span data-stu-id="38fdd-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="38fdd-121">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="38fdd-121">digitalvideo</span></span> | <span data-ttu-id="38fdd-122">*fluxo* de fluxo de áudio no *retângulo* da espera de *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="38fdd-123">inserir substituição para *posicionar* *fluxo* de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="38fdd-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="38fdd-124">sequenciador</span><span class="sxs-lookup"><span data-stu-id="38fdd-124">sequencer</span></span>    | <span data-ttu-id="38fdd-125">da *posição* de inserção</span><span class="sxs-lookup"><span data-stu-id="38fdd-125">from *position* insert</span></span>                                  | <span data-ttu-id="38fdd-126">substituir na *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="38fdd-127">videocassete</span><span class="sxs-lookup"><span data-stu-id="38fdd-127">vcr</span></span>          | <span data-ttu-id="38fdd-128">no *momento* da inicialização da *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="38fdd-129">inserir substituição na *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="38fdd-130">waveaudio</span><span class="sxs-lookup"><span data-stu-id="38fdd-130">waveaudio</span></span>    | <span data-ttu-id="38fdd-131">da *posição* de inserção</span><span class="sxs-lookup"><span data-stu-id="38fdd-131">from *position* insert</span></span>                                  | <span data-ttu-id="38fdd-132">substituir na *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="38fdd-133">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRecordFlags** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="38fdd-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="38fdd-134">Valor</span><span class="sxs-lookup"><span data-stu-id="38fdd-134">Value</span></span>                 | <span data-ttu-id="38fdd-135">Significado</span><span class="sxs-lookup"><span data-stu-id="38fdd-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38fdd-136">no *retângulo*</span><span class="sxs-lookup"><span data-stu-id="38fdd-136">at *rectangle*</span></span>        | <span data-ttu-id="38fdd-137">Especifica uma região retangular da entrada externa usada como a origem dos pixels compactados e salvos.</span><span class="sxs-lookup"><span data-stu-id="38fdd-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="38fdd-138">Se não for especificado, o retângulo usa como padrão o retângulo especificado para [colocar](put.md) "vídeo".</span><span class="sxs-lookup"><span data-stu-id="38fdd-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="38fdd-139">Quando ele é definido de forma diferente do retângulo de "vídeo", a imagem exibida não é o que é registrado.</span><span class="sxs-lookup"><span data-stu-id="38fdd-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="38fdd-140">às *vezes*</span><span class="sxs-lookup"><span data-stu-id="38fdd-140">at *time*</span></span>             | <span data-ttu-id="38fdd-141">Indica quando o dispositivo deve começar a executar este comando ou, se o dispositivo tiver sido cued, quando o comando cued for iniciado.</span><span class="sxs-lookup"><span data-stu-id="38fdd-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="38fdd-142">Para obter mais informações, consulte o comando [Cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="38fdd-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="38fdd-143">*fluxo* de fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="38fdd-143">audio stream *stream*</span></span> | <span data-ttu-id="38fdd-144">Especifica o fluxo de áudio usado para gravação.</span><span class="sxs-lookup"><span data-stu-id="38fdd-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="38fdd-145">Se esse sinalizador não for especificado e o formato de arquivo não definir um padrão, ele será gravado no fluxo que é fisicamente primeiro.</span><span class="sxs-lookup"><span data-stu-id="38fdd-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="38fdd-146">da *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-146">from *position*</span></span>       | <span data-ttu-id="38fdd-147">Especifica uma posição inicial para a gravação.</span><span class="sxs-lookup"><span data-stu-id="38fdd-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="38fdd-148">Se o sinalizador "from" não for especificado, o dispositivo começará a gravar na posição atual.</span><span class="sxs-lookup"><span data-stu-id="38fdd-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="38fdd-149">bloqueio</span><span class="sxs-lookup"><span data-stu-id="38fdd-149">hold</span></span>                  | <span data-ttu-id="38fdd-150">Congela a imagem quando a gravação termina em vez de mostrar o vídeo ao vivo.</span><span class="sxs-lookup"><span data-stu-id="38fdd-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="38fdd-151">Quando a gravação é interrompida, um comando "arquivo" de [Monitor](monitor.md) automático é executado.</span><span class="sxs-lookup"><span data-stu-id="38fdd-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="38fdd-152">Para retornar ao vídeo ao vivo, emita o comando "Input" do **Monitor** .</span><span class="sxs-lookup"><span data-stu-id="38fdd-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="38fdd-153">inicializar</span><span class="sxs-lookup"><span data-stu-id="38fdd-153">initialize</span></span>            | <span data-ttu-id="38fdd-154">Inicialize a fita (mídia), que envolve a gravação de código de paficação (se possível) para vídeo e áudio em branco.</span><span class="sxs-lookup"><span data-stu-id="38fdd-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="38fdd-155">Esse comando poderá levar várias horas se a fita inteira precisar ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="38fdd-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="38fdd-156">insert</span><span class="sxs-lookup"><span data-stu-id="38fdd-156">insert</span></span>                | <span data-ttu-id="38fdd-157">Especifica que novos dados são adicionados ao arquivo na posição atual.</span><span class="sxs-lookup"><span data-stu-id="38fdd-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="38fdd-158">overwrite</span><span class="sxs-lookup"><span data-stu-id="38fdd-158">overwrite</span></span>             | <span data-ttu-id="38fdd-159">Especifica que novos dados substituirão os dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="38fdd-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="38fdd-160">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="38fdd-160">to *position*</span></span>         | <span data-ttu-id="38fdd-161">Especifica uma posição final para a gravação.</span><span class="sxs-lookup"><span data-stu-id="38fdd-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="38fdd-162">Se o sinalizador "to" não for especificado, o dispositivo será registros até receber um comando [Stop](stop.md) ou [Pause](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="38fdd-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="38fdd-163">*fluxo* de fluxo de vídeo</span><span class="sxs-lookup"><span data-stu-id="38fdd-163">video stream *stream*</span></span> | <span data-ttu-id="38fdd-164">Especifica o fluxo de vídeo usado para gravação.</span><span class="sxs-lookup"><span data-stu-id="38fdd-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="38fdd-165">Se isso não for especificado e o formato de arquivo não definir um padrão, ele será gravado no fluxo que é fisicamente primeiro.</span><span class="sxs-lookup"><span data-stu-id="38fdd-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="38fdd-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="38fdd-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="38fdd-167">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="38fdd-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="38fdd-168">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="38fdd-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="38fdd-169">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="38fdd-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38fdd-170">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="38fdd-170">Return Value</span></span>

<span data-ttu-id="38fdd-171">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="38fdd-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="38fdd-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="38fdd-172">Remarks</span></span>

<span data-ttu-id="38fdd-173">A gravação é interrompida quando um comando [Stop](stop.md) ou [Pause](pause.md) é emitido.</span><span class="sxs-lookup"><span data-stu-id="38fdd-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="38fdd-174">Para o driver MCIWAVE, todos os dados gravados após a abertura de um arquivo serão descartados se o arquivo for fechado sem salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="38fdd-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="38fdd-175">Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="38fdd-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="38fdd-176">As faixas a serem registradas são especificadas pelo comando [SetCode](settimecode.md) "Record", defina os comandos "montar registro", [setvideo](setvideo.md) "registro" e "registro" de conjunto de [áudio](setaudio.md) .</span><span class="sxs-lookup"><span data-stu-id="38fdd-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="38fdd-177">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38fdd-177">Examples</span></span>

<span data-ttu-id="38fdd-178">O comando a seguir inicia a gravação na posição atual.</span><span class="sxs-lookup"><span data-stu-id="38fdd-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="38fdd-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38fdd-179">Requirements</span></span>



| <span data-ttu-id="38fdd-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="38fdd-180">Requirement</span></span> | <span data-ttu-id="38fdd-181">Valor</span><span class="sxs-lookup"><span data-stu-id="38fdd-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="38fdd-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38fdd-182">Minimum supported client</span></span><br/> | <span data-ttu-id="38fdd-183">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38fdd-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="38fdd-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38fdd-184">Minimum supported server</span></span><br/> | <span data-ttu-id="38fdd-185">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38fdd-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="38fdd-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="38fdd-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fdd-187">MCI</span><span class="sxs-lookup"><span data-stu-id="38fdd-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="38fdd-188">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="38fdd-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="38fdd-189">advertência</span><span class="sxs-lookup"><span data-stu-id="38fdd-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="38fdd-190">monitor</span><span class="sxs-lookup"><span data-stu-id="38fdd-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="38fdd-191">pause</span><span class="sxs-lookup"><span data-stu-id="38fdd-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="38fdd-192">Posicione</span><span class="sxs-lookup"><span data-stu-id="38fdd-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="38fdd-193">set</span><span class="sxs-lookup"><span data-stu-id="38fdd-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="38fdd-194">SetAudio</span><span class="sxs-lookup"><span data-stu-id="38fdd-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="38fdd-195">SetCode</span><span class="sxs-lookup"><span data-stu-id="38fdd-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="38fdd-196">setvideo</span><span class="sxs-lookup"><span data-stu-id="38fdd-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="38fdd-197">stop</span><span class="sxs-lookup"><span data-stu-id="38fdd-197">stop</span></span>](stop.md)
</dt> </dl>

 

