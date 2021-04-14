---
title: comando de busca
description: O comando Seek move para a posição especificada e para. CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- Multimídia do Windows de comando de busca
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369249"
---
# <a name="seek-command"></a><span data-ttu-id="841b9-105">comando de busca</span><span class="sxs-lookup"><span data-stu-id="841b9-105">seek command</span></span>

<span data-ttu-id="841b9-106">O comando Seek move para a posição especificada e para.</span><span class="sxs-lookup"><span data-stu-id="841b9-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="841b9-107">CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="841b9-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="841b9-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="841b9-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="841b9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="841b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841b9-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="841b9-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="841b9-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="841b9-111">Identifier of an MCI device.</span></span> <span data-ttu-id="841b9-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="841b9-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="841b9-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span><span class="sxs-lookup"><span data-stu-id="841b9-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="841b9-114">Sinalizador para mover para uma posição especificada.</span><span class="sxs-lookup"><span data-stu-id="841b9-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="841b9-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **busca** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="841b9-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="841b9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="841b9-116">Value</span></span>        | <span data-ttu-id="841b9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="841b9-117">Meaning</span></span>                          | <span data-ttu-id="841b9-118">Significado</span><span class="sxs-lookup"><span data-stu-id="841b9-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="841b9-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="841b9-119">cdaudio</span></span>      | <span data-ttu-id="841b9-120">até a *posição* final</span><span class="sxs-lookup"><span data-stu-id="841b9-120">to end to *position*</span></span>             | <span data-ttu-id="841b9-121">para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-121">to start</span></span>                     |
| <span data-ttu-id="841b9-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="841b9-122">digitalvideo</span></span> | <span data-ttu-id="841b9-123">até a *posição* final</span><span class="sxs-lookup"><span data-stu-id="841b9-123">to end to *position*</span></span>             | <span data-ttu-id="841b9-124">para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-124">to start</span></span>                     |
| <span data-ttu-id="841b9-125">sequenciador</span><span class="sxs-lookup"><span data-stu-id="841b9-125">sequencer</span></span>    | <span data-ttu-id="841b9-126">até a *posição* final</span><span class="sxs-lookup"><span data-stu-id="841b9-126">to end to *position*</span></span>             | <span data-ttu-id="841b9-127">para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-127">to start</span></span>                     |
| <span data-ttu-id="841b9-128">videocassete</span><span class="sxs-lookup"><span data-stu-id="841b9-128">vcr</span></span>          | <span data-ttu-id="841b9-129">em *\_ número* de marca de *tempo* invertido</span><span class="sxs-lookup"><span data-stu-id="841b9-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="841b9-130">até a *posição* final para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-130">to end to *position* to start</span></span> |
| <span data-ttu-id="841b9-131">videodisc</span><span class="sxs-lookup"><span data-stu-id="841b9-131">videodisc</span></span>    | <span data-ttu-id="841b9-132">reverter para fim</span><span class="sxs-lookup"><span data-stu-id="841b9-132">reverse to end</span></span>                   | <span data-ttu-id="841b9-133">para *posição* para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-133">to *position* to start</span></span>        |
| <span data-ttu-id="841b9-134">waveaudio</span><span class="sxs-lookup"><span data-stu-id="841b9-134">waveaudio</span></span>    | <span data-ttu-id="841b9-135">até a *posição* final</span><span class="sxs-lookup"><span data-stu-id="841b9-135">to end to *position*</span></span>             | <span data-ttu-id="841b9-136">para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-136">to start</span></span>                     |



 

<span data-ttu-id="841b9-137">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszSeekFlags** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="841b9-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="841b9-138">Valor</span><span class="sxs-lookup"><span data-stu-id="841b9-138">Value</span></span>            | <span data-ttu-id="841b9-139">Significado</span><span class="sxs-lookup"><span data-stu-id="841b9-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="841b9-140">às *vezes*</span><span class="sxs-lookup"><span data-stu-id="841b9-140">at *time*</span></span>        | <span data-ttu-id="841b9-141">Indica quando o dispositivo deve começar a executar este comando ou, se o dispositivo tiver sido cued, quando o comando cued for iniciado.</span><span class="sxs-lookup"><span data-stu-id="841b9-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="841b9-142">Para obter mais informações, consulte o comando [Cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="841b9-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="841b9-143">marcar *\_ número* de marca</span><span class="sxs-lookup"><span data-stu-id="841b9-143">mark *mark\_num*</span></span> | <span data-ttu-id="841b9-144">Busca a marca relativa indicada por *Mark \_ num*, que deve ser um valor inteiro positivo.</span><span class="sxs-lookup"><span data-stu-id="841b9-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="841b9-145">Marcas são sinais gravados na fita VCR usando o comando [Mark](mark.md) e são usados para pesquisa de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="841b9-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="841b9-146">reverse</span><span class="sxs-lookup"><span data-stu-id="841b9-146">reverse</span></span>          | <span data-ttu-id="841b9-147">Indica que a direção de busca em VCRs e CAV videodiscs é retroativa.</span><span class="sxs-lookup"><span data-stu-id="841b9-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="841b9-148">Esse sinalizador é inválido se o sinalizador "to" for especificado.</span><span class="sxs-lookup"><span data-stu-id="841b9-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="841b9-149">Para VCRs, esse sinalizador deve ser usado com o sinalizador "Mark".</span><span class="sxs-lookup"><span data-stu-id="841b9-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="841b9-150">para o fim</span><span class="sxs-lookup"><span data-stu-id="841b9-150">to end</span></span>           | <span data-ttu-id="841b9-151">Busca o fim do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="841b9-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="841b9-152">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="841b9-152">to *position*</span></span>    | <span data-ttu-id="841b9-153">Especifica a posição para parar a busca.</span><span class="sxs-lookup"><span data-stu-id="841b9-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="841b9-154">Para dispositivos **cdaudio** , o MCI retornará um erro fora do intervalo se a posição especificada for maior do que o comprimento do disco.</span><span class="sxs-lookup"><span data-stu-id="841b9-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="841b9-155">para iniciar</span><span class="sxs-lookup"><span data-stu-id="841b9-155">to start</span></span>         | <span data-ttu-id="841b9-156">Busca o início do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="841b9-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="841b9-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="841b9-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="841b9-158">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="841b9-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="841b9-159">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="841b9-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="841b9-160">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="841b9-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841b9-161">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="841b9-161">Return Value</span></span>

<span data-ttu-id="841b9-162">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="841b9-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="841b9-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="841b9-163">Remarks</span></span>

<span data-ttu-id="841b9-164">Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="841b9-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="841b9-165">Os dispositivos de vídeo digital dão suporte a dois modos de busca, que podem ser alterados usando o comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="841b9-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="841b9-166">O modo "Seek exactly on" faz com que o comando Seek seja movido para o quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="841b9-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="841b9-167">O modo "Seek exactly off" faz com que o comando Seek se mova para o quadro-chave mais próximo antes do quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="841b9-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="841b9-168">Se um dispositivo de áudio de CD estiver sendo executado quando o comando de busca for emitido, a reprodução será interrompida.</span><span class="sxs-lookup"><span data-stu-id="841b9-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="841b9-169">Quando o comando Seek é emitido com um dispositivo VIDEODISC, o dispositivo pesquisa usando Fast forward ou Fast reverso com vídeo e áudio desligados.</span><span class="sxs-lookup"><span data-stu-id="841b9-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="841b9-170">Quando o comando Seek é emitido com um dispositivo wave-Audio, o comportamento depende do tamanho da amostra.</span><span class="sxs-lookup"><span data-stu-id="841b9-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="841b9-171">Se o tamanho da amostra for de 16 bits ou maior, o Seek passará para o início do exemplo mais próximo quando uma posição especificada não coincidir com o início de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="841b9-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="841b9-172">Exemplos</span><span class="sxs-lookup"><span data-stu-id="841b9-172">Examples</span></span>

<span data-ttu-id="841b9-173">O comando a seguir procura o início do arquivo de mídia associado ao dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="841b9-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="841b9-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="841b9-174">Requirements</span></span>



| <span data-ttu-id="841b9-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="841b9-175">Requirement</span></span> | <span data-ttu-id="841b9-176">Valor</span><span class="sxs-lookup"><span data-stu-id="841b9-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="841b9-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="841b9-177">Minimum supported client</span></span><br/> | <span data-ttu-id="841b9-178">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="841b9-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="841b9-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="841b9-179">Minimum supported server</span></span><br/> | <span data-ttu-id="841b9-180">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="841b9-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="841b9-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="841b9-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841b9-182">MCI</span><span class="sxs-lookup"><span data-stu-id="841b9-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="841b9-183">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="841b9-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="841b9-184">advertência</span><span class="sxs-lookup"><span data-stu-id="841b9-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="841b9-185">marca</span><span class="sxs-lookup"><span data-stu-id="841b9-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="841b9-186">set</span><span class="sxs-lookup"><span data-stu-id="841b9-186">set</span></span>](set.md)
</dt> </dl>

 

