---
description: Constantes XAudio2 que especificam parâmetros padrão, valores máximos e sinalizadores.
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: Valores e sinalizadores de limite XAudio2 (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11293b55a44b0aefdeacf95b9e36e90a626de2c1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470702"
---
# <a name="xaudio2-boundary-values-and-flags"></a>Valores e sinalizadores de limite XAudio2

Constantes XAudio2 que especificam parâmetros padrão, valores máximos e sinalizadores.

**Valores de limite XAudio2**



| Constante                                                                                                                                                                                                     | Descrição                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**XAUDIO2 \_ MAX \_ BUFFER \_ BYTES**</dt> </dl>             | Valor máximo permitido para [**BUFFER XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**BUFFERS XAUDIO2 \_ MAX \_ NA FILA \_**</dt> </dl>       | Máximo de buffers permitidos em uma fila de voz.<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**SISTEMA DE \_ \_ BUFFERS MÁXIMOS XAUDIO2 \_**</dt> </dl>       | Buffers máximos permitidos para threads do sistema (Xbox 360 somente).<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ MAX \_ AUDIO \_ CHANNELS**</dt> </dl>       | Valor máximo permitido para **WAVEFORMATEX.nChannels.**<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**TAXA DE AMOSTRA DE XAUDIO2 \_ MIN \_ \_**</dt> </dl>                | Taxa mínima de amostra de áudio com suporte.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**TAXA DE AMOSTRA MÁXIMA DE XAUDIO2 \_ \_ \_**</dt> </dl>                | Taxa máxima de amostra de áudio com suporte.<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**NÍVEL DE \_ VOLUME MÁXIMO XAUDIO2 \_ \_**</dt> </dl>             | Nível máximo de volume permitido.<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**TAXA DE \_ \_ FREQ DE \_ XAUDIO2 MIN**</dt> </dl>                   | Taxa de frequência mínima permitida em uma voz de origem.<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**TAXA DE \_ FREQ MÁX. \_ XAUDIO2 \_**</dt> </dl>                   | Taxa de frequência máxima permitida em uma voz de origem.<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**TAXA DE \_ FREQ PADRÃO XAUDIO2 \_ \_**</dt> </dl>       | Valor padrão para o **argumento MaxFrequencyRatio** de [**IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FILTER \_ ONEOVERQ**</dt> </dl>    | Valor máximo para [**\_ \_ PARÂMETROS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)DE FILTRO XAUDIO2 .**OneOverQ**.<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**FREQUÊNCIA MÁXIMA DO FILTRO XAUDIO2 \_ \_ \_**</dt> </dl> | Valor máximo para [**\_ \_ PARÂMETROS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)DE FILTRO XAUDIO2 .**Frequência**.<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**CONTAGEM MÁXIMA DE \_ \_ LOOPS XAUDIO2 \_**</dt> </dl>                   | Valor máximo que não será tratado como loop infinito para [**\_ BUFFER XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**INSTÂNCIAS XAUDIO2 \_ \_ MAX**</dt> </dl>                       | Máximo de instâncias simultâneas do XAudio2 permitidas Xbox 360.<br/>                                                                       |



**Valores XAudio2 com significado especial**



| Constante                                                                                                                                                                                              | Descrição                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**XAUDIO2 \_ COMMIT \_ NOW**</dt> </dl>                         | Usado como um parâmetro para métodos com um argumento OperationSet. Confira [Conjuntos de Operações XAudio2](xaudio2-operation-sets.md) para obter mais informações.<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ COMMIT \_ ALL**</dt> </dl>                         | Usado como um parâmetro em [**IXAudio2::CommitChanges.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**OPSET XAUDIO2 \_ \_ INVÁLIDO**</dt> </dl>                | Especifica um valor inválido para argumentos OperationSet. Confira [Conjuntos de Operações XAudio2](xaudio2-operation-sets.md) para obter mais informações.<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ NO \_ LOOP \_ REGION**</dt> </dl>            | Não especifica nenhuma região de loop, usada no [**\_ BUFFER XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**XAUDIO2 \_ LOOP \_ INFINITE**</dt> </dl>                | Especifica o loop infinito, usado no [**\_ BUFFER XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)**LoopCount**.<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**CANAIS PADRÃO \_ XAUDIO2 \_**</dt> </dl>       | Especifica o número padrão de canais para a plataforma atual, usado em [**IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**TAXA DE AMOSTRA PADRÃO XAUDIO2 \_ \_**</dt> </dl> | Especifica a taxa de exemplo padrão para a plataforma atual, usada em [**IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)<br/>        |



**Sinalizadores XAudio2**




| Constante | Descrição | 
|----------|-------------|
| <span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl><dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt></dl> | Especifica que a versão de depuração/verificada do mecanismo de áudio deve ser usada em vez da versão de lançamento. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Criar</strong></a>.<br /><blockquote>[!Note]<br />Não há suporte para esse sinalizador Windows 8 ou Windows 10.</blockquote><br /> | 
| <span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl><dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt></dl> | Especifica que uma voz de origem não usará a mudança de tom, consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl><dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt></dl> | Especifica que nenhuma conversão de taxa de exemplo está disponível em uma voz de origem, as saídas da voz devem ter a mesma taxa de exemplo. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl><dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt></dl> | Especifica que o efeito de filtro deve estar disponível em uma voz. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2::CreateSourceVoice</strong></a> <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>e IXAudio2::CreateSubmixVoice</strong></a>.<br /> | 
| <span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl><dt><strong>XAUDIO2_PLAY_TAILS</strong></dt></dl> | Especifica que uma voz deve continuar emitindo a saída de efeito depois que ela for interrompida. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice::Stop</strong></a>.<br /> | 
| <span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl><dt><strong>XAUDIO2_END_OF_STREAM</strong></dt></dl> | Indica o último buffer em um fluxo. Consulte <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>. <strong>Sinalizadores</strong>.<br /> | 
| <span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl><dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt></dl> | Especifica que o mecanismo de áudio deve parar quando nenhuma voz de origem for iniciada e iniciar quando uma voz for iniciada. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Criar</strong></a>.<br /> | 
| <span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl><dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt></dl> | Indica que um filtro deve ser usado em um envio de voz. Consulte <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>. <strong>Sinalizadores</strong>.<br /> | 
| <span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl><dt><strong>XAUDIO2_1024_QUANTUM</strong></dt></dl> | Especifica um quantum de processamento não padrão de 21,33 ms (1024 amostras a 48KHz). Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Criar</strong></a>.<br /> | 
| <span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl><dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt></dl> | Especifica que um cliente de áudio virtual não deve ser usado. Consulte <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2::CreateMasteringVoice</strong></a>.<br /><blockquote>[!Note]<br />Em dispositivos na família de dispositivos móveis, um cliente de áudio virtual é sempre usado, independentemente de esse sinalizador ser usado.</blockquote><br /> | 




**Parâmetros padrão XAudio2 para o filtro de voz integrado**



| Constante                                                                                                                                                                                                                 | Descrição                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**TIPO DE FILTRO PADRÃO XAUDIO2 \_ \_ \_**</dt> </dl>                | Especifica o tipo de filtro padrão a ser usado com vozes e mensagens de voz.<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**FREQUÊNCIA DE FILTRO PADRÃO XAUDIO2 \_ \_ \_**</dt> </dl> | Especifica a frequência de filtro padrão a ser usada com vozes e mensagens de voz.<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ DEFAULT \_ FILTER \_ ONEOVERQ**</dt> </dl>    | Especifica a taxa de filtro padrão de decaimento a ser usada com vozes e mensagens de voz.<br/> |



## <a name="remarks"></a>Comentários

### <a name="platform-requirements"></a>Requisitos de plataforma

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); SDK do DirectX (XAudio 2.7)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[XAudio2:: Constants](constants.md)
</dt> </dl>

 

 
