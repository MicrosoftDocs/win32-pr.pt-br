---
description: Constantes XAudio2 que especificam parâmetros padrão, valores máximos e sinalizadores.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Sinalizadores e valores de limite de XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811950"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Sinalizadores e valores de limite de XAudio2

Constantes XAudio2 que especificam parâmetros padrão, valores máximos e sinalizadores.

**Valores de limite de XAudio2**



| Constante                                                                                                                                                                                                     | Descrição                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**XAUDIO2 \_ máximo \_ de \_ bytes do buffer**</dt> </dl>             | Valor máximo permitido para [**o \_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer). AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**\_Máximo de \_ buffers enfileirados XAudio2 \_**</dt> </dl>       | Máximo de buffers permitidos em uma fila de voz.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**\_Sistema XAudio2 Max \_ buffers \_**</dt> </dl>       | Máximo de buffers permitidos para threads do sistema (somente no Xbox 360).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ máximo \_ de \_ canais de áudio**</dt> </dl>       | Valor máximo permitido para **WAVEFORMATEX. nChannels**.<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**\_Taxa de \_ amostragem \_ mínima de XAudio2**</dt> </dl>                | Taxa de amostragem de áudio mínima com suporte.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**\_Taxa de \_ amostragem \_ máxima XAudio2**</dt> </dl>                | Taxa máxima de amostras de áudio com suporte.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**\_Nível máximo de \_ volume \_ do XAudio2**</dt> </dl>             | Nível máximo de volume permitido.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**\_Taxa de \_ freq. mínima de XAudio2 \_**</dt> </dl>                   | Taxa de frequência mínima permitida em uma voz de origem.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**\_Taxa máxima de \_ freq \_ XAudio2**</dt> </dl>                   | Taxa de frequência máxima permitida em uma voz de origem.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ \_ taxa de freq padrão \_**</dt> </dl>       | Valor padrão para o argumento **MaxFrequencyRatio** de [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ Max \_ Filter \_ ONEOVERQ**</dt> </dl>    | Valor máximo para [**\_ \_ parâmetros de filtro XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**\_Frequência máxima de \_ filtro \_ do XAudio2**</dt> </dl> | Valor máximo para [**\_ \_ parâmetros de filtro XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters).**Frequência**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**\_Contagem de \_ loop \_ Max de XAudio2**</dt> </dl>                   | Valor máximo que não será tratado como loop infinito para o [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**XAUDIO2 \_ máximo de \_ instâncias**</dt> </dl>                       | Máximo de instâncias simultâneas do XAudio2 permitidas no Xbox 360.<br/>                                                                       |



**Valores de XAudio2 com significado especial**



| Constante                                                                                                                                                                                              | Descrição                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ confirmar \_ agora**</dt> </dl>                         | Usado como um parâmetro para métodos com um argumento Operationset. Consulte [conjuntos de operações XAudio2](xaudio2-operation-sets.md) para obter mais informações.<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ confirmar \_ tudo**</dt> </dl>                         | Usado como um parâmetro em [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges).<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**XAUDIO2 \_ OPSET inválida \_**</dt> </dl>                | Especifica um valor inválido para argumentos Operationset. Consulte [conjuntos de operações XAudio2](xaudio2-operation-sets.md) para obter mais informações.<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ nenhuma \_ região de loop \_**</dt> </dl>            | Especifica nenhuma região de loop, usada [**no \_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**\_Loop XAudio2 \_ infinito**</dt> </dl>                | Especifica o loop infinito, usado no [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**\_Canais padrão \_ XAudio2**</dt> </dl>       | Especifica o número padrão de canais para a plataforma atual, usado em [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**\_Amostra padrão de XAudio2 \_**</dt> </dl> | Especifica a taxa de amostragem padrão para a plataforma atual, usada em [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).<br/>        |



**Sinalizadores de XAudio2**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que a versão de depuração/verificada do mecanismo de áudio deve ser usada em vez da versão de lançamento. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador não tem suporte no Windows 8 ou Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que uma voz de origem não usará a mudança de densidade, consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que nenhuma conversão de taxa de amostragem está disponível em uma voz de origem, as saídas da voz devem ter a mesma taxa de amostragem. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que o efeito de filtro deve estar disponível em uma voz. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2:: CreateSourceVoice</strong></a> e <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2:: CreateSubmixVoice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que uma voz deve continuar emitindo a saída de efeito depois de ser interrompida. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice:: Stop</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">Indica o último buffer em um fluxo. Consulte <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Sinalizadores</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que o mecanismo de áudio deve parar quando nenhuma voz de origem é iniciada e iniciada quando um Voice é iniciado. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">Indica que um filtro deve ser usado em um envio de voz. Consulte <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Sinalizadores</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">Especifica um quantum de processamento não padrão de 21,33 MS (1024 amostras em 48KHz). Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que um cliente de áudio virtual não deve ser usado. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2:: CreateMasteringVoice</strong></a>.<br/>
<blockquote>
[!Note]<br />
Em dispositivos na família de dispositivos móveis, um cliente de áudio virtual sempre é usado, independentemente de esse sinalizador ser usado.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**XAudio2 parâmetros padrão para o filtro de voz interno**



| Constante                                                                                                                                                                                                                 | Descrição                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**\_Tipo de \_ filtro \_ padrão XAudio2**</dt> </dl>                | Especifica o tipo de filtro padrão a ser usado com vozes e envios de voz.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**XAUDIO2 \_ \_ frequência de filtro padrão \_**</dt> </dl> | Especifica a frequência de filtro padrão a ser usada com vozes e envios de voz.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ \_ filtro padrão \_ ONEOVERQ**</dt> </dl>    | Especifica a taxa de filtro padrão de decaimento a ser usada com vozes e envios de voz.<br/> |



## <a name="remarks"></a>Comentários

### <a name="platform-requirements"></a>Requisitos de plataforma

Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK do DirectX (XAudio 2,7)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[XAudio2:: Constants](constants.md)
</dt> </dl>

 

 
