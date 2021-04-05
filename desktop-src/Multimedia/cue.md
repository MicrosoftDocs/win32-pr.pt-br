---
title: comando de indicação
description: O comando de indicação se prepara para reproduzir ou gravar. Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- comando de indicação multimídia do Windows
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824827"
---
# <a name="cue-command"></a><span data-ttu-id="8c974-105">comando de indicação</span><span class="sxs-lookup"><span data-stu-id="8c974-105">cue command</span></span>

<span data-ttu-id="8c974-106">O comando de indicação se prepara para reproduzir ou gravar.</span><span class="sxs-lookup"><span data-stu-id="8c974-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="8c974-107">Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="8c974-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="8c974-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8c974-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="8c974-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c974-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c974-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8c974-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8c974-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8c974-111">Identifier of an MCI device.</span></span> <span data-ttu-id="8c974-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="8c974-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="8c974-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span><span class="sxs-lookup"><span data-stu-id="8c974-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="8c974-114">Sinalizador que prepara um dispositivo para reprodução ou gravação.</span><span class="sxs-lookup"><span data-stu-id="8c974-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="8c974-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **indicação** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="8c974-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c974-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8c974-116">Value</span></span></th>
<th><span data-ttu-id="8c974-117">Marcar</span><span class="sxs-lookup"><span data-stu-id="8c974-117">Cue</span></span></th>
<th><span data-ttu-id="8c974-118">Marcar</span><span class="sxs-lookup"><span data-stu-id="8c974-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c974-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="8c974-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="8c974-120">input</span><span class="sxs-lookup"><span data-stu-id="8c974-120">input</span></span></li>
<li><span data-ttu-id="8c974-121">noshow</span><span class="sxs-lookup"><span data-stu-id="8c974-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8c974-122">output</span><span class="sxs-lookup"><span data-stu-id="8c974-122">output</span></span></li>
<li><span data-ttu-id="8c974-123">para a <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="8c974-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c974-124">videocassete</span><span class="sxs-lookup"><span data-stu-id="8c974-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="8c974-125">da <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="8c974-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="8c974-126">input</span><span class="sxs-lookup"><span data-stu-id="8c974-126">input</span></span></li>
<li><span data-ttu-id="8c974-127">output</span><span class="sxs-lookup"><span data-stu-id="8c974-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8c974-128">prelance</span><span class="sxs-lookup"><span data-stu-id="8c974-128">preroll</span></span></li>
<li><span data-ttu-id="8c974-129">reverse</span><span class="sxs-lookup"><span data-stu-id="8c974-129">reverse</span></span></li>
<li><span data-ttu-id="8c974-130">para a <em>posição</em></span><span class="sxs-lookup"><span data-stu-id="8c974-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c974-131">waveaudio</span><span class="sxs-lookup"><span data-stu-id="8c974-131">waveaudio</span></span></td>
<td><span data-ttu-id="8c974-132">input</span><span class="sxs-lookup"><span data-stu-id="8c974-132">input</span></span></td>
<td><span data-ttu-id="8c974-133">output</span><span class="sxs-lookup"><span data-stu-id="8c974-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8c974-134">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszInOutTo* e seus significados.</span><span class="sxs-lookup"><span data-stu-id="8c974-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="8c974-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8c974-135">Value</span></span>           | <span data-ttu-id="8c974-136">Significado</span><span class="sxs-lookup"><span data-stu-id="8c974-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c974-137">da *posição*</span><span class="sxs-lookup"><span data-stu-id="8c974-137">from *position*</span></span> | <span data-ttu-id="8c974-138">Indica onde começar.</span><span class="sxs-lookup"><span data-stu-id="8c974-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8c974-139">input</span><span class="sxs-lookup"><span data-stu-id="8c974-139">input</span></span>           | <span data-ttu-id="8c974-140">Prepara para gravação.</span><span class="sxs-lookup"><span data-stu-id="8c974-140">Prepares for recording.</span></span> <span data-ttu-id="8c974-141">Para dispositivos de vídeo digital, esse sinalizador poderá ser omitido se a fonte da apresentação atual já for a entrada externa.</span><span class="sxs-lookup"><span data-stu-id="8c974-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="8c974-142">noshow</span><span class="sxs-lookup"><span data-stu-id="8c974-142">noshow</span></span>          | <span data-ttu-id="8c974-143">Prepara para reproduzir um quadro sem exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="8c974-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="8c974-144">Quando esse sinalizador é especificado, a exibição continua a mostrar a imagem no buffer de quadro, embora seu quadro correspondente não seja a posição atual.</span><span class="sxs-lookup"><span data-stu-id="8c974-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="8c974-145">Um comando de indicação subsequente sem esse sinalizador e sem o sinalizador "to" exibe o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="8c974-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="8c974-146">output</span><span class="sxs-lookup"><span data-stu-id="8c974-146">output</span></span>          | <span data-ttu-id="8c974-147">Prepara para jogar.</span><span class="sxs-lookup"><span data-stu-id="8c974-147">Prepares for playing.</span></span> <span data-ttu-id="8c974-148">Se nenhuma "entrada" nem "saída" for especificada, a configuração padrão será "saída".</span><span class="sxs-lookup"><span data-stu-id="8c974-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="8c974-149">prelance</span><span class="sxs-lookup"><span data-stu-id="8c974-149">preroll</span></span>         | <span data-ttu-id="8c974-150">Move a distância de preversão do *ponto em* diante.</span><span class="sxs-lookup"><span data-stu-id="8c974-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="8c974-151">O ponto de entrada é a posição atual ou a posição especificada pelo sinalizador "de".</span><span class="sxs-lookup"><span data-stu-id="8c974-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="8c974-152">reverse</span><span class="sxs-lookup"><span data-stu-id="8c974-152">reverse</span></span>         | <span data-ttu-id="8c974-153">Indica que a direção da reprodução está em ordem inversa (retroativa).</span><span class="sxs-lookup"><span data-stu-id="8c974-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8c974-154">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="8c974-154">to *position*</span></span>   | <span data-ttu-id="8c974-155">Move o espaço de trabalho para a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="8c974-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="8c974-156">Para dispositivos VCR, esse sinalizador indica onde parar.</span><span class="sxs-lookup"><span data-stu-id="8c974-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="8c974-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="8c974-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8c974-158">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="8c974-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="8c974-159">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="8c974-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="8c974-160">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8c974-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c974-161">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8c974-161">Return Value</span></span>

<span data-ttu-id="8c974-162">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8c974-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c974-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c974-163">Remarks</span></span>

<span data-ttu-id="8c974-164">Embora não seja necessário, emitir o comando de indicação antes de reproduzir ou gravar em alguns dispositivos pode reduzir o atraso antes que o dispositivo inicie a ação.</span><span class="sxs-lookup"><span data-stu-id="8c974-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="8c974-165">Esse comando falhará se a reprodução ou a gravação estiver em andamento ou se o dispositivo estiver em pausa.</span><span class="sxs-lookup"><span data-stu-id="8c974-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="8c974-166">Quando advertência para reprodução (usando a indicação "saída"), emitir o comando [Play](play.md) com o sinalizador "from", "to" ou "Reverse" cancela o comando cue.</span><span class="sxs-lookup"><span data-stu-id="8c974-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="8c974-167">Quando advertência para gravação (usando a indicação de "entrada"), a emissão do comando de [registro](record.md) com o sinalizador "de", "para" ou "inicializar" cancela o comando de indicação.</span><span class="sxs-lookup"><span data-stu-id="8c974-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="8c974-168">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c974-168">Examples</span></span>

<span data-ttu-id="8c974-169">O comando a seguir prepara o dispositivo "mysound" para gravação.</span><span class="sxs-lookup"><span data-stu-id="8c974-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="8c974-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c974-170">Requirements</span></span>



| <span data-ttu-id="8c974-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c974-171">Requirement</span></span> | <span data-ttu-id="8c974-172">Valor</span><span class="sxs-lookup"><span data-stu-id="8c974-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8c974-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c974-173">Minimum supported client</span></span><br/> | <span data-ttu-id="8c974-174">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c974-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c974-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c974-175">Minimum supported server</span></span><br/> | <span data-ttu-id="8c974-176">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c974-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8c974-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c974-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c974-178">MCI</span><span class="sxs-lookup"><span data-stu-id="8c974-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8c974-179">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="8c974-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="8c974-180">reproduzir</span><span class="sxs-lookup"><span data-stu-id="8c974-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="8c974-181">gravável</span><span class="sxs-lookup"><span data-stu-id="8c974-181">record</span></span>](record.md)
</dt> </dl>

 

