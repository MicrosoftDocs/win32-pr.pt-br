---
title: comando info
description: O comando info recupera uma descrição de hardware de um dispositivo. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- Multimídia do Windows de comando de informações
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369857"
---
# <a name="info-command"></a><span data-ttu-id="899b5-105">comando info</span><span class="sxs-lookup"><span data-stu-id="899b5-105">info command</span></span>

<span data-ttu-id="899b5-106">O comando info recupera uma descrição de hardware de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="899b5-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="899b5-107">Todos os dispositivos MCI reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="899b5-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="899b5-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="899b5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="899b5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="899b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899b5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="899b5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="899b5-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="899b5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="899b5-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="899b5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="899b5-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span><span class="sxs-lookup"><span data-stu-id="899b5-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="899b5-114">Sinalizador que identifica o tipo de informação necessário.</span><span class="sxs-lookup"><span data-stu-id="899b5-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="899b5-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **info** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="899b5-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="899b5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="899b5-116">Value</span></span>        | <span data-ttu-id="899b5-117">Significado</span><span class="sxs-lookup"><span data-stu-id="899b5-117">Meaning</span></span>                                                             | <span data-ttu-id="899b5-118">Significado</span><span class="sxs-lookup"><span data-stu-id="899b5-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="899b5-119">cdaudio</span><span class="sxs-lookup"><span data-stu-id="899b5-119">cdaudio</span></span>      | <span data-ttu-id="899b5-120">informações identityinfo UPC</span><span class="sxs-lookup"><span data-stu-id="899b5-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="899b5-121">product</span><span class="sxs-lookup"><span data-stu-id="899b5-121">product</span></span>                                             |
| <span data-ttu-id="899b5-122">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="899b5-122">digitalvideo</span></span> | <span data-ttu-id="899b5-123">áudio algorithmaudio qualityfileproductstill algorithmstill Quality</span><span class="sxs-lookup"><span data-stu-id="899b5-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="899b5-124">usageversionvideo algorithmvideo qualitywindow Text</span><span class="sxs-lookup"><span data-stu-id="899b5-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="899b5-125">overlay</span><span class="sxs-lookup"><span data-stu-id="899b5-125">overlay</span></span>      | <span data-ttu-id="899b5-126">produto</span><span class="sxs-lookup"><span data-stu-id="899b5-126">fileproduct</span></span>                                                         | <span data-ttu-id="899b5-127">texto da janela</span><span class="sxs-lookup"><span data-stu-id="899b5-127">window text</span></span>                                         |
| <span data-ttu-id="899b5-128">sequenciador</span><span class="sxs-lookup"><span data-stu-id="899b5-128">sequencer</span></span>    | <span data-ttu-id="899b5-129">copyrightfile</span><span class="sxs-lookup"><span data-stu-id="899b5-129">copyrightfile</span></span>                                                       | <span data-ttu-id="899b5-130">nameproduct</span><span class="sxs-lookup"><span data-stu-id="899b5-130">nameproduct</span></span>                                         |
| <span data-ttu-id="899b5-131">videocassete</span><span class="sxs-lookup"><span data-stu-id="899b5-131">vcr</span></span>          | <span data-ttu-id="899b5-132">product</span><span class="sxs-lookup"><span data-stu-id="899b5-132">product</span></span>                                                             | <span data-ttu-id="899b5-133">version</span><span class="sxs-lookup"><span data-stu-id="899b5-133">version</span></span>                                             |
| <span data-ttu-id="899b5-134">videodisk</span><span class="sxs-lookup"><span data-stu-id="899b5-134">videodisk</span></span>    | <span data-ttu-id="899b5-135">product</span><span class="sxs-lookup"><span data-stu-id="899b5-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="899b5-136">waveaudio</span><span class="sxs-lookup"><span data-stu-id="899b5-136">waveaudio</span></span>    | <span data-ttu-id="899b5-137">entrada de dados</span><span class="sxs-lookup"><span data-stu-id="899b5-137">fileinput</span></span>                                                           | <span data-ttu-id="899b5-138">outputproduct</span><span class="sxs-lookup"><span data-stu-id="899b5-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="899b5-139">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszInfoType** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="899b5-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="899b5-140">Valor</span><span class="sxs-lookup"><span data-stu-id="899b5-140">Value</span></span>           | <span data-ttu-id="899b5-141">Significado</span><span class="sxs-lookup"><span data-stu-id="899b5-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="899b5-142">algoritmo de áudio</span><span class="sxs-lookup"><span data-stu-id="899b5-142">audio algorithm</span></span> | <span data-ttu-id="899b5-143">Retorna o nome do algoritmo de compactação de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="899b5-144">qualidade de áudio</span><span class="sxs-lookup"><span data-stu-id="899b5-144">audio quality</span></span>   | <span data-ttu-id="899b5-145">Retorna o nome do descritor de qualidade de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="899b5-146">Isso pode retornar "desconhecido" se o aplicativo tiver definido parâmetros para valores específicos que não correspondam a qualidades definidas.</span><span class="sxs-lookup"><span data-stu-id="899b5-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="899b5-147">direitos autorais</span><span class="sxs-lookup"><span data-stu-id="899b5-147">copyright</span></span>       | <span data-ttu-id="899b5-148">Recupera o aviso de direitos autorais do arquivo MIDI do evento meta de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="899b5-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="899b5-149">arquivo</span><span class="sxs-lookup"><span data-stu-id="899b5-149">file</span></span>            | <span data-ttu-id="899b5-150">Recupera o nome do arquivo usado pelo dispositivo composto.</span><span class="sxs-lookup"><span data-stu-id="899b5-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="899b5-151">Se o dispositivo for aberto sem um arquivo e o comando de [carregamento](load.md) não tiver sido usado, uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="899b5-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="899b5-152">identidade de informações</span><span class="sxs-lookup"><span data-stu-id="899b5-152">info identity</span></span>   | <span data-ttu-id="899b5-153">Produz um identificador exclusivo para o CD de áudio atualmente carregado no Player que está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="899b5-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="899b5-154">UPC de informações</span><span class="sxs-lookup"><span data-stu-id="899b5-154">info upc</span></span>        | <span data-ttu-id="899b5-155">Produz o código do produto universal (UPC) que é codificado em um CD de áudio.</span><span class="sxs-lookup"><span data-stu-id="899b5-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="899b5-156">O UPC é uma cadeia de caracteres de dígitos.</span><span class="sxs-lookup"><span data-stu-id="899b5-156">The UPC is a string of digits.</span></span> <span data-ttu-id="899b5-157">Ele pode não estar disponível para todos os CDs.</span><span class="sxs-lookup"><span data-stu-id="899b5-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="899b5-158">input</span><span class="sxs-lookup"><span data-stu-id="899b5-158">input</span></span>           | <span data-ttu-id="899b5-159">Recupera a descrição do dispositivo de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="899b5-160">Retorna "None" se um dispositivo de entrada não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="899b5-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="899b5-161">name</span><span class="sxs-lookup"><span data-stu-id="899b5-161">name</span></span>            | <span data-ttu-id="899b5-162">Recupera o nome da sequência do evento meta de nome de sequência/faixa.</span><span class="sxs-lookup"><span data-stu-id="899b5-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="899b5-163">output</span><span class="sxs-lookup"><span data-stu-id="899b5-163">output</span></span>          | <span data-ttu-id="899b5-164">Recupera a descrição do dispositivo de saída atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="899b5-165">Retorna "None" se um dispositivo de saída não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="899b5-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="899b5-166">product</span><span class="sxs-lookup"><span data-stu-id="899b5-166">product</span></span>         | <span data-ttu-id="899b5-167">Recupera uma descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="899b5-167">Retrieves a description of the device.</span></span> <span data-ttu-id="899b5-168">Essas informações geralmente incluem o nome do produto e o modelo.</span><span class="sxs-lookup"><span data-stu-id="899b5-168">This information often includes the product name and model.</span></span> <span data-ttu-id="899b5-169">O comprimento da cadeia de caracteres será de 31 caracteres ou menos.</span><span class="sxs-lookup"><span data-stu-id="899b5-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="899b5-170">algoritmo ainda</span><span class="sxs-lookup"><span data-stu-id="899b5-170">still algorithm</span></span> | <span data-ttu-id="899b5-171">Retorna o nome do algoritmo de compactação de imagem ainda atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="899b5-172">qualidade ainda</span><span class="sxs-lookup"><span data-stu-id="899b5-172">still quality</span></span>   | <span data-ttu-id="899b5-173">Retorna o nome do descritor de qualidade da imagem atual ainda.</span><span class="sxs-lookup"><span data-stu-id="899b5-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="899b5-174">Isso pode retornar "desconhecido" se o aplicativo tiver definido parâmetros para valores específicos que não correspondam a qualidades definidas.</span><span class="sxs-lookup"><span data-stu-id="899b5-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="899b5-175">uso</span><span class="sxs-lookup"><span data-stu-id="899b5-175">usage</span></span>           | <span data-ttu-id="899b5-176">Retorna uma cadeia de caracteres que descreve as restrições de uso que podem ser impostas pelo proprietário dos dados visuais ou de áudio no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="899b5-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="899b5-177">version</span><span class="sxs-lookup"><span data-stu-id="899b5-177">version</span></span>         | <span data-ttu-id="899b5-178">Retorna o nível de versão do driver de dispositivo e do hardware.</span><span class="sxs-lookup"><span data-stu-id="899b5-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="899b5-179">algoritmo de vídeo</span><span class="sxs-lookup"><span data-stu-id="899b5-179">video algorithm</span></span> | <span data-ttu-id="899b5-180">Retorna o nome do algoritmo de compactação de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="899b5-181">qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="899b5-181">video quality</span></span>   | <span data-ttu-id="899b5-182">Retorna o nome do descritor de qualidade de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="899b5-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="899b5-183">Isso pode retornar "desconhecido" se o aplicativo tiver definido parâmetros para valores específicos que não correspondam a qualidades definidas.</span><span class="sxs-lookup"><span data-stu-id="899b5-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="899b5-184">texto da janela</span><span class="sxs-lookup"><span data-stu-id="899b5-184">window text</span></span>     | <span data-ttu-id="899b5-185">Recupera a legenda da janela usada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="899b5-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="899b5-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="899b5-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="899b5-187">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="899b5-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="899b5-188">Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="899b5-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="899b5-189">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="899b5-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899b5-190">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="899b5-190">Return Value</span></span>

<span data-ttu-id="899b5-191">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="899b5-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="899b5-192">Exemplos</span><span class="sxs-lookup"><span data-stu-id="899b5-192">Examples</span></span>

<span data-ttu-id="899b5-193">O comando a seguir recupera uma descrição do hardware associado ao dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="899b5-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="899b5-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="899b5-194">Requirements</span></span>



| <span data-ttu-id="899b5-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="899b5-195">Requirement</span></span> | <span data-ttu-id="899b5-196">Valor</span><span class="sxs-lookup"><span data-stu-id="899b5-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="899b5-197">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="899b5-197">Minimum supported client</span></span><br/> | <span data-ttu-id="899b5-198">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="899b5-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="899b5-199">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="899b5-199">Minimum supported server</span></span><br/> | <span data-ttu-id="899b5-200">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="899b5-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="899b5-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="899b5-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="899b5-202">MCI</span><span class="sxs-lookup"><span data-stu-id="899b5-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="899b5-203">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="899b5-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="899b5-204">carga</span><span class="sxs-lookup"><span data-stu-id="899b5-204">load</span></span>](load.md)
</dt> </dl>

 

