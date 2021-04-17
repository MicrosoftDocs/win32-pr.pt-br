---
title: comando Play
description: O comando Play começa a reproduzir um dispositivo. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- reproduzir multimídia do Windows do comando
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758747"
---
# <a name="play-command"></a><span data-ttu-id="f498f-105">comando Play</span><span class="sxs-lookup"><span data-stu-id="f498f-105">play command</span></span>

<span data-ttu-id="f498f-106">O comando Play começa a reproduzir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f498f-106">The play command starts playing a device.</span></span> <span data-ttu-id="f498f-107">CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f498f-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="f498f-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f498f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f498f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f498f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f498f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f498f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f498f-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f498f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f498f-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="f498f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f498f-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span><span class="sxs-lookup"><span data-stu-id="f498f-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f498f-114">Sinalizador para reproduzir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f498f-114">Flag for playing a device.</span></span> <span data-ttu-id="f498f-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Play** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="f498f-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="f498f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f498f-116">Value</span></span>        | <span data-ttu-id="f498f-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f498f-117">Meaning</span></span>                          | <span data-ttu-id="f498f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f498f-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="f498f-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="f498f-119">cdaudio</span></span>      | <span data-ttu-id="f498f-120">da *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-120">from *position*</span></span>                  | <span data-ttu-id="f498f-121">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-121">to *position*</span></span>                     |
| <span data-ttu-id="f498f-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="f498f-122">digitalvideo</span></span> | <span data-ttu-id="f498f-123">da *posição* de tela inteira repetir</span><span class="sxs-lookup"><span data-stu-id="f498f-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="f498f-124">reverter para a janela de *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="f498f-125">sequenciador</span><span class="sxs-lookup"><span data-stu-id="f498f-125">sequencer</span></span>    | <span data-ttu-id="f498f-126">da *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-126">from *position*</span></span>                  | <span data-ttu-id="f498f-127">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-127">to *position*</span></span>                     |
| <span data-ttu-id="f498f-128">videocassete</span><span class="sxs-lookup"><span data-stu-id="f498f-128">vcr</span></span>          | <span data-ttu-id="f498f-129">às *vezes* a partir da *posição* inversa</span><span class="sxs-lookup"><span data-stu-id="f498f-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="f498f-130">Digitalizar para *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-130">scan to *position*</span></span>                |
| <span data-ttu-id="f498f-131">videodisc</span><span class="sxs-lookup"><span data-stu-id="f498f-131">videodisc</span></span>    | <span data-ttu-id="f498f-132">rápida da verificação reversa de *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="f498f-133">menor velocidade do *inteiro* para *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="f498f-134">waveaudio</span><span class="sxs-lookup"><span data-stu-id="f498f-134">waveaudio</span></span>    | <span data-ttu-id="f498f-135">da *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-135">from *position*</span></span>                  | <span data-ttu-id="f498f-136">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-136">to *position*</span></span>                     |



 

<span data-ttu-id="f498f-137">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszPlayFlags** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="f498f-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="f498f-138">Valor</span><span class="sxs-lookup"><span data-stu-id="f498f-138">Value</span></span>           | <span data-ttu-id="f498f-139">Significado</span><span class="sxs-lookup"><span data-stu-id="f498f-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f498f-140">às *vezes*</span><span class="sxs-lookup"><span data-stu-id="f498f-140">at *time*</span></span>       | <span data-ttu-id="f498f-141">Indica quando o dispositivo deve começar a executar este comando ou, se o dispositivo tiver sido cued, quando o comando cued for iniciado.</span><span class="sxs-lookup"><span data-stu-id="f498f-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="f498f-142">Para obter mais informações, consulte o comando [Cue](cue.md) .</span><span class="sxs-lookup"><span data-stu-id="f498f-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f498f-143">rápido</span><span class="sxs-lookup"><span data-stu-id="f498f-143">fast</span></span>            | <span data-ttu-id="f498f-144">Indica que o dispositivo deve ser executado mais rápido do que o normal.</span><span class="sxs-lookup"><span data-stu-id="f498f-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="f498f-145">Para determinar a velocidade exata em um VIDEODISC Player, use o sinalizador "velocidade" do comando de [status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="f498f-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="f498f-146">Para especificar a velocidade mais precisamente, use o sinalizador "velocidade" desse comando.</span><span class="sxs-lookup"><span data-stu-id="f498f-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="f498f-147">da *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-147">from *position*</span></span> | <span data-ttu-id="f498f-148">Especifica uma posição inicial para a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f498f-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="f498f-149">Se o sinalizador "from" não for especificado, a reprodução começará na posição atual.</span><span class="sxs-lookup"><span data-stu-id="f498f-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="f498f-150">Para dispositivos **cdaudio** , se a posição "de" for maior que a posição final do disco, ou se a posição "de" for maior que a posição "para", o driver retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f498f-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="f498f-151">Para dispositivos **VIDEODISC** , as posições padrão estão em quadros para discos CAV e em horas, minutos e segundos para discos CLV.</span><span class="sxs-lookup"><span data-stu-id="f498f-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="f498f-152">tela inteira</span><span class="sxs-lookup"><span data-stu-id="f498f-152">fullscreen</span></span>      | <span data-ttu-id="f498f-153">Especifica que uma exibição de tela inteira deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="f498f-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="f498f-154">Use este sinalizador somente ao reproduzir arquivos compactados.</span><span class="sxs-lookup"><span data-stu-id="f498f-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="f498f-155">(Arquivos não compactados não serão exibidos em tela inteira.)</span><span class="sxs-lookup"><span data-stu-id="f498f-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f498f-156">Pete</span><span class="sxs-lookup"><span data-stu-id="f498f-156">repeat</span></span>          | <span data-ttu-id="f498f-157">Especifica que a reprodução deve ser reiniciada quando o final do conteúdo é atingido.</span><span class="sxs-lookup"><span data-stu-id="f498f-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f498f-158">reverse</span><span class="sxs-lookup"><span data-stu-id="f498f-158">reverse</span></span>         | <span data-ttu-id="f498f-159">Especifica que a direção da execução é retroativa.</span><span class="sxs-lookup"><span data-stu-id="f498f-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="f498f-160">Não é possível especificar um local final com o sinalizador "Reverse".</span><span class="sxs-lookup"><span data-stu-id="f498f-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="f498f-161">Para videodiscs, "Scan" aplica-se somente ao formato CAV.</span><span class="sxs-lookup"><span data-stu-id="f498f-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f498f-162">scanner</span><span class="sxs-lookup"><span data-stu-id="f498f-162">scan</span></span>            | <span data-ttu-id="f498f-163">É reproduzido o mais rápido possível sem desabilitar o vídeo (embora o áudio possa estar desabilitado).</span><span class="sxs-lookup"><span data-stu-id="f498f-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="f498f-164">Para videodiscs, "Scan" aplica-se somente ao formato CAV.</span><span class="sxs-lookup"><span data-stu-id="f498f-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f498f-165">lento</span><span class="sxs-lookup"><span data-stu-id="f498f-165">slow</span></span>            | <span data-ttu-id="f498f-166">É reproduzido lentamente.</span><span class="sxs-lookup"><span data-stu-id="f498f-166">Plays slowly.</span></span> <span data-ttu-id="f498f-167">Para determinar a velocidade exata em um VIDEODISC Player, use o sinalizador "velocidade" do comando de [status](status.md) .</span><span class="sxs-lookup"><span data-stu-id="f498f-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="f498f-168">Para especificar a velocidade mais precisamente, use o sinalizador "velocidade" desse comando.</span><span class="sxs-lookup"><span data-stu-id="f498f-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="f498f-169">Para videodiscs, "lento" aplica-se somente ao formato CAV.</span><span class="sxs-lookup"><span data-stu-id="f498f-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="f498f-170">*número inteiro* de velocidade</span><span class="sxs-lookup"><span data-stu-id="f498f-170">speed *integer*</span></span> | <span data-ttu-id="f498f-171">Reproduz um VIDEODISC na velocidade especificada, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="f498f-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="f498f-172">Esse sinalizador se aplica somente a discos CAV.</span><span class="sxs-lookup"><span data-stu-id="f498f-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f498f-173">para a *posição*</span><span class="sxs-lookup"><span data-stu-id="f498f-173">to *position*</span></span>   | <span data-ttu-id="f498f-174">Especifica uma posição final para a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f498f-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="f498f-175">Se o sinalizador "to" não for especificado, a reprodução será interrompida no final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f498f-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="f498f-176">Para dispositivos **cdaudio** , se a posição "para" for maior que a posição final do disco, o driver retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f498f-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="f498f-177">Para dispositivos **VIDEODISC** , as posições padrão estão em quadros para discos CAV e em horas, minutos e segundos para discos CLV.</span><span class="sxs-lookup"><span data-stu-id="f498f-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="f498f-178">janela</span><span class="sxs-lookup"><span data-stu-id="f498f-178">window</span></span>          | <span data-ttu-id="f498f-179">Especifica que a execução deve usar a janela associada à instância do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f498f-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="f498f-180">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="f498f-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="f498f-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="f498f-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f498f-182">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="f498f-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="f498f-183">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f498f-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="f498f-184">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f498f-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f498f-185">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f498f-185">Return Value</span></span>

<span data-ttu-id="f498f-186">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f498f-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f498f-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="f498f-187">Remarks</span></span>

<span data-ttu-id="f498f-188">Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="f498f-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="f498f-189">Esse comando começa a reproduzir na velocidade atual, conforme definido com o comando Set "Speed".</span><span class="sxs-lookup"><span data-stu-id="f498f-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="f498f-190">A direção será inversa se o sinalizador "Reverse" for especificado ou se o sinalizador "to" for especificado como um valor menor do que o sinalizador "from".</span><span class="sxs-lookup"><span data-stu-id="f498f-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="f498f-191">Se o sinalizador "from" não for especificado, a reprodução começará na posição atual.</span><span class="sxs-lookup"><span data-stu-id="f498f-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="f498f-192">Os sinalizadores "para" e "reverso" não podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="f498f-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="f498f-193">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f498f-193">Examples</span></span>

<span data-ttu-id="f498f-194">O comando a seguir reproduz o dispositivo "mysound" da posição 1000 até a posição 2000, enviando uma mensagem de notificação quando a reprodução é concluída.</span><span class="sxs-lookup"><span data-stu-id="f498f-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="f498f-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f498f-195">Requirements</span></span>



| <span data-ttu-id="f498f-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="f498f-196">Requirement</span></span> | <span data-ttu-id="f498f-197">Valor</span><span class="sxs-lookup"><span data-stu-id="f498f-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f498f-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f498f-198">Minimum supported client</span></span><br/> | <span data-ttu-id="f498f-199">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f498f-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f498f-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f498f-200">Minimum supported server</span></span><br/> | <span data-ttu-id="f498f-201">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f498f-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f498f-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="f498f-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f498f-203">MCI</span><span class="sxs-lookup"><span data-stu-id="f498f-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f498f-204">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="f498f-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="f498f-205">advertência</span><span class="sxs-lookup"><span data-stu-id="f498f-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="f498f-206">set</span><span class="sxs-lookup"><span data-stu-id="f498f-206">set</span></span>](set.md)
</dt> </dl>

 

