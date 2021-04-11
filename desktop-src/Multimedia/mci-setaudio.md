---
title: MCI_SETAUDIO comando (mmsystem. h)
description: O \_ comando autoaudio do MCI define os valores associados à reprodução e à captura de áudio. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- Multimídia do Windows de comando MCI_SETAUDIO
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163613"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="36838-105">\_Comando de SETaudio do MCI</span><span class="sxs-lookup"><span data-stu-id="36838-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="36838-106">O \_ comando autoaudio do MCI define os valores associados à reprodução e à captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="36838-107">Os dispositivos de vídeo digital e VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="36838-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="36838-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="36838-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="36838-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36838-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36838-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="36838-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="36838-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="36838-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="36838-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="36838-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="36838-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="36838-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="36838-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="36838-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="36838-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span><span class="sxs-lookup"><span data-stu-id="36838-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="36838-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="36838-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="36838-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="36838-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36838-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="36838-118">Return Value</span></span>

<span data-ttu-id="36838-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="36838-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36838-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="36838-120">Remarks</span></span>

<span data-ttu-id="36838-121">Os seguintes sinalizadores se aplicam ao tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="36838-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="36838-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>ALG DGV do MCI de \_ \_ áudio \_</span><span class="sxs-lookup"><span data-stu-id="36838-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="36838-123">O membro **lpstrAlgorithm** da estrutura identificada por *lpSetAudio* contém um endereço de um buffer que contém o nome de um algoritmo de compactação de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="36838-124">O algoritmo de compactação é usado por comandos de [ \_ gravação MCI](mci-record.md) ou de [ \_ reserva de MCI](mci-reserve.md) subsequentes.</span><span class="sxs-lookup"><span data-stu-id="36838-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="36838-125">Os algoritmos disponíveis são dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36838-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="36838-126">Se o algoritmo for incompatível com o formato de arquivo atual, o formato de arquivo será alterado para o formato padrão do algoritmo.</span><span class="sxs-lookup"><span data-stu-id="36838-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="36838-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>\_DGV de \_ horário de áudio \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="36838-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="36838-128">O tempo especificado é em milissegundos e é o tempo absoluto quando usado com o MCI \_ DGV \_ \_ por áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="36838-129">(Esse tempo não está em etapa com a reprodução do espaço de trabalho.)</span><span class="sxs-lookup"><span data-stu-id="36838-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="36838-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_entrada de \_ SetAudio do MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="36838-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="36838-131">Modifica o sinalizador Bass, agudos ou volume para que ele afete o sinal de entrada e modifique o que é registrado.</span><span class="sxs-lookup"><span data-stu-id="36838-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="36838-132">Se possível, esse é o padrão ao monitorar a entrada.</span><span class="sxs-lookup"><span data-stu-id="36838-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="36838-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_item de \_ áudio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="36838-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="36838-134">Uma constante de áudio é especificada no membro **dwItem** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-135">A constante identifica o valor que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="36838-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="36838-136">As seguintes constantes são definidas:</span><span class="sxs-lookup"><span data-stu-id="36838-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="36838-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>\_AVGBYTESPERSEC DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="36838-138">O número médio de bytes é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-139">Esse valor define o número médio de bytes por segundo para reprodução ou gravação nos formatos PCM (modulação de código de pulso) e ADPCM (modulação diferencial de código de pulso).</span><span class="sxs-lookup"><span data-stu-id="36838-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="36838-140">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="36838-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="36838-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SetAudio \_ Bass</span><span class="sxs-lookup"><span data-stu-id="36838-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="36838-142">O nível de baixa frequência de áudio é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="36838-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>\_BITSPERSAMPLE DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="36838-144">O número de bits por amostra é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-145">Esse valor define o número de bits por amostra reproduzido ou registrado no formato PCM.</span><span class="sxs-lookup"><span data-stu-id="36838-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="36838-146">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="36838-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="36838-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>\_BLOCKALIGN DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="36838-148">O alinhamento do bloco de dados é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-149">Esse valor define o alinhamento dos blocos de dados em relação ao início dos dados de onda de entrada.</span><span class="sxs-lookup"><span data-stu-id="36838-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="36838-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>\_SAMPLESPERSEC DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="36838-151">A taxa de amostra é especificada no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-152">Esse valor define a taxa de amostragem para reproduzir e gravar com os algoritmos PCM e ADPCM.</span><span class="sxs-lookup"><span data-stu-id="36838-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="36838-153">O arquivo é salvo neste formato.</span><span class="sxs-lookup"><span data-stu-id="36838-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="36838-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_fonte de \_ áudio DGV do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="36838-155">Uma constante que especifica a fonte de entrada de áudio é incluída no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-156">As constantes a seguir são definidas para as fontes de entrada de áudio:</span><span class="sxs-lookup"><span data-stu-id="36838-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="36838-157">\_média de \_ origem do \_ DGV do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="36838-158">A média dos canais de áudio esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="36838-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="36838-159">\_fonte de áudio DGV do MCI com a \_ \_ \_ esquerda</span><span class="sxs-lookup"><span data-stu-id="36838-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="36838-160">Canal de áudio à esquerda.</span><span class="sxs-lookup"><span data-stu-id="36838-160">Left audio channel.</span></span>

<span data-ttu-id="36838-161">\_ \_ \_ origem \_ do DGV do MCI com fonte de áudio</span><span class="sxs-lookup"><span data-stu-id="36838-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="36838-162">Canal de áudio correto.</span><span class="sxs-lookup"><span data-stu-id="36838-162">Right audio channel.</span></span>

<span data-ttu-id="36838-163">\_estéreo de \_ fonte de áudio MCI DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="36838-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="36838-164">Aparelhos.</span><span class="sxs-lookup"><span data-stu-id="36838-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="36838-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_fluxo de \_ áudio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="36838-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="36838-166">Um fluxo de áudio é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-167">O valor inteiro especifica o fluxo de áudio reproduzido do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36838-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="36838-168">Se o fluxo não for especificado, o primeiro fluxo de áudio fisicamente intercalado será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="36838-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="36838-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ de som \_</span><span class="sxs-lookup"><span data-stu-id="36838-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="36838-170">O nível de alta frequência de áudio é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="36838-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_volume de \_ áudio MCI \_ DGV</span><span class="sxs-lookup"><span data-stu-id="36838-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="36838-172">O nível de áudio para um ou ambos os canais de áudio é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-173">Se os volumes esquerdo e direito tiverem sido definidos com valores diferentes, a taxa do volume da esquerda para a direita será quase inalterada.</span><span class="sxs-lookup"><span data-stu-id="36838-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="36838-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ setáudio \_ esquerdo</span><span class="sxs-lookup"><span data-stu-id="36838-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="36838-175">Habilita o canal de áudio à esquerda quando usado com o MCI \_ definido \_ como ativado.</span><span class="sxs-lookup"><span data-stu-id="36838-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="36838-176">Desabilita o canal de áudio à esquerda quando usado com o MCI \_ definido como \_ desativado.</span><span class="sxs-lookup"><span data-stu-id="36838-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="36838-177">Quando esse sinalizador é usado com a combinação do valor de DGV do MCI \_ \_ e do \_ \_ \_ volume de áudio MCI DGV \_ , ele define o volume do canal de áudio à esquerda.</span><span class="sxs-lookup"><span data-stu-id="36838-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="36838-178">Quando esse sinalizador é usado com a \_ \_ fonte de áudio MCI DGV \_ , ele especifica o canal de áudio à esquerda como a origem do digitalizador de entrada de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="36838-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ por áudio \_</span><span class="sxs-lookup"><span data-stu-id="36838-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="36838-180">Um parâmetro de comprimento de transição está incluído no membro **dwOver** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-181">O valor de comprimento especifica quanto tempo (em unidades do formato de hora atual) deve ser necessário para fazer uma alteração que usa um fator.</span><span class="sxs-lookup"><span data-stu-id="36838-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="36838-182">Se esse sinalizador não for usado, as alterações ocorrerão imediatamente.</span><span class="sxs-lookup"><span data-stu-id="36838-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="36838-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_qualidade de \_ áudio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="36838-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="36838-184">O membro **lpstrQuality** da estrutura identificada por *lpSetAudio* contém um endereço de um buffer que define a qualidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="36838-185">Uma cadeia de caracteres de texto dentro do buffer especifica as características do algoritmo de compactação de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="36838-186">O \_ sinalizador de \_ alg DGV de autoáudio do MCI \_ pode ser usado para selecionar um descritor de qualidade para o algoritmo especificado.</span><span class="sxs-lookup"><span data-stu-id="36838-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="36838-187">Se esse sinalizador for omitido, o algoritmo atual será usado.</span><span class="sxs-lookup"><span data-stu-id="36838-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="36838-188">Os algoritmos e os nomes de descritores disponíveis dependem do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36838-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="36838-189">Cada dispositivo fornece documentação para os algoritmos disponíveis e uma descrição dos nomes de descritores aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="36838-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="36838-190">O comando de [ \_ qualidade do MCI](mci-quality.md) pode definir nomes de descritores adicionais.</span><span class="sxs-lookup"><span data-stu-id="36838-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="36838-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_registro de \_ áudio DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="36838-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="36838-192">Especifica se a gravação inclui ou exclui dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="36838-193">Quando combinado com o MCI \_ definido \_ ativado, os dados de áudio são registrados.</span><span class="sxs-lookup"><span data-stu-id="36838-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="36838-194">Quando combinado com o MCI \_ definido \_ , os dados de áudio são excluídos.</span><span class="sxs-lookup"><span data-stu-id="36838-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="36838-195">O padrão inclui dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="36838-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV de \_ som \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="36838-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="36838-197">Habilita o canal de áudio correto quando usado com o MCI \_ definido \_ como ativado.</span><span class="sxs-lookup"><span data-stu-id="36838-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="36838-198">Desabilita o canal de áudio correto quando usado com o MCI \_ definido como \_ desativado.</span><span class="sxs-lookup"><span data-stu-id="36838-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="36838-199">Quando esse sinalizador é usado com a combinação do valor de DGV do MCI \_ \_ e do \_ \_ \_ volume de áudio MCI DGV \_ , ele define o volume do canal de áudio correto.</span><span class="sxs-lookup"><span data-stu-id="36838-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="36838-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_valor DGV \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="36838-201">Um valor é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*.</span><span class="sxs-lookup"><span data-stu-id="36838-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="36838-202">O significado do valor é especificado pela constante definida para o \_ sinalizador de item de áudio DGV do MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="36838-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="36838-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="36838-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="36838-204">Desabilita o canal de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="36838-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="36838-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="36838-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="36838-206">Habilita o canal de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="36838-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="36838-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>\_saída de SETaudio do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="36838-208">Modifica o sinalizador Bass, agudos ou volume para que ele modifique apenas o sinal de reprodução e não o que é registrado.</span><span class="sxs-lookup"><span data-stu-id="36838-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="36838-209">Se possível, esse é o padrão ao monitorar a entrada.</span><span class="sxs-lookup"><span data-stu-id="36838-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="36838-210">Para dispositivos de vídeo digital, o parâmetro *lpSetAudio* aponta para uma estrutura de parâmetros de [**áudio do \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="36838-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="36838-211">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="36838-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="36838-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_registro de \_ áudio de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="36838-213">Define a gravação de áudio como on ou off, que é usada em conjunto com um dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="36838-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="36838-214">MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="36838-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="36838-215">Gravação de áudio ativada.</span><span class="sxs-lookup"><span data-stu-id="36838-215">Audio recording on.</span></span>

<span data-ttu-id="36838-216">conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="36838-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="36838-217">Gravação de áudio desativada.</span><span class="sxs-lookup"><span data-stu-id="36838-217">Audio recording off.</span></span> <span data-ttu-id="36838-218">Pode ser necessário primeiro desativar a gravação de montagem (usando o comando [MCI \_ set](mci-set.md) com o \_ conjunto de VCR MCI \_ definir \_ \_ sinalizador de registro de montagem definido como desativado) antes que a gravação de áudio possa ser desativada.</span><span class="sxs-lookup"><span data-stu-id="36838-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="36838-219">\_faixa MCI</span><span class="sxs-lookup"><span data-stu-id="36838-219">MCI\_TRACK</span></span>

<span data-ttu-id="36838-220">O membro **dwTrack** da estrutura identificada por *lpSetAudio* especifica qual faixa é afetada pelo comando.</span><span class="sxs-lookup"><span data-stu-id="36838-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="36838-221">\_fonte de \_ áudio do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="36838-222">Define a fonte de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-222">Sets the audio source.</span></span> <span data-ttu-id="36838-223">Esse sinalizador deve ser usado com o sinalizador de áudio MCI do \_ VCR \_ \_ para sinalizar.</span><span class="sxs-lookup"><span data-stu-id="36838-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="36838-224">\_Monitor de \_ áudio de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="36838-225">Define o monitor de fonte de áudio.</span><span class="sxs-lookup"><span data-stu-id="36838-225">Sets the audio source monitor.</span></span> <span data-ttu-id="36838-226">Esse sinalizador deve ser usado com o sinalizador de áudio MCI do \_ VCR \_ \_ para sinalizar.</span><span class="sxs-lookup"><span data-stu-id="36838-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="36838-227">\_vídeo de VCR do MCI \_ \_ para</span><span class="sxs-lookup"><span data-stu-id="36838-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="36838-228">O membro **dwTo** da estrutura identificada por *lpSetAudio* contém uma constante que descreve o tipo de entrada ou entrada monitorada.</span><span class="sxs-lookup"><span data-stu-id="36838-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="36838-229">Ele deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="36838-229">It must be one of the following:</span></span>

<span data-ttu-id="36838-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="36838-230"><dl> <dd></span></span>

<span data-ttu-id="36838-231">\_ \_ \_ sintonizador de tipo de src VCR do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="36838-232">O tipo é sintonizador.</span><span class="sxs-lookup"><span data-stu-id="36838-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="36838-233">\_linha de \_ tipo de src VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="36838-234">O tipo é linha.</span><span class="sxs-lookup"><span data-stu-id="36838-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="36838-235">\_tipo de \_ src do VCR \_ do MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="36838-236">O tipo é auxiliar.</span><span class="sxs-lookup"><span data-stu-id="36838-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="36838-237">\_tipo de src VCR do MCI \_ \_ \_ genérico</span><span class="sxs-lookup"><span data-stu-id="36838-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="36838-238">O tipo é genérico.</span><span class="sxs-lookup"><span data-stu-id="36838-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="36838-239">\_tipo de src de vídeo MCI \_ \_ \_ sem áudio</span><span class="sxs-lookup"><span data-stu-id="36838-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="36838-240">O tipo está mudo.</span><span class="sxs-lookup"><span data-stu-id="36838-240">Type is mute.</span></span> <span data-ttu-id="36838-241">Isso pode ser usado somente com o \_ sinalizador de fonte de vídeo do VCR MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="36838-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="36838-242">\_saída do \_ tipo de src VCR \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="36838-243">O tipo é saída.</span><span class="sxs-lookup"><span data-stu-id="36838-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="36838-244">\_número de \_ áudio do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="36838-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="36838-245">O membro dwNumber da estrutura identificada por lpSetAudio contém a entrada de áudio (do tipo especificado no membro dwTo) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="36838-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="36838-246">Para dispositivos VCR, o parâmetro *lpSetAudio* aponta para uma estrutura de parâmetros de [**áudio do \_ VCR \_ \_ MCI**](mci-vcr-setaudio-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="36838-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="36838-247">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36838-247">Requirements</span></span>



| <span data-ttu-id="36838-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="36838-248">Requirement</span></span> | <span data-ttu-id="36838-249">Valor</span><span class="sxs-lookup"><span data-stu-id="36838-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36838-250">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36838-250">Minimum supported client</span></span><br/> | <span data-ttu-id="36838-251">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36838-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36838-252">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36838-252">Minimum supported server</span></span><br/> | <span data-ttu-id="36838-253">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36838-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36838-254">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="36838-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="36838-255"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36838-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36838-256">Confira também</span><span class="sxs-lookup"><span data-stu-id="36838-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36838-257">MCI</span><span class="sxs-lookup"><span data-stu-id="36838-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="36838-258">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="36838-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

