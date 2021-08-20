---
title: MCI_SET comando (Mmsystem.h)
description: O comando MCI \_ SET define as informações do dispositivo. Os dispositivos cd audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay e waveform-audio reconhecem esse comando.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET comando Windows Multimídia
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
ms.openlocfilehash: 7f5affb6ce41c5c321b24353ece8f0946dc668194ac59cee95e579178a8b03df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803381"
---
# <a name="mci_set-command"></a>Comando MCI \_ SET

> [!NOTE]
> Comunicação sem preconceitos A Microsoft dá suporte a um ambiente diversificado e inclusões.  Neste documento, há referências à palavra 'slave'. O Guia de Estilo da Microsoft [para Bias-Free Comunicações](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Esse texto é usado, pois é atualmente o texto usado dentro dos comandos. Para consistência, este documento contém essa palavra. Quando essa palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.

O comando MCI \_ SET define as informações do dispositivo. Os dispositivos cd audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay e waveform-audio reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI WAIT ou, para dispositivos de vídeo digital e \_ VCR, MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Ponteiro para uma [**estrutura MCI \_ SET \_ PARMS.**](mci-set-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que suportam MCI \_ SET:

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ SET \_ AUDIO
</dt> <dd>

Um número de canal de áudio é incluído no membro dwAudio da estrutura identificada por *lpSet*. Esse sinalizador deve ser usado com MCI \_ SET \_ ON ou MCI SET \_ \_ OFF. Use uma das seguintes constantes para indicar o número do canal:

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ SET \_ AUDIO \_ ALL
</dt> <dd>

Todos os canais de áudio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ SET \_ AUDIO \_ LEFT
</dt> <dd>

Canal esquerdo.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ SET \_ AUDIO \_ RIGHT
</dt> <dd>

Canal direito.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>PORTA DO CONJUNTO DE MCI \_ \_ \_ FECHADA
</dt> <dd>

Fecha a cobertura de mídia (se há).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI \_ SET \_ DOOR \_ OPEN
</dt> <dd>

Abre a cobertura de mídia (se for o caso).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ SET \_ OFF
</dt> <dd>

Desabilita o canal de áudio ou vídeo especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ SET \_ ON
</dt> <dd>

Habilita o canal de áudio ou vídeo especificado.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>FORMATO DE HORA \_ \_ DO CONJUNTO DE MCI \_
</dt> <dd>

Um parâmetro de formato de hora é incluído no **membro dwTimeFormat** da estrutura identificada por *lpSet*. Os sinalizadores a seguir são usados com este sinalizador:

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>BYTES DE FORMATO \_ MCI \_
</dt> <dd>

Em um formato de dados PCM (Pulse Code Modulartion), altera a descrição do membro de tempo para bytes para entrada ou saída. Reconhecido pelo tipo **de dispositivo waveaudio.**

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>QUADROS DE FORMATO MCI \_ \_
</dt> <dd>

Os comandos subsequentes usarão quadros. Reconhecido pelos tipos **de dispositivo digitalvideo,** **vcr** e **videodisc.**

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>FORMATO MCI \_ \_ HMS
</dt> <dd>

Altera o formato de hora para horas, minutos e segundos. Reconhecido pelos tipos **de dispositivo vcr** **e videodisc.**

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>FORMATO MCI \_ \_ MILISSEGUNDOS
</dt> <dd>

Altera o formato de hora para milissegundos. Reconhecido por todos os tipos de dispositivo.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>\_MSF DE \_ FORMATO MCI
</dt> <dd>

Altera o formato de hora para minutos, segundos e quadros. Reconhecido pelos tipos **de dispositivo cdaudio** **e vcr.**

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>EXEMPLOS DE FORMATO MCI \_ \_
</dt> <dd>

Altera o formato de hora para exemplos de entrada ou saída. Reconhecido pelo tipo **de dispositivo waveaudio.**

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>FORMATO MCI \_ \_ SMPTE \_ 24, FORMATO MCI \_ \_ SMPTE \_ 25 e FORMATO \_ \_ MCI SMPTE \_ 30
</dt> <dd>

Define o formato de hora como 24, 25 e 30 quadros SMPTE (Society of Motion Picture and Tv Engineers), respectivamente. Reconhecido pelos tipos **de dispositivo sequencer** **e vcr.**

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI \_ FORMAT \_ SMPTE \_ 30DROP
</dt> <dd>

Define o formato de hora como 30 SMPTE de quadro-soltar. Reconhecido pelos tipos **de dispositivo sequencer** **e vcr.**

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>TMSF DE \_ \_ FORMATO MCI
</dt> <dd>

Altera o formato de hora para faixas, minutos, segundos e quadros. (A MCI usa números de faixa contínua.) Reconhecido pelos tipos **de dispositivo cdaudio** **e vcr.**

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>VÍDEO DO MCI \_ SET \_
</dt> <dd>

Define o sinal de vídeo como on ou off. Esse sinalizador deve ser usado com MCI \_ SET \_ ON ou MCI SET \_ \_ OFF. Dispositivos que não têm vídeo retornam a FUNÇÃO SEM \_ SUPORTE DO MCIERR. \_

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Os seguintes sinalizadores adicionais são usados com o **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ SET \_ FILEFORMAT
</dt> <dd>

Um parâmetro de formato de arquivo é incluído no **membro dwFileFormat** da estrutura identificada por *lpSet*. Para dispositivos de vídeo digital, o formato de arquivo é usado para salvar ou capturar comandos. Se omitido, isso pode ser padrão para um formato definido pelo driver de dispositivo. Se o formato de arquivo especificado entrar em conflito com o algoritmo e a qualidade selecionados no momento, eles serão alterados para os padrões do formato de arquivo. As seguintes constantes de formato de arquivo são definidas:

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

Formato AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ AVSS
</dt> <dd>

Formato AVSS.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>\_DGV \_ FF \_ DIB da MCI
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

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ SSEB
</dt> <dd>

Formato DIB RLE.

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

O **membro dwPrerollDuration** da estrutura identificada por *lpSet* contém o comprimento da fita, no formato de hora atual, necessário para estabilizar a saída do VCR.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>FORMATO DE REGISTRO \_ DO CONJUNTO DE VCR \_ \_ DA \_ MCI
</dt> <dd>

O **membro dwRecordFormat** da estrutura identificada por *lpSet* contém uma constante que descreve a velocidade do registro, que deve ser uma das seguintes:

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>EP DE \_ FORMATO VCR \_ DA MCI \_
</dt> <dd>

Registros em velocidade lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>LP DE \_ FORMATO VCR \_ da MCI \_
</dt> <dd>

Registros em velocidade média e lenta.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>FORMATO DE VCR DA MCI \_ \_ \_ SP
</dt> <dd>

Registros em velocidade padrão.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>VELOCIDADE DO CONJUNTO \_ DE VCR \_ DA MCI \_
</dt> <dd>

O **membro dwSpeed** da estrutura identificada por *lpSet* contém a nova configuração de velocidade, em que 1000 é a velocidade normal, 2000 é velocidade dupla e 500 é a metade da velocidade e assim por diante.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>COMPRIMENTO DA FITA DO CONJUNTO \_ DE VCR \_ \_ DA \_ MCI
</dt> <dd>

O **membro dwTapeLength** da estrutura identificada por *lpSet* contém o novo comprimento da fita, desde que o comprimento da fita não seja detectável.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MODO DE TEMPO \_ DEFINIDO PELO VCR \_ \_ DA \_ MCI
</dt> <dd>

O **membro dwTimeMode** da estrutura identificada por *lpSet* contém uma constante que indica o novo modo de tempo posicional. As seguintes constantes são válidas:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>CONTADOR DE TEMPO \_ DO VCR \_ da MCI \_
</dt> <dd>

Força o dispositivo a usar o contador exclusivamente.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>DETECÇÃO DE TEMPO \_ DO VCR \_ da MCI \_
</dt> <dd>

Sempre que um novo ataque for inserido no dispositivo ou o modo mudar de não pronto para pronto, o dispositivo deverá tentar determinar se há um código de hora disponível no local. Se o código de hora estiver disponível, use o código de data/hora em todos os comandos subsequentes que especifiquem posições. Caso contrário, use o contador .

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI \_ VCR \_ TIME \_ TIMECODE
</dt> <dd>

Força o dispositivo a usar o código de hora exclusivamente.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>ACOMPANHAMENTO DE CONJUNTO \_ DE VCR \_ DA MCI \_
</dt> <dd>

Ajusta a velocidade do transporte em fita VCR com um ajuste fino e deve ser usado com um dos seguintes sinalizadores:

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>VCR \_ PLUS da MCI \_
</dt> <dd>

Aumenta a velocidade de transporte de fita.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ MINUS
</dt> <dd>

Diminui a velocidade de transporte de fita.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>REDEFINIÇÃO DE VCR da MCI \_ \_
</dt> <dd>

Retorna o ajuste de acompanhamento para zero.

</dd> </dl>

Para dispositivos VCR, o *parâmetro lpSet* aponta para uma [**estrutura MCI \_ VCR SET \_ \_ PARMS.**](mci-vcr-set-parms.md)

O sinalizador adicional a seguir é usado com o **tipo de dispositivo videodisc:**

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>FAIXA DE \_ FORMATO VD \_ da MCI \_
</dt> <dd>

Altera o formato de hora para faixas. A MCI usa números de faixa contínua.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o **tipo de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>ENTRADA DE ONDA MCI \_ \_
</dt> <dd>

Define a entrada usada para gravação para **o membro wInput** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>SAÍDA DE ONDA DA MCI \_ \_
</dt> <dd>

Define a saída usada para reprodução para o **membro wOutput** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI \_ WAVE \_ SET \_ ANYINPUT
</dt> <dd>

Qualquer entrada de onda compatível com o formato atual pode ser usada para gravação.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI \_ WAVE \_ SET \_ ANYOUTPUT
</dt> <dd>

Qualquer saída de onda compatível com o formato atual pode ser usada para reprodução.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI \_ WAVE \_ SET \_ AVGBYTESPERSEC
</dt> <dd>

Define os bytes por segundo usados para reprodução, gravação e gravação no **membro nAvgBytesPerSec** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI \_ WAVE \_ SET \_ BITSPERSAMPLE
</dt> <dd>

Define os bits por exemplo usados para reprodução, gravação e gravação no **membro nBitsPerSample** do formato de dados PCM identificado por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI \_ WAVE \_ SET \_ BLOCKALIGN
</dt> <dd>

Define o alinhamento de bloco usado para reprodução, gravação e gravação no **membro nBlockAlign** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>CANAIS DO CONJUNTO \_ DE \_ ONDA DA \_ MCI
</dt> <dd>

O número de canais é indicado no membro **nChannels** da estrutura identificada por *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>FORMATTAG DO CONJUNTO \_ \_ DE ONDA \_ DA MCI
</dt> <dd>

Define o tipo de formato usado para reprodução, gravação e gravação no **membro wFormatTag** da estrutura identificada por *lpSet*. Especificar o PCM WAVE \_ FORMAT altera o formato para \_ PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI \_ WAVE \_ SET \_ SAMPLESPERSEC
</dt> <dd>

Define os exemplos por segundo usados para reprodução, gravação e gravação no **membro nSamplesPerSec** da estrutura identificada por *lpSet*.

</dd> </dl>

Para dispositivos waveform-audio, o *parâmetro lpSet* aponta para uma [**estrutura MCI WAVE SET \_ \_ \_ PARMS.**](mci-wave-set-parms.md)

Várias propriedades de dados waveform-audio são definidas quando o arquivo para armazenar os dados é criado. Essas propriedades descrevem como os dados são estruturados dentro do arquivo e não podem ser alterados depois que a gravação é iniciada. A lista de sinalizadores a seguir identifica estas propriedades:

-   MCI \_ WAVE \_ SET \_ AVGBYTESPERSEC
-   MCI \_ WAVE \_ SET \_ BITSPERSAMPLE
-   MCI \_ WAVE \_ SET \_ BLOCKALIGN
-   CANAIS DO CONJUNTO \_ DE \_ ONDA DA \_ MCI
-   FORMATTAG DO CONJUNTO \_ \_ DE ONDA \_ DA MCI
-   MCI \_ WAVE \_ SET \_ SAMPLESPERSEC

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

