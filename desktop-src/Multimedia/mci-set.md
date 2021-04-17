---
title: MCI_SET comando (mmsystem. h)
description: O \_ comando set do MCI define as informações do dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- Multimídia do Windows de comando MCI_SET
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "105766374"
---
# <a name="mci_set-command"></a>Comando de definição do MCI \_

> [!NOTE]
> Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.  Neste documento, há referências à palavra ' escravo '. O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos. Para fins de consistência, este documento contém esta palavra. Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.

O \_ comando set do MCI define as informações do dispositivo. CD de áudio, Digital-Video, MIDI Sequencer, VCR, VIDEODISC, vídeo-Overlay e Wave-Audio Devices reconhecem esse comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros do MCI Set**](mci-set-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte ao conjunto de MCI \_ :

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>\_áudio definido por MCI \_
</dt> <dd>

Um número de canal de áudio é incluído no membro dwAudio da estrutura identificada por *lpSet*. Esse sinalizador deve ser usado com o MCI \_ definido \_ como ativado ou MCI \_ definido como \_ off. Use uma das seguintes constantes para indicar o número do canal:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>o MCI \_ definir \_ áudio \_ tudo
</dt> <dd>

Todos os canais de áudio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ definir \_ áudio \_ restante
</dt> <dd>

Canal esquerdo.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ definir \_ áudio \_ à direita
</dt> <dd>

Canal direito.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>porta do conjunto do MCI \_ \_ \_ fechada
</dt> <dd>

Fecha a cobertura de mídia (se houver).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>porta do conjunto do MCI \_ \_ \_ aberta
</dt> <dd>

Abre a tampa de mídia (se houver).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado
</dt> <dd>

Desabilita o vídeo ou o canal de áudio especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em
</dt> <dd>

Habilita o vídeo ou o canal de áudio especificado.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>\_formato de \_ hora \_ definido do MCI
</dt> <dd>

Um parâmetro de formato de hora é incluído no membro **dwTimeFormat** da estrutura identificada por *lpSet*. Os sinalizadores a seguir são usados com este sinalizador:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_bytes de formato MCI \_
</dt> <dd>

Em um formato de dados PCM (modulação de código de pulso), o altera a descrição do membro de tempo para bytes para entrada ou saída. Reconhecido pelo tipo de dispositivo **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_quadros de formato MCI \_
</dt> <dd>

Os comandos subsequentes usarão quadros. Reconhecido pelos tipos de dispositivo **DigitalVideo**, **VCR** e **VIDEODISC** .

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_formato MCI \_ HMS
</dt> <dd>

Altera o formato de hora para horas, minutos e segundos. Reconhecido pelos tipos de dispositivo **VCR** e **VIDEODISC** .

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>\_milissegundos do formato MCI \_
</dt> <dd>

Altera o formato de hora para milissegundos. Reconhecido por todos os tipos de dispositivo.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_formato MCI \_ MSF
</dt> <dd>

Altera o formato de hora para minutos, segundos e quadros. Reconhecido pelos tipos de dispositivo **cdaudio** e **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_exemplos de formato MCI \_
</dt> <dd>

Altera o formato de hora para exemplos de entrada ou saída. Reconhecido pelo tipo de dispositivo **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Formato MCI \_ SMPTE \_ 24, \_ formato MCI \_ SMPTE \_ 25 e formato MCI \_ \_ SMPTE \_ 30
</dt> <dd>

Define o formato de hora como 24, 25 e 30 quadros SMPTE (sociedade de imagem de movimento e engenheiros de televisão), respectivamente. Reconhecido pelos tipos de dispositivo **Sequencer** e **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Formato MCI \_ SMPTE \_ 30DROP
</dt> <dd>

Define o formato de hora para 30 quadros de distribuição SMPTE. Reconhecido pelos tipos de dispositivo **Sequencer** e **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_formato MCI \_ TMSF
</dt> <dd>

Altera o formato de hora para faixas, minutos, segundos e quadros. (O MCI usa números de faixa contínuos.) Reconhecido pelos tipos de dispositivo **cdaudio** e **VCR** .

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_vídeo de conjunto de MCI \_
</dt> <dd>

Define ou desativa o sinal de vídeo. Esse sinalizador deve ser usado com o MCI \_ definido \_ como ativado ou MCI \_ definido como \_ off. Dispositivos que não têm vídeo de retorno MCIERR \_ função sem suporte \_ .

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>DGV do MCI \_ \_ definir \_ FileFormat
</dt> <dd>

Um parâmetro de formato de arquivo é incluído no membro **dwFileFormat** da estrutura identificada por *lpSet*. Para dispositivos de vídeo digital, o formato de arquivo é usado para salvar ou capturar comandos. Se omitido, isso pode padronizar para um formato definido por driver de dispositivo. Se o formato de arquivo especificado estiver em conflito com o algoritmo e a qualidade selecionados no momento, eles serão alterados para os padrões para o formato de arquivo. As seguintes constantes de formato de arquivo são definidas:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ avi
</dt> <dd>

Formato AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS
</dt> <dd>

Formato AVSS.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB
</dt> <dd>

Formato DIB.

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF
</dt> <dd>

Formato JFIF.

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG
</dt> <dd>

Formato JPEG.

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG
</dt> <dd>

Formato MPEG.

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB
</dt> <dd>

Formato de DIB RLE.

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG
</dt> <dd>

Formato RJPEG.

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI \_ DGV \_ definir \_ busca \_ exata
</dt> <dd>

Define o formato usado para posicionamento. Esse sinalizador deve ser usado com o MCI \_ definido \_ como ativado ou MCI \_ definido como \_ off. Se \_ o MCI definido \_ em for especificado, executar ou gravar precisamente acessará o quadro especificado com o \_ sinalizador MCI de. Isso pode adicionar um atraso extra se o quadro solicitado não for um quadro-chave. Se \_ o MCI definido \_ como OFF for especificado, o dispositivo buscará uma imagem de quadro-chave que precede o quadro solicitado. Para alguns arquivos e dispositivos, esse pode ser o primeiro quadro do arquivo. O padrão para esse sinalizador depende do dispositivo.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_velocidade do \_ conjunto de DGV MCI \_
</dt> <dd>

Um parâmetro Speed é incluído no membro **dwSpeed** da estrutura identificada por *lpSet*. A velocidade é especificada como uma proporção entre a taxa de quadros nominal e a taxa de quadros desejada, em que a taxa de quadros nominal é designada como 1000. Meia velocidade é 500 e a velocidade dupla é 2000. O intervalo de velocidade permitido depende do dispositivo e possivelmente do arquivo também.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_DGV MCI \_ set \_ ainda
</dt> <dd>

Quando usado com o MCI \_ DGV \_ set \_ FileFormat, \_ o MCI set define o formato de arquivo usado para comandos de captura.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpSet* aponta para uma [**estrutura \_ DGV MCI \_ set \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **Sequencer** :

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>\_formato de Seq MCI \_ \_ SONGPTR
</dt> <dd>

Define o formato de hora para as unidades de ponteiro de música.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_mestre de \_ conjunto de Seq MCI \_
</dt> <dd>

Define o Sequencer como uma fonte de dados de sincronização e indica que o tipo de sincronização é especificado no membro **dwMaster** da estrutura identificada por *lpSet*. MCISEQ retorna MCIERR \_ função sem suporte \_ . As constantes a seguir são definidas para o tipo de sincronização:

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ Midi
</dt> <dd>

O Sequencer enviará dados de sincronização de formato MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE
</dt> <dd>

O Sequencer enviará dados de sincronização de formato SMPTE.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_Seq MCI \_ None
</dt> <dd>

O sequenciador não enviará dados de sincronização.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>\_deslocamento do \_ conjunto de Seq MCI \_
</dt> <dd>

Altera o deslocamento SMPTE de uma sequência para aquela especificada pelo membro **dwOffset** da estrutura identificada por *lpSet*. Isso afeta apenas as sequências com um tipo de divisão SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_porta do \_ conjunto de Seq MCI \_
</dt> <dd>

Define a porta MIDI de saída de uma sequência para aquela especificada pelo identificador de dispositivo MIDI no membro **dwPort** da estrutura identificada por *lpSet*. O dispositivo fecha a porta anterior (se houver) e tenta abrir e usar a nova porta. Se falhar, ele retornará um erro e reabrirá a porta usada anteriormente (se houver). As constantes a seguir são definidas para as portas:

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_Seq MCI \_ None
</dt> <dd>

Fecha a porta usada anteriormente (se houver). O Sequencer se comporta exatamente como se uma porta estivesse aberta, exceto que nenhuma mensagem MIDI é enviada.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_mapeador de Midi
</dt> <dd>

Define a porta aberta para o mapeador de MIDI.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>\_slave do \_ conjunto de Seq MCI \_
</dt> <dd>

Define o Sequencer para receber dados de sincronização e indica que o tipo de sincronização é especificado no membro **dwSlave** da estrutura identificada por *lpSet*. MCISEQ retorna MCIERR \_ função sem suporte \_ . As constantes a seguir são definidas para o tipo de sincronização:

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_arquivo Seq \_ MCI
</dt> <dd>

Define o Sequencer para receber dados de sincronização contidos no arquivo MIDI.

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ Midi
</dt> <dd>

Define o Sequencer para receber dados de sincronização de MIDI.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>\_Seq MCI \_ None
</dt> <dd>

Define o Sequencer para ignorar os dados de sincronização em um fluxo de MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE
</dt> <dd>

Define o Sequencer para receber dados de sincronização do SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_tempo de \_ definição do Seq MCI \_
</dt> <dd>

Altera o tempo da sequência de MIDI para o especificado pelo membro **dwTempo** da estrutura apontada por *lpSet*. Para sequências com o tipo de divisão PPQN, o tempo é especificado em batidas por minuto; para sequências com o tipo de divisão SMPTE, o tempo é especificado em quadros por segundo.

</dd> </dl>

Para dispositivos do Sequencer, o parâmetro *lpSet* aponta para uma estrutura de [**parâmetros de \_ \_ conjunto \_ de Seq MCI**](mci-seq-set-parms.md) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_registro de \_ montagem de conjunto de VCR MCI \_ \_
</dt> <dd>

Define o dispositivo a ser gravado nos modos de montagem ou inserção (quando assemble está desativado, INSERT é on e vice-versa). Use com um dos seguintes sinalizadores:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em
</dt> <dd>

Define o registro de montagem ativado e ativa o registro de inserção. Registra todas as faixas de vídeo, áudio e código de recursos.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado
</dt> <dd>

Define o registro de montagem como off e ativa o registro de inserção. Quando o registro de montagem está desativado, faixas individuais de vídeo, áudio e código de pafica podem ser selecionadas para gravação.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_relógio de \_ conjunto de VCR MCI \_
</dt> <dd>

O membro **dwClock** da estrutura identificada por *lpSet* contém o novo horário do relógio.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>\_contador de \_ conjunto de VCR \_ MCI forma \_
</dt> <dd>

O membro **dwCounterFormat** da estrutura identificada por *lpSet* contém uma constante especificando o novo formato de hora do contador a ser usado pelo contador de status. Para obter uma lista de constantes válidas, \_ consulte \_ formato de hora Set MCI \_ na lista de sinalizadores adicionais para este comando.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>\_valor do \_ contador do conjunto de VCR MCI \_ \_
</dt> <dd>

O membro **dwCounterValue** da estrutura identificada por *lpSet* contém o novo valor do contador.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_índice de \_ conjunto de VCR MCI \_
</dt> <dd>

O membro **dwIndex** da estrutura identificada por *lpSet* contém uma constante que indica o conteúdo da exibição na tela e deve ser um dos seguintes:

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_contador de \_ índice de VCR MCI \_
</dt> <dd>

Exibe o contador.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_data do \_ índice de VCR do MCI \_
</dt> <dd>

Exibe a data.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_tempo de \_ índice de VCR do MCI \_
</dt> <dd>

Exibe a hora.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>código de meio do \_ índice de VCR MCI \_ \_
</dt> <dd>

Exibe o código de code.

Para obter mais informações, consulte o comando de [ \_ índice MCI](mci-index.md) .

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_ \_ \_ tempo limite de pausa de set de VCR MCI \_
</dt> <dd>

O membro **dwPauseTimeout** da estrutura identificada por *lpSet* contém a duração máxima, em milissegundos, de um comando PAUSE.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>duração do registro do VCR do MCI \_ \_ definido \_ \_
</dt> <dd>

O membro **dwPostrollDuration** da estrutura identificada por *lpSet* contém o comprimento da fita de vídeo, no formato de hora atual, necessário para finalizar o transporte de videocassete quando um comando Stop ou PAUSE é emitido.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_potência do \_ conjunto de VCR MCI \_
</dt> <dd>

Define ou desativa a ativação. Deve ser usado com um dos seguintes sinalizadores:

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado
</dt> <dd>

Desliga o desligamento.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em
</dt> <dd>

Ativa a ativação.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_duração da \_ preversão do conjunto de VCR MCI \_ \_
</dt> <dd>

O membro **dwPrerollDuration** da estrutura identificada por *lpSet* contém o comprimento da fita de vídeo, no formato de hora atual, necessário para estabilizar a saída do VCR.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_formato de \_ registro do conjunto de VCR MCI \_ \_
</dt> <dd>

O membro **dwRecordFormat** da estrutura identificada por *lpSet* contém uma constante que descreve a velocidade do registro, que deve ser uma das seguintes:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_EP de \_ formato \_ VCR MCI
</dt> <dd>

Registros em velocidade lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_formato de videocassete MCI \_ \_ LP
</dt> <dd>

Registros em velocidade média-lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>\_SP de \_ formato \_ VCR MCI
</dt> <dd>

Registros na velocidade padrão.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_velocidade do \_ conjunto de VCR MCI \_
</dt> <dd>

O membro **dwSpeed** da estrutura identificada por *lpSet* contém a nova configuração de velocidade, em que 1000 é velocidade normal, 2000 é de velocidade dupla e 500 é meia velocidade e assim por diante.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_tamanho da \_ fita do conjunto de VCR MCI \_ \_
</dt> <dd>

O membro **dwTapeLength** da estrutura identificada por *lpSet* contém o novo comprimento da fita, desde que o comprimento da fita não seja detectável.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>\_modo de \_ \_ tempo definido de VCR \_ do MCI
</dt> <dd>

O membro **dwTimeMode** da estrutura identificada por *lpSet* contém uma constante que indica o novo modo de tempo posicional. As seguintes constantes são válidas:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tempo de VCR MCI \_
</dt> <dd>

Força o dispositivo a usar o contador exclusivamente.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>\_detecção de \_ tempo de VCR MCI \_
</dt> <dd>

Cada vez que uma nova fita de vídeo é inserida no dispositivo ou o modo é alterado de não pronto para pronto, o dispositivo deve tentar determinar se há um código de tempo disponível na fita de vídeo. Se o código de indisponibilidade estiver disponível, use o código de sob todos os comandos subsequentes que especificam posições. Caso contrário, use o contador.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>tempo de vida de \_ hora do VCR MCI \_ \_
</dt> <dd>

Força o dispositivo a usar o código de Code exclusivamente.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_controle de \_ conjunto de VCR MCI \_
</dt> <dd>

Ajusta a velocidade do transporte de fita do VCR com um ajuste fino e deve ser usado com um dos seguintes sinalizadores:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_VCR MCI \_ Plus
</dt> <dd>

Aumenta a velocidade de transporte de fita.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>subtração de \_ VCR MCI \_
</dt> <dd>

Diminui a velocidade de transporte de fita.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>redefinição de \_ VCR MCI \_
</dt> <dd>

Retorna o ajuste de controle para zero.

</dd> </dl>

Para dispositivos VCR, o parâmetro *lpSet* aponta para uma estrutura de [**conjunto de \_ \_ \_ parâmetros do VCR MCI**](mci-vcr-set-parms.md) .

O seguinte sinalizador adicional é usado com o tipo de dispositivo **VIDEODISC** :

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_faixa de \_ formato de VD do MCI \_
</dt> <dd>

Altera o formato de hora para faixas. O MCI usa números de faixa contínuos.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_
</dt> <dd>

Define a entrada usada para gravar no membro **wInput** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_
</dt> <dd>

Define a saída usada para reproduzir o membro **wOutput** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>ANYINPUT de onda do MCI \_ \_ set \_
</dt> <dd>

Qualquer entrada de onda compatível com o formato atual pode ser usada para gravação.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>ANYOUTPUT de onda do MCI \_ \_ set \_
</dt> <dd>

Qualquer saída de Wave compatível com o formato atual pode ser usada para reprodução.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>AVGBYTESPERSEC de onda do MCI \_ \_ set \_
</dt> <dd>

Define os bytes por segundo usados para reproduzir, gravar e salvar no membro **nAvgBytesPerSec** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>BITSPERSAMPLE de onda do MCI \_ \_ set \_
</dt> <dd>

Define os bits por exemplo usado para reproduzir, gravar e salvar no membro **nBitsPerSample** do formato de dados PCM identificado por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>BLOCKALIGN de onda do MCI \_ \_ set \_
</dt> <dd>

Define o alinhamento de bloco usado para reproduzir, gravar e salvar no membro **nBlockAlign** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_canais de \_ conjunto de ondas MCI \_
</dt> <dd>

O número de canais é indicado no membro **nChannels** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>FORMATTAG de onda do MCI \_ \_ set \_
</dt> <dd>

Define o tipo de formato usado para reproduzir, gravar e salvar no membro **wFormatTag** da estrutura identificada por *lpSet*. Especificar \_ o formato Wave \_ PCM altera o formato para PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>SAMPLESPERSEC de onda do MCI \_ \_ set \_
</dt> <dd>

Define os exemplos por segundo usados para reproduzir, gravar e salvar no membro **nSamplesPerSec** da estrutura identificada por *lpSet*.

</dd> </dl>

Para dispositivos de formato de onda-áudio, o parâmetro *lpSet* aponta para uma estrutura [**MCI do \_ tipo Wave \_ set \_ parms**](mci-wave-set-parms.md) .

Várias propriedades dos dados de formato de onda-áudio são definidas quando o arquivo para armazenar os dados é criado. Essas propriedades descrevem como os dados são estruturados dentro do arquivo e não podem ser alterados após o início da gravação. A lista de sinalizadores a seguir identifica essas propriedades:

-   AVGBYTESPERSEC de onda do MCI \_ \_ set \_
-   BITSPERSAMPLE de onda do MCI \_ \_ set \_
-   BLOCKALIGN de onda do MCI \_ \_ set \_
-   \_canais de \_ conjunto de ondas MCI \_
-   FORMATTAG de onda do MCI \_ \_ set \_
-   SAMPLESPERSEC de onda do MCI \_ \_ set \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

